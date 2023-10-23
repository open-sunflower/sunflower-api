邮件
==============

获取验证码
-----------

您可以使用以下接口在登录前获取验证码，无需登录。

**请求**

```json
{
  "email": "foobar@jinrifen.de",
  "scene": "login"
}
```

| 参数                             | 必填     |
| -------------------------------- | -------- |
| `email: string`                  | 是       |
| `scene: string`                  | 是       |

**状态码**

- `200 OK`：成功获取验证码。

使用以下命令示例进行请求：

```bash
curl -X "POST" "http://localhost:3000/api/v1/email/deliver" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "email": "foobar@jinrifen.de",
  "scene": "login"
}'
```

**响应**
```json
{"message": "发送成功"}
```
