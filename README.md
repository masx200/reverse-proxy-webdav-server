# reverse-proxy-webdav-server

反向代理`webdav`服务器,并由`caddy`提供静态文件服务

基于 `caddy` 和 `webdav-cli` 和 `nodejs`

https://github.com/caddyserver/caddy

https://www.npmjs.com/package/@masx200/webdav-cli

对于读取文件,请求方法为`HEAD`或者`GET`,不需要用户身份验证,由`caddy`直接提供静态文件服务.

对于写入文件,请求方法不为`HEAD`或者`GET`,需要用户身份验证,由`caddy`反向代理`webdav`服务提供.

# 安装

下载并安装 `caddy` 和 `nodejs` 和`yarn`和 `webdav-cli`

https://nodejs.org/en/

https://yarnpkg.com/

```
npx yarn global add yarn
```

```shell
yarn global add @masx200/webdav-cli
```

# 启动

运行`webdav-server`和`caddy-reverse-proxy`目录下的`start.cmd`

启动 多个 `webdav-cli` 进程 提供服务

http://localhost:1901

http://localhost:1902

http://localhost:1903

http://localhost:1904

http://localhost:1905

然后访问 由`caddy server` 提供的网关

http://localhost:1900
