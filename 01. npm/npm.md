# npm

国内镜像下载地址 https://registry.npm.taobao.org
设置方式为npm config set registry https://registry.npm.taobao.org 设置好后，通过命令npm config get registry进行检查

npm 安装一个包两种方式

本地安装 npm i 包名
全局安装 npm i -g 包名
重要：全局安装的包并非所有工程可用，它仅提供全局的 CLI 工具

可以通过命令npm config get prefix查看全局安装目录

大部分情况下，都不需要全局安装包，除非：

包的版本非常稳定，很少有大的更新
提供的 CLI 工具在各个工程中使用的非常频繁
CLI 工具仅为开发环境提供支持，而非部署环境
npm
npm init --yes/ npm init -y 所有配置默认值

## 本地安装所有依赖 dependencies + devDependencies
npm install
npm i

## 仅安装生产环境的依赖 dependencies
npm install --production
安装依赖到生产环境
npm i 包名

npm i --save 包名

npm i -S 包名

安装依赖到开发环境
npm i --save-dev 包名

npm i -D 包名

npm 还对某些常用的脚本名称进行了简化，下面的脚本名称是不需要使用run的：

start stop test

一些细节：

脚本中可以省略npx

start脚本有默认值：node server.js

运行环境
开发环境
生产环境
测试环境
node获取环境 process.env.NODE_ENV

设置环境 package.json里面设置

设置环境为开发环境，并且运行node index.js命令

"scripts": { "start": "set NODE_ENV=development&&node index.js" },

为了避免不同系统的设置方式的差异，可以使用第三方库 cross-env 对环境变量进行设置

"jquery": "^3.1.4" //表示版本3固定，后面的1.4版本是可以变化的

npm root 查询包安装路径

npm root -g 查询包安装全局路径

npm view webpack

npm v react versions npm info vue npm show vue

查询安装包

npm list 查看本地安装的包 npm list -g 查看全局安装的包 npm ls --depth=0 直接依赖的包 npm ll --depth=2 第二级第三级依赖包

list aliases: ls la ll

npm outdated 检查需要更新的包

npm update [-g] [包名] 更新包

update 别名（aliases）：up、upgrade

npm uninstall [-g] 包名

uninstall aliases: remove, rm, r, un, unlink

npm 配置
npm config ls [-l] [--json] 查询目前生效的各种配置

npm config get 配置项 获取某个配置项

npm config set 配置项=值 设置某个配置项

npm config delete 配置项 移除某个配置项