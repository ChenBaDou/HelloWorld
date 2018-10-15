##脚手架使用说明
该项目基于`nodejs`，使用前请安装最新版本`nodejs`。

打开终端，进入到该项目所在路径，然后通过`npm i --save-dev`或者通过`yarn install -D`来安装包依赖,安装完成后再在终端中输入`sh start.sh`按enter后会在终端上有提示信息显示。
 
<mark>注意：如果要集合`vue`、`react`开发使用，请拉取对应分支。</mark>  


####1、start.sh文件
该文件会监控开发环境中的`webpack`文件变化而自动重启`webpack`服务。


####2、bulid_package.sh文件

该文件是执行打包命令文件，依赖于所在`git`分支打包不同环境。例如：

`bug_**`分支打本地开发环境包，

`dev_**`分支打本地开发环境包，

`hotfix`分支打本地开发环境包，

`test`分支打测试环境包，

`release`分支打准生产环境包，

`master`分支打生产环境包。

####4、webpack.config.babel.js打包配置文件
主要关注`defaults`配置,需经常修改的webpack配置项

```javascript
devServer       服务配置

entry           入口文件

providePlugin   全局变量设置

resolve         引用第三方库,设置别名  (util库就可当第三方库引入)

HtmlPlugin      html文件模板 
```
`HtmlPlugin`具体参考`html-webpack-plugin` [用法](https://doc.webpack-china.org/plugins/html-webpack-plugin)

次要关注 `config` 配置,如需做`webpack`深层次配置,请按`webpack`配置配到`config`即可;

####5、config.json配置文件

不同环境接口地址配置文件。也可以自定义扩展，但是得同时修改`webpack.babel.js`的`urlData`函数
