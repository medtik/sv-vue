# Solar Value Web APP

<p align="center">
    <a href="https://vuejs.org" target="_blank" rel="noopener noreferrer">
        <img width="200" src="https://avatars1.githubusercontent.com/u/41156540?s=200&v=4" alt="Vue logo">
    </a>
</p>
<p align="center">A Web App dev for Solar Value</p>
<p align="center">
  <a href="https://circleci.com/gh/vuejs/vue/tree/dev"><img src="https://img.shields.io/circleci/project/vuejs/vue/dev.svg" alt="Build Status"></a>
  <a href="https://codecov.io/github/vuejs/vue?branch=dev"><img src="https://img.shields.io/codecov/c/github/vuejs/vue/dev.svg" alt="Coverage Status"></a>
  <a href="https://npmcharts.com/compare/vue?minimal=true"><img src="https://img.shields.io/npm/dm/vue.svg" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/v/vue.svg" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/l/vue.svg" alt="License"></a>
</p>

![N](./doc/sv-pc-demo.png)

## Start

``` npm
npm install
npm run serve // dev
npm run build // publish
```

## Work Plan

- 第一阶段：APP 静态原型开发（1周）

| 任务名称 | 开始时间 | 预测结束 | 实际结束 | 负责人 |
| :-------- | :--------: | :----------: | :-----------: | :-----: |
| `DataTable` 组件开发 + `Summary` 页面 | 2018/07/31 | 2018/07/31 | 达标 | DengDeng |
| `Event 页` + 根据设计图调整 + `highcharts` 配置 | 2018/07/31 | 2018/07/31 | 达标 | ZhanQuan |
| `多项目` 与 `单项目` 剩余页面搭建 | 2018/08/01 | 2018/08/01 | 达标 | DengDeng |
| 所有项目 `highchart` 图表配置, `Google` 谷歌地图组件 | 2018/08/01 | 2018/08/01 | 达标 | ZhanQuan |
| `下拉无限懒加载列表`组件 + `单项目Detail页面` | 2018/08/02 | 2018/08/02 | 达标 | DengDeng |
| 日历组件 `vue-event-calendar` 开发与改造 | 2018/08/03 | 2018/08/03 | 达标 | DengDeng |

- 第二阶段： APP 业务逻辑与接口联调（1周）

| 任务名称 | 开始时间 | 预测结束 | 实际结束 | 负责人 |
| :-------- | -------- | ---------- | :-----------: | :-----: |
| `axios` 请求模块封装,Nodejs 开发环境跨域代理 | 2018/08/06 | 2018/08/06 | 达标 | DengDeng |
| Portfolio `highcharts` 图表与 `Projectlist` 接口联调  | 2018/08/07 | 2018/08/07 | 达标 | DengDeng |
| Energy `highcharts` 图表与 `Projectlist` 接口联调 | 2018/08/08 | 2018/08/08 | 达标 | DengDeng |
| Portfolio 图表点击事件联动加载数据 | 2018/08/09 | 2018/08/09 | 达标 | DengDeng |
| 登录接口联调 + tab分页加载项目文档功能 | 2018/08/10 | 2018/08/11 | 达标 | DengDeng |
| 周末加班，与波哥共同接口联调，修复图表联动 `bug` | 2018/08/12 | 2018/08/12 | - | DengDeng |

- 第三阶段： APP 测试返修与上线优化（1周）

| 任务名称 | 开始时间 | 预测结束 | 实际结束 | 负责人 |
| :-------- | -------- | ---------- | ----------- | :-----: |
| 谷歌地图联调，多项目顶部菜单改造,搜索功能样式 | 2018/08/13 | 2018/08/13 | 达标 | DengDeng |
| 完成 `Energy/Table` 的拼接联调接口 | 2018/08/14 | 2018/08/14 | 达标 | DengDeng |
| 新增月份选择控件，修改日期联动发电量图表 | 2018/08/15 | 2018/08/15 | 达标 | DengDeng |
| 调试剩余接口 | 2018/08/16 | 2018/08/16 | 达标 | DengDeng |
| 发电量图表接口联调与组件开发 | 2018/08/17 | 2018/08/17 | 达标 | Zhangquan |

- 第四阶段： APP 性能优化与体验升级（1周）

| 任务名称 | 开始时间 | 预测结束 | 实际结束 | 负责人 |
| :-------- | -------- | ---------- | ----------- | :-----: |
| 登陆时报错弹窗，`loading` 骨架屏 | 2018/08/20 | 2018/08/20 | - | DengDeng |
    
## Restful API

| 名称 | 类型 | URL |
| :---- | ---- | :---- |
| 用户登陆 | POST | /account/loginForMB?loginName=panbo&password=xxx |
| 用户注销 | POST | /account/logoutForMB |
| 项目分类 | GET | /api/collection/list |
| 多项目总览项目列表 | GET | /api/collection/projects?id=1&page=1&pageSize=10|
| 指标面板数据 | GET | /api/widgets/data?cid=1&type=summary |
| portfolio项目地区分布 | GET | /api/portfolio/region?id=1 |
| portfolio三联动图表 | GET | /api/portfolio/chats?id=1&region=Kyushu&fit=40&codYears=0-5 |
| portfolio项目列表 | GET | /api/portfolio/projects?id=1&region=Kyushu&fit=40&codYears=0-5 &page=1&pageSize=10 |
| portfolio指标面板 | GET | /api/portfolio/widgets?id=1&region=Kyushu&fit=40&codYears=0-5 |
| 发电量页面项目列表 | GET | /api/energy/projects?id=1&start=&end=&source=output&page=1&pageSize=10 |
| 发电量页面比较表格 | GET | /api/energy/tables?pid=1&start=2018-8-15&end=2018-9-15 |
| 项目列表-收藏 | GET | /api/project/favorite?pid=8|
| 项目列表-取消收藏 | GET | /api/project/unfavorite?pid=8 |
| 单项目滚屏幕明细 | GET | /api/project/Items?pid=105 |
| 单项目总览明细 | GET | /api/project/Infoes?pid=105 |
| 单项目相关文档 | GET | /api/project/documents?pid=105&type=monthlyreport&page=1&pagesize=10 |
| 项目搜索功能 | GET | /api/search/projects?keyword=金尺 |

## Work Log

- 2018/08/20
    - 请求未授权提示，移除
    - 自定义部署路径配置 `baseUrl`
    - 

- 2018/08/06
    - `axios` 请求模块封装
    - 开发环境跨域代理设置
    - `顶部导航` 与 `Widget面板` api联调对接成功
    - coolie 键 `.AspNet.ApplicationCookie`

- 2018/08/03
    - 事件日历组件开发与调试
    - 发现问题，eslint 规则无约束，代码不规范
    - `vue` 组件命名依然不够优雅

- 2018/08/02
    - 引入下拉加载组件
    - 考虑使用 `highStock` 触屏拉伸，时间段

- 2018/08/01
    - 完成 `单项目` 基本原型开发
    - 引入事件日历
    - 申请百度地图API `kK8ubS00D9vxxBTEaT8QD8QcIIjfXHZw`

- 2018/07/31
    - 完成 `多项目` 基本原型开发
    - 组件设计

- 2018/07/30
    - 完成 `dashboard`

- 2018/07/26
    - 完善登录流程，理解 `csrfToken` 安全提交校验
    - 打通前后端登录推出过程
    - 改变 `highchart` 主题颜色

- 2018/07/25
    - 完成图标体系 `Icon库` 选型，`Material Design Icon` 配套

- 2018/07/24
    - 完成登陆页面制作，背景放弃图片，选用 `24k` 大小的粒子动画 `particles.js` 
    - 引入安慰加载骨架屏组件 `vue-content-loader`
    - 使用状态管理 `Vuex` 存储用户登陆信息状态

- 2018/07/23
    - 完成嵌套路由设置，路由传参 `props`
    - 设置 `nav-tabs` 选中状态关联路由
    - 颜色，icon 的使用

- 2017/07/20
    - 基本页面组件划分搭建
    - 图表组件选用 `HighCharts`
    - 尝试对 `api` 封装, 开发环境下请求域名，生产环境下路由

- 2017/07/19
    - 使用 `egg` 构建 `Nodejs` 轻量服务器 `sv-egg`
    - 开发 `Restful API`，为前端工程 `sv-vue` 提供接口测试与 `Mock` 服务

- 2017/07/18
    - 新建前端工程 `sv-vue`, 一款日本新能源产业基金 Web App 应用
    - `Vuetify` 前端组件库选型测试

- 2017/07/16
    - 设计图定稿
    - 参考谷歌 `Material Design` 材料化设计方案
    - PhotoShop 产出设计稿（共计10页）





