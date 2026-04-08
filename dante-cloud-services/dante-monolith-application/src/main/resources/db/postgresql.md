# 创建单体版 postgresql 数据库脚本

```
// 创建用户 athena 密码是 athena
CREATE USER athena WITH PASSWORD 'athena';

// 创建数据库 dante_athena, 并将用户 athena 分配给该数据
CREATE DATABASE dante_athena OWNER athena;

// 将数据库 dante_athena 的所有权限分配给 athena
GRANT ALL PRIVILEGES ON DATABASE dante_athena TO athena;
```