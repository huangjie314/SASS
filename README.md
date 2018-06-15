# SASS
项目使用SASS来编写样式
## 编译sass

`sass`编译有很多种方式，如命令行编译模式、sublime插件`SASS-Build`、编译软件`koala`、前端自动化软件`codekit`、Grunt打造前端自动化工作流`grunt-sass`、Gulp打造前端自动化工作流`gulp-ruby-sass`等。 

### 命令行编译

~~~
//单文件转换命令
sass input.scss output.css

//单文件监听命令
sass --watch input.scss:output.css

//如果你有很多的sass文件目录，你可以告诉sass监听整个目录：
sass --watch app/sass:public/stylesheets
~~~

### 命令行编译配置选项

命令行编译`sass`有配置选项，如编译过后css排版、生成调试map、开启debug信息等，可通过使用命令`sass -v`查看详细。我们一般常用两种`--style``--sourcemap` 

~~~
//编译格式
sass --watch input.scss:output.css --style compact

//编译添加调试map
sass --watch input.scss:output.css --sourcemap

//选择编译格式并添加调试map
sass --watch input.scss:output.css --style expanded --sourcemap

//开启debug信息
sass --watch input.scss:output.css --debug-info
~~~

* `--style`表示解析后的css是什么排版格式：
  * `--style nested` 嵌套缩进的css代码，它是默认值；
  * `--style expanded` 没有缩进的、扩展的css代码；
  * `--style compact` 简洁格式的css代码；
  * `--style compressed` 压缩后的css代码；
* `--sourcemap`表示开启`sourcemap`调试。开启`sourcemap`调试后，会生成一个后缀名为`.css.map`文件。
