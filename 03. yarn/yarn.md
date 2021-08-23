# yarn

cd yarn 进入到yarn文件夹中

cd .. 返回上级目录

yarn init 初始化包

yarn add [package] 安装包命令

yarn remove [package] [package-name]

yarn run CLI名称 运行本地安装的CLI

yarn bin 查看bin目录

yarn global bin 查看全局bin目录

yarn info react 查看react,查看的东西太多不建议用

yarn info react versions 查看react版本

yarn info react readme 查看react readme

yarn outdated 查看需要更新的包

yarn check 可以验证package.json文件的依赖记录和lock文件是否一致

yarn audit

使用yarn audit命令，可以检查本地安装的包有哪些已知漏洞，以表格的形式列出，漏洞级别分为以下几种：

INFO：信息级别
LOW: 低级别
MODERATE：中级别
HIGH：高级别
CRITICAL：关键级别
yarn why 可以在控制台打印出为什么安装了这个包，哪些包会用到它

yarn create react-app my-app

等同于下面的两条命令

yarn global add create-react-app create-react-app my-app
