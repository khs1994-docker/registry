将以下命令中的 `username` `password` 替换为 `用户名` 和 `密码` ，也可以添加多个用户更多内容请搜索 `htpasswd`

```bash
$ docker run --rm \
    --entrypoint htpasswd \
    registry \
    # -mbn username password > auth/nginx.htpasswd \
    -Bbn username password > auth/nginx.htpasswd
```
