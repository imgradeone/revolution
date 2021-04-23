# DDLC 中文 Mod 分部 文档

文档编写中…… 1%

## 运行

这是 Node.js 项目，需要安装 Node.js，同时需要安装 yarn 的 1.x 版本。

### 下载依赖

```shell
$ yarn
```

### 运行项目并调试

```shell
$ yarn docs:dev
```

### 构建

```shell
$ yarn docs:build
```

## 远程构建

本 repo 使用 [jenkey2011/vuepress-deploy](jenkey2011/vuepress-deploy)。您只需要在 Settings 里面设置 Secrets - ACCESS_TOKEN，然后添加 GitHub 帐号的 Access Token 即可。