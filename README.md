# reverse-proxy-webdav-server
反向代理webdav服务器,并提供静态文件服务

基于 caddy 和 webdav-cli

https://github.com/caddyserver/caddy

https://www.npmjs.com/package/@masx200/webdav-cli


对于读取文件,请求方法为`HEAD`或者`GET`,不需要用户身份验证,由`caddy`直接提供静态文件服务.

对于写入文件,请求方法不为`HEAD`或者`GET`,需要用户身份验证,由`caddy`反向代理`webdav`服务提供.
