将以下命令中的 `username` `password` 替换为 `用户名` 和 `密码` ，也可以添加多个用户更多内容请搜索 `htpasswd`

```bash
$ docker run --rm \
    --entrypoint htpasswd \
    registry \
    -Bbn username password > auth/nginx.htpasswd
```

注意 Nginx 可能不能解密，请换为：

```bash
$ docker run --rm \
    --entrypoint htpasswd \
    registry \
    -mbn username password > auth/nginx.htpasswd
```
