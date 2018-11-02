# Vue 电商后台管理系统后台 API 接口服务器

## 技术栈

- Node.js
- Express
- MySQL

## 项目整体文件说明

- `config` 配置文件目录
  - `default.json` 默认配置文件（其中包含数据库配置，jwt配置）
- `dao` 数据访问层，存放对数据库的增删改查操作
  - `DAO.js` 提供的公共访问数据库的方法
- `models` 存放具体数据库 ORM 模型文件
- `docs` 包含 sql 文件和 api 接口文档
  - `shop.sql` 本地数据库的 sql 文件
  - `接口api文档.md` 关于服务器的所有接口文档
- `modules` 当前项目模块
  - `authorization.js` API权限验证模块
  - `database.js` 数据库模块（数据库加载基于 nodejs-orm2 库加载）
  - `passport.js` 基于 passport 模块的登录搭建
  - `resextra.js` API 统一返回结果接口
- `node_modules` 项目依赖的第三方模块
- `routes` 统一路由
  - `api` 提供 api 接口
  - `mapp` 提供移动APP界面
  - `mweb` 提供移动web站点
- `services` 服务层，业务逻辑代码在这一层编写，通过不同的接口获取的数据转换成统一的前端所需要的数据
- `app.js` 主项目入口文件
- `package.json` 项目配置文件

## Develop

1. 克隆仓库地址到本地并下载依赖
```shell
$ git clone https://github.com/WDBBdpd223322/vue_oa_api.git
$ cd vue_oa_api/
$ npm install
```

2. 数据库导入
  - 找到 `vue_oa_api/docs/shop.sql` 文件
  - 将此文件导入本地 mysql 数据库内

3. 修改服务器配置文件
  - 打开 `vue_oa_api/config/default.json` 文件
  - 修改 `database` / `user` / `password`
  - 保证和本地数据库信息一致

4. 开启服务器
```shell
$ cd vue_oa_api/
$ npm start
```

