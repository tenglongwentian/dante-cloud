# PostgreSQL 数据库创建脚本

```
// 创建用户 herodotus 密码是 herodotus。如果用户已经存在，则可以略过。
CREATE USER herodotus WITH PASSWORD 'herodotus';

// 创建数据库 dante_cloud, 并将用户 herodotus 分配给该数据库。
CREATE DATABASE dante_cloud OWNER herodotus;

// 将数据库 dante_cloud 的所有权限分配给 herodotus
GRANT ALL PRIVILEGES ON DATABASE dante_cloud TO herodotus;
```

```
// 创建用户 athena 密码是 athena。如果用户已经存在，则可以略过。
CREATE USER athena WITH PASSWORD 'athena';

// 创建数据库 dante_athena, 并将用户 athena 分配给该数据库。
CREATE DATABASE dante_athena OWNER athena;

// 将数据库 dante_athena 的所有权限分配给 athena。生产环境需根据实际需求进行调整。
GRANT ALL PRIVILEGES ON DATABASE dante_athena TO athena;
```