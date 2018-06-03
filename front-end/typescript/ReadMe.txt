下载TypeScript
npm install -g typescript

下载VSCode


创建项目
  创建package.json
    使用命令npm init [-yes]来创建package.json文件，一般默认就可以，具体详情可以看这里。

  创建tsconfig.json
    使用tsc --init命令就可以快速创建一个tsconfig.json文件，关于tsconfig.json的属性描述请访问这里。

  安装项目依赖和开发依赖
     npm install @types/jquery @types/bootstrap -save-dev
	 
  创建index.html

  
  创建index.ts文件并编写TS代码

  
编译和启动项目
vscode：点击菜单 任务-运行任务，点击 tsc:构建-tsconfig.json
编译快捷键：Ctrl + Shift + B
vscode自动生成js代码，点击菜单 任务-运行任务 点击 tsc:监视-tsconfig.json 

命令行：我们使用package.json中的scripts来编译和启动项目。
编译比较简单，tsc命令就可以编译项目，tsc -w命令监控并自动编译，编译会使用tsconfig.json中的配置项。


安装完毕后，我们修改package.json中的scripts如下：
"scripts": {
    "test": "tsc -w "
}
 npm run start

 
/**  
启动项目我们安装live-server，来帮助我们启动一个服务器环境，live-server非常轻便且带有自动刷新功能，我们使用npm全局安装即可：
npm install -g live-server
"scripts": {
    "test": "tsc -w & live-server"
}
**/

运行构建任务
如果node.js已经被安装，你能运行你的helloworld例子通过打开一个终端然后运行
node HelloWorld.js


----Debug配置
Ctrl + Shift + D 点击配置图标，选择nodejs



常用快捷键：
跳转标记&展示所有标记
ctrl+shift+o：列出所有定义符号关于当前打开和允许您在其中导航。
ctrl+T：让你搜索当前项目中或文件范围中所有定义的标记。你需要有一个typescript文件打开在编辑器中。
格式化代码
shift+alt+f:格式化整个文档。ctrl+k ctrl+f：格式化当前选择的资源代码。
注释：
a) 单行注释：[ctrl+k,ctrl+c] 或 ctrl+/
b) 取消单行注释：[ctrl+k,ctrl+u] (按下ctrl不放，再按k + u)
c) 多行注释：[alt+shift+A]