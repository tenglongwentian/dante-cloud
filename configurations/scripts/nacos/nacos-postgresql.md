# PostgreSQL 创建 nacos 数据库 脚本 

```
// 创建用户 nacos 密码是 nacos。如果用户已经存在，则可以略过。
CREATE USER nacos WITH PASSWORD 'nacos';

// 创建数据库 nacos, 并将用户 nacos 分配给该数据库。
CREATE DATABASE nacos OWNER nacos;

// 将数据库 nacos 的所有权限分配给 nacos。生产环境需根据实际需求进行调整。
GRANT ALL PRIVILEGES ON DATABASE nacos TO nacos;
```