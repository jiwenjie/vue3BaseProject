## 简介

项目的基础版本出自于源于大佬的 vue3-composition-admin。

版本：

vue3 发布之后，性能增强，速度 vue2 的倍数，打包体积都在减小（treeshaking），composition api 增加了项目可读性。

项目目的：

- 学习 vue3+ts
- 保持 composition api 风格

### 目录结构

```
admin-tmpl
├─ .env.dev.build     # 开发环境
├─ .env.dev.serve     # 开发本地本地
├─ .env.prod.build    # 生产环境
├─ .env.prod.serve    # 生产环境本地
├─ .env.test.build    # 测试环境
├─ .env.test.serve    # 测试环境本地
├─ .eslintrc.js       # eslint
├─ README.md
├─ dist               # 打包dist
├─ mock               # mock服务
├─ public             # 静态资源
├─ src                # 源码
│  ├─ @types          # ts 声明
│  ├─ apis            # 接口请求
│  ├─ assets          # webpack打包的资源
│  ├─ components      # 公共组件
│  ├─ config          # 全部配置
│  ├─ constant        # 常量
│  ├─ directives      # 全局指令
│  ├─ layout          # 全局Layout
│  ├─ locales         # 国际化
│  ├─ model           # 全部model存放
│  ├─ plugins         # 插件
│  ├─ router          # 路由
│  ├─ store           # 全局store管理
│  ├─ styles          # 全局样式
│  ├─ utils           # 全局公共方法
│  └─ views           # 所有业务页面
├─ tsconfig.json      # ts 编译配置
└─ vue.config.js      # vue-cli 配置

```

## HighLight

项目均已最新技术实现，Vue3 配套升级全家桶和涉及的插件组件等

项目采用技术:

- vue3 + composition api
- typescript3.9
- sass (dart sass)
- [echats5](https://github.com/apache/echarts)

vue next 系列:

- [element-plus](https://github.com/element-plus/element-plus)
- [vue-router-next](https://github.com/vuejs/vue-router-next)
- [vuex-4.0](https://github.com/vuejs/vuex)
- [vue-i18n-next](https://github.com/intlify/vue-i18n-next)

## Setup

项目主要是前端和 mock server（node）

### 前后端都启动

```shell
  yarn
  yarn start
```

### 单独启动 Mock

后台模拟服务器和其他版本不同，采用 koa2+Faker 进行模拟。

- [Koa2](https://github.com/koajs/koa)
- [Faker](https://github.com/Marak/faker.js)

启动 mock server:

```shell
    yarn mock
```

### 单独启动 vue admin

```shell
    yarn  serve:dev
```

多环境命令查看 package.json script:

```shell
    "serve:dev": "cross-env NODE_ENV=development dotenv -e .env.dev.serve vue-cli-service serve",
    "build:dev": "cross-env NODE_ENV=production  dotenv -e .env.dev.build vue-cli-service build",
    "serve:test": "cross-env NODE_ENV=development dotenv -e .env.test.serve vue-cli-service serve",
    "build:test": "cross-env NODE_ENV=production  dotenv -e .env.test.build vue-cli-service build",
    "serve:prod": "cross-env NODE_ENV=development dotenv -e .env.prod.serve vue-cli-service serve",
    "build:prod": "cross-env NODE_ENV=production  dotenv -e .env.prod.build vue-cli-service build",
```

### eslint

```shell
    yarn  lint
```

提交自动检测：

```json
 "gitHooks": {
    "pre-commit": "lint-staged"
  },
  "lint-staged": {
    "*.{js,jsx,vue,ts,tsx}": [
      "vue-cli-service lint",
      "git add"
    ]
  }
```

## Browsers support

Modern browsers and Internet Explorer 10+.

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)</br>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)</br>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)</br>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](https://godban.github.io/browsers-support-badges/)</br>Safari |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| IE10, IE11, Edge                                                                                                                                                                                                 | last 2 versions                                                                                                                                                                                                    | last 2 versions                                                                                                                                                                                                | last 2 versions                                                                                                                                                                                                |

## License

[MIT](https://github.com/rcyj-FED/vue3-composition-admin/blob/main/LICENSE)

Copyright (c) 2021-present
