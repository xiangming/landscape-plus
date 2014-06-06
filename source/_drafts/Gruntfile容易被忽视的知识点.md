title: caogao
tags:

---

## 起因
折腾hexo时，看到了其内置主题（landscape）的Gruntfile.js:
```javascript
module.exports = function(grunt){
  grunt.initConfig({
    gitclone: {
      fontawesome: {
        options: {
          repository: 'https://github.com/FortAwesome/Font-Awesome.git',
          directory: 'tmp/fontawesome'
        },
      },
      fancybox: {
        options: {
          repository: 'https://github.com/fancyapps/fancyBox.git',
          directory: 'tmp/fancybox'
        }
      }
    },
    copy: {
      fontawesome: {
        expand: true,
        cwd: 'tmp/fontawesome/fonts/',
        src: ['**'],
        dest: 'source/css/fonts/'
      },
      fancybox: {
        expand: true,
        cwd: 'tmp/fancybox/source/',
        src: ['**'],
        dest: 'source/fancybox/'
      }
    },
    _clean: {
      tmp: ['tmp'],
      fontawesome: ['source/css/fonts'],
      fancybox: ['source/fancybox']
    }
  });

  require('load-grunt-tasks')(grunt);

  grunt.renameTask('clean', '_clean');

  grunt.registerTask('fontawesome', ['gitclone:fontawesome', 'copy:fontawesome', '_clean:tmp']);
  grunt.registerTask('fancybox', ['gitclone:fancybox', 'copy:fancybox', '_clean:tmp']);
  grunt.registerTask('default', ['gitclone', 'copy', '_clean:tmp']);
  grunt.registerTask('clean', ['_clean']);
};
```

---

## 发现
在上面的Gruntfile.js文件中，有三个容易被忽视的方法（思路）：

### 临时存储区
作者使用一个tmp目录来临时存放gitclone下来的文件，取出自己需要的部分`fontawesome/fonts/`和`fancybox/source/`，然后删掉temp。

### 自动加载依赖
当你的`Gruntfile.js`里面只有少数的任务时，是否使用`load-grunt-tasks`无关紧要；当你有非常多任务需要load时，你就要像下面这样`loadNpmTasks`下去：
```javascript
//加载插件
    grunt.loadNpmTasks('grunt-contrib-uglify');
    grunt.loadNpmTasks('grunt-contrib-less');
    grunt.loadNpmTasks('grunt-contrib-cssmin');
    grunt.loadNpmTasks('grunt-contrib-watch');
    ...
    ...
    ...
```
其实，你只需要像下面这样，使用插件，让它帮你去load依赖。
```javascript
require('load-grunt-tasks')(grunt);
```
使用`load-grunt-tasks`这个插件的作用就很明显了。

### 子任务
这点一般大家都知道，不过还是提一下：
```javascript
'gitclone:fontawesome'
```
只执行`gitclone`的`fontawesome`子任务。