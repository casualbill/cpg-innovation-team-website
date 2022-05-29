# 正大创新团队官方网站前端项目
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=CPG-Innovation-Team_cpg-innovation-team-website&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=CPG-Innovation-Team_cpg-innovation-team-website) 
[![CircleCI](https://circleci.com/gh/CPG-Innovation-Team/cpg-innovation-team-website/tree/master.svg?style=svg)](https://circleci.com/gh/CPG-Innovation-Team/cpg-innovation-team-website/tree/master)
[![codecov](https://codecov.io/gh/CPG-Innovation-Team/cpg-innovation-team-website/branch/master/graph/badge.svg?token=CA7DJRBY7X)](https://codecov.io/gh/CPG-Innovation-Team/cpg-innovation-team-website)

## 系统依赖
需要安装 [Node.js](https://nodejs.org), 在版本 Node.js 14.17上稳定运行
    
## 本地运行
- 首次运行或有依赖变更时执行安装 `npm install`

- 启动本地服务 `npm run serve`

- 编译生产环境代码包 `npm run build`

- 执行单元测试 `npm run test:unit`

- 执行代码校验 `npm run lint`

## 规范及标准
1. 命名规范
   1. 文件名：
      1. Vue 组件文件：使用大驼峰，扩展名为 vue。如：ExampleComponent.vue
      2. 脚本文件：使用小驼峰，扩展名为 js。如：exampleLogic.js
      3. 资源文件：
         1. 图标：使用小写字母以 icon 起始并使用"-"链接。如：icon-example-icon.png
         2. 背景图片：使用小写字母以 bg 起始并使用"-"链接。如：bg-example-background.jpg
         3. 广告图片：使用小写字母以 ad 起始并使用"-"链接。如：ad-example-advertisement.jpg
         4. 其他无分类图片：使用小写字母以 img 起始并使用"-"链接。如：img-example-image.jpg
         5. 视频：使用小写字母以 video 起始并使用"-"链接。如：video-example-video.mp4
         6. 扩展名小写，JPEG 格式以 .jpg 为统一扩展名
   2. Vue 组件名：使用大驼峰，并与文件名一致。如：ExampleComponent
   3. 变量、方法名：使用小驼峰。如：exampleVariable、exampleFunction
   4. 常量名：使用大写字母下划线分隔。如：EXAMPLE_CONST
   5. 样式名：全小写并使用"-"连接。如：example-style
   6. 命名规则：使用英语单词组合，见文知义，不简写
2. 代码规范及校验：
   1. 采用 [Airbnb](https://github.com/airbnb/javascript) 标准定义代码规范
   2. 使用 [ESLint](https://eslint.org/) 进行代码校验
   3. 使用 [Yorkie](https://github.com/yyx990803/yorkie) 作为 GitHooks 预提交校验
3. 代码风格： 
   1. 使用空格缩进，缩进量为2个空格
   2. 单行不超过120个字符
   3. 使用 [Prettier](https://prettier.io/) 统一代码风格并自动格式化
4. 提交信息（Commit Message)：可以准确描述本次提交的涉及的功能模块和具体修改内容，非相关内容请分开多次提交

## 项目结构
```
.
├── README.md   项目说明文档
├── babel.config.js     Babel配置文件
├── jest.config.js      Jest单元测试配置文件
├── package-lock.json   项目依赖版本配置文件
├── package.json    项目配置文件
├── public
│   ├── favicon.ico     网站图标
│   └── index.html      网站HTML模板
├── src
│   ├── App.vue     全局页面
│   ├── Event.js    事件总线文件
│   ├── assets      静态资源文件目录，含图片、视频等
│   ├── components      公用组件目录
│   │   ├── AdminNav.vue    后管顶部导航栏
│   │   ├── Charts
│   │   │   └── Traffic.vue
│   │   ├── Editor.vue      富文本编辑器组件
│   │   ├── Footer.vue      主页底部导航栏
│   │   ├── GalleryLabel.vue    图片瀑布流标签组件
│   │   ├── HeaderNav.vue   主页顶部导航栏
│   │   └── RollingGallery.vue      主页图片瀑布流组件
│   ├── data    数据文件目录
│   ├── lang    语言文件目录
│   ├── main.js     项目入口文件
│   ├── plugins     插件目录
│   │   ├── vue-i18n.js     i18n国际化配置文件
│   │   └── vuetify.js      UI组件库Vuetify配置文件
│   ├── router.js       路由文件
│   ├── util.js     公用方法文件
│   └── views       页面目录
│       ├── AboutUs.vue     关于我们页面
│       ├── Blog.vue    博客页面
│       ├── BlogDetail.vue      博客详情页面
│       ├── Homepage.vue    主页
│       ├── ProjectInfo.vue     项目介绍页面
│       ├── RecruitmentDetail.vue   招聘详情页面
│       ├── RecruitmentInfo.vue     招聘信息页面
│       ├── SearchResults.vue       搜索结果页面
│       ├── TeamInfo.vue        团队介绍页面
│       └── admin   后台管理系统目录
│           ├── AccessDenied.vue    无权限访问页面
│           ├── Announcement.vue    公告页面
│           ├── Approval.vue    审核页面
│           ├── ApproveBlog.vue     审核博客页面
│           ├── Blogs.vue   博客管理页面
│           ├── ChangePassword.vue      修改密码页面
│           ├── CreateBlog.vue      创建博客页面
│           ├── Dashboard.vue   仪表盘页面
│           ├── Login.vue       登陆页面
│           ├── Permission.vue  权限管理页面
│           ├── Profile.vue     用户资料页面
│           ├── Signup.vue      注册页面
│           ├── UpdateBlog.vue  更新博客页面
│           └── Users.vue       用户管理页面
├── tests
│   ├── e2e     e2e测试目录
│   └── unit    单元测试目录
└── vue.config.js
```

## 技术栈
Vue.js

### UI组件库
[Vuetify](https://vuetifyjs.com/zh-Hans/)

### 集成工具
- 自动化构建部署 [CircleCI](https://app.circleci.com/pipelines/github/CPG-Innovation-Team/cpg-innovation-team-website)
- 代码质量静态扫描 [SonarCloud](https://sonarcloud.io/project/overview?id=CPG-Innovation-Team_cpg-innovation-team-website)
- 单元测试覆盖率报告 [Codecov](https://app.codecov.io/gh/CPG-Innovation-Team/cpg-innovation-team-website)
