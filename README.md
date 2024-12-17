# Hapydev-api 是Hapydev的后端API服务

通过Hapydev-api，您可以对Hapydev中产生的数据进行集中存储，考虑到服务扩展性，我们支持将第三方功能通过webapi的方式集成到项目中。

### 安装方式

- 第1种:通过git克隆方式进行安装

```bash
git clone git@github.com:hapydev-team/hapydev-server.git
cd hapydev-server
```

修改.env文件，手动配置好Mysql，redis,minio,短信api，邮件api等环境变量后，继续运行下方脚本

```bash
 npm install
 npm run gen
 npm start
```

- 第2种:通过Docker方式进行安装

```bash
docker pull hapydev/hapydev-api
docker run -d -p 6002:6002  hapydev/hapydev-api
```

安装成功后，http://ip:6002/api/v1.0 即可对外提供服务

### 环境变量

| 变量名称            | 变量描述                   | 示例参数                                   |
| ------------------- | -------------------------- | ------------------------------------------ |
| DATABASE_URL        | MySQL数据库地址            | "mysql://root:pwd@localhost:3306/hapydev"  |
| REDIS_URL           | redis服务地址              | "redis://localhost:6379/0"                 |
| MINIO_ENDPOINT      | minio服务地址              | "localhost"                                |
| MINIO_ACCESS_KEY    | minio密钥                  | "1BLRKoXioW4MUliLtRmm"                     |
| MINIO_SECRET_KEY    | minio 密钥密码             | "vmWWcN6YpIWPYAY9n31xPvn7TyNsOuAMUN2f0Kca" |
| MINIO_PORT          | minio 端口号               | "9000"                                     |
| JWT_ACCESS_SECRET   | Jwt token 密钥             | "zf7vWzZjmbvRC7DmKx5s326DpdV23g50"         |
| JWT_ACCESS_EXPIRES  | jwt token 过期时间         | "30m"                                      |
| JWT_REFRESH_SECRET  | jwt refresh token 密钥     | "xasdnkd&ZeMsOisLxsd3e0HgsTsxshjd"         |
| JWT_REFRESH_EXPIRES | jwt refresh token过期时间  | "30d"                                      |
| APP_BASE_URL        | Hapydev工具Web方式访问地址 | 'https://app.hapydev.com'                  |
| EMAIL_SERVICE_API   | 邮件服务地址               | 'http://localhost:7001/email/send'         |
| SMS_SERVICE_API     | 短信服务地址               | 'http://localhost:7001/sms/send'           |

## Bug 和需求反馈

如果您想要反馈 Bug、提供产品意见，或者希望和 Hapydev 团队近距离交流，欢迎加入以下渠道。

- 扫客服小二微信加群：（备注：hapydev技术交流）

<p align="left"><img src="https://github.com/hapydev-team/hapydev/raw/main/src/assets/products/contact-wechat.png" width="200"  /></p>
