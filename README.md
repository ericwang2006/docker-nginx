# Docker image for nginx

Dockerfile 参考自官方的 [docker-nginx](https://github.com/nginxinc/docker-nginx/tree/master/mainline/alpine) 。  
使用的是 mainline alpine 版本构建的。  

基于 commit baa050df601b5e798431a9db458e16f53b1031f6 修改的此 Dockerfile 。

## 更新至 Nginx 1.17.9

## Tags

* [`latest`,`amd64-1.17.9` (Dockerfile)](https://github.com/Ran-snow/docker-nginx/blob/master/Dockerfile)
* ~~[`arm64v8-1.17.9` (Dockerfile)](https://github.com/Ran-snow/docker-nginx/blob/master/Dockerfile)~~

## 架构支持

`amd64`, ~~`arm64v8`~~

## 修改如下
1. ~~改用 [https://mirrors.aliyun.com](https://mirrors.aliyun.com) 镜像源，用以提升构建速度。~~
2. 使用openssl 1.1.1f, 并对openssl进行防篡改(gpg)校验。
3. 启用 Nginx 对 TLS1.3 http2 brotli 的支持。
4. 使用东八时区。
5. 预设“Modern configuration”型配置文件示例

## 构建

~~docker build -t rsnow/nginx:arm64v8-1.17.9 .~~

## 推送镜像

~~docker push rsnow/nginx:arm64v8-1.17.9~~

## 更多

[Nginx Docker Official Images](https://hub.docker.com/_/nginx)

此仓库始于 Github 私有仓库开启免费使用宣布日(Jan 8, 2019) ！