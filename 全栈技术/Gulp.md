前端重構文檔2.0

1、环境搭建：安装Node环境

下载地址：[https://nodejs.org/en/download/](https://nodejs.org/en/download/)

2、安装Gulp和Gulp插件 

npm install -g gulp （全局安装）

npm install --save-dev gulp  

安装好后确认是否安装成功，再次输入gulp -v查看版本号  

svn根目录下已有package.json文件  

只需 npm install

会自动安装以下gulp插件 

npm install --save-dev gulp-rev 

npm install --save-dev gulp-rev-collector 

npm install --save-dev gulp-asset-rev 

npm install --save-dev run-sequence 

3、修改rev的配置文件以实现参数格式后缀（?v=d8a9eda343）

在项目根目录webapp下 

打开node_modules\gulp-rev\index.js 

//第144行

manifest[originalFile] = revisionedFile;

//更新为:

manifest[originalFile] = originalFile + ‘?v=’ + file.revHash;

打开node_modules\rev-path\index.js

//9行

return modifyFilename(pth, (filename, ext) => {'$filename + $ext'});

//更新为:

return modifyFilename(pth, (filename, ext) => filename + ext);

打开node_modules\gulp-rev-collector\index.js

let cleanReplacement =  path.basename(json[key]).replace(new RegExp( opts.revSuffix ), '' );

//修改为：

 let cleanReplacement =  path.basename(json[key]).split('?')[0];

4、开始构建项目

项目根目录下已有个gulpfile.js文件，进入项目根目录下，

在CMD 命令窗口下执行：

cd D:\JE-1\JE-1\050编码\020Cloud\jhWeb\jhCloud\src\main\webapp

gulp default