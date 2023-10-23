认证
==============

要进行身份验证，按照以下步骤操作：

1. 登录后，获取一个名为 `access_token` 的令牌。

2. 将获取到的 `access_token` 添加到请求头部，使用格式 `'Authorization: Bearer {access_token}'`。示例如下：

```bash
curl -X "DELETE" "http://localhost:3000/api/v1/account/sign_out" \
     -H 'Authorization: Bearer UPcnxonw75jViTt62DWfTTob'
```

**状态码**
-  `200 OK`：表示令牌合法，操作成功。
-  `401 Unauthorized`：表示令牌非法，操作未授权。