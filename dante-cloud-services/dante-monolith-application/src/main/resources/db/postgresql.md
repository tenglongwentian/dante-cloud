# 创建单体版 PostgreSQL 数据库脚本

```
// 创建用户 athena 密码是 athena。如果用户已经存在，则可以略过。
CREATE USER athena WITH PASSWORD 'athena';

// 创建数据库 dante_athena, 并将用户 athena 分配给该数据库
CREATE DATABASE dante_athena OWNER athena;

// 将数据库 dante_athena 的所有权限分配给 athena。生产环境需根据实际需求进行调整。
GRANT ALL PRIVILEGES ON DATABASE dante_athena TO athena;
```