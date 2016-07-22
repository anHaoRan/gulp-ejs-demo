# gulp-ejs-demo
gulp+ejs 合并静态页模版，文件更新自动热重载。

* `npm install`  安装依赖
* `gulp dev` 启动一个自动热重载的服务器，默认端口3000
* `gulp ejs` 合并模版，服务器启动时会自动监听文件更新执行该任务
 
## 流程

1. 模板编码，即 `templates/` 目录，页面入口以 `.html` 结尾，分支模版以 `.ejs` 结尾，没有目录结果限制，按需引入或编写新的页面模块。在这个阶段可以启动服务器 `gulp dev` 进行实时页面预览。
2. 编写数据文件，分为全局数据文件 `global.json` 和页面数据文件，使用通用的 `json` 格式。全局数据文件必须放到模版根目录，一个页面对应一个同名的数据文件同级目录。数据中可以写，比如： `title：页面标题` 、`styles：依赖的样式文件路径`、 `scripts：依赖的脚本文件路径` ，随时可以根据实际情况添加新的数据项。
3. 执行 `gulp ejs` 任务，生成页面到 `html/` 目录，如果之前启动了热重载服务器不需要这一步。


## 其他

实际工作中肯定还会搭配其他任务一起运行，比如：css 和 js 相关任务。此 Demo 中省略，可根据各自项目情况自行更改。
