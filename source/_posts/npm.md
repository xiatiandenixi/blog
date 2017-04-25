---
title: 发布自己的npm包到全局仓库
date: 2017-04-25
tags: 随笔
---

# 发布自己的npm包到全局仓库



### 去npm官网注册一个账号

 传送门： https://www.npmjs.com/signup

### 本地登录账号

```python
$ npm login

Username: xxxxxx
Password:
Email: (this IS public) xxx@gmail.com
Logged in as falm on https://registry.npmjs.org/.

```
恭喜，登录成功。

### 初始化

```python

$ mkdir npm-project && cd npm-project
$ npm init

```
输入完npm init之后，跟着填写项目信息就可以了。
```javascript
name: npm-project  # 填写包名
version: (1.0.0)                       # 版本号
description: a new npm-project # 描述
entry point: (index.js)      #  入口文件名
test command:
git repository: https://github.com/xiatiandenixi/npm-project.git  # git仓库地址
keywords: keywords    # 关键字
author: xiatiandenixi  # 作者
license: (ISC) MIT   # 许可证
```

生成的package.json
```javascript
# package.json
{
  "name": "npm-project",
  "version": "1.0.0",
  "description": "a new npm-project",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/xiatiandenixi/npm-project.git"
  },
  "keywords": [
    "keywords"
  ],
  "author": "xiatiandenixi",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/xiatiandenixi/npm-project/issues"
  },
  "homepage": "https://github.com/xiatiandenixi/npm-project#readme"
}
```
接下来就是愉快的码代码时间....


### 发布

```python
npm publish
```