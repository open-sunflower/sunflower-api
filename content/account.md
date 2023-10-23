账户
==============

登录/注册
-----------

在登录之前或注册时，您需要首先通过 `/api/v1/email/deliver` 接口获取验证码。

**请求**

```json
{
  "email": "foobar@jinrifen.de",
  "code": "0333"
}
```

| 参数                             | 必填     |
| -------------------------------- | -------- |
| `email: string`                  | 是       |
| `code: string`                   | 是       |

**状态码**

- `200 OK`：登录/注册成功。

使用以下命令示例进行请求：

```bash
curl -X "POST" "http://localhost:3000/api/v1/account/sign_in" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "email": "foobar@jinrifen.de",
  "code": "8505"
}'
```

退出
-----------

在需要注销当前令牌时，请使用以下接口。

```bash
curl -X "DELETE" "http://localhost:3000/api/v1/account/sign_out" \
     -H 'Authorization: Bearer UPcnxonw75jViTt62DWfTTob'
```

**状态码**

- `204`：成功退出。