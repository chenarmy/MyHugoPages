# 源码打包运行

## 安装
- 下载配置 java11 环境，这里不介绍
- 安装 yarn 和 npm 环境，对应 thingsboard 中 pom.xml 的版本
- 到 msa 下 web-ui 目录，到 msa 下 javascript 目录，以及 ui-ngx 目录下
- 执行，并生成 target 目录，里面有 node 等文件
```
yarn install
```
- 项目根目录，执行以下命令进行打包
```
mvn install -DskipTests
```
- 进入 application 目录中的 target，选择对应的部署方式进行部署

## 运行
- 配置数据库 url 地址，账号密码
- 链接 postgresql 数据
```
psql -h 127.0.0.1 -p 5432 -U postgres -d thingsboard362
```
- 导入 /home/user/ 目录下的 xxxx.sql 数据
```
\i /home/user/xxxx.sql
```
- 查看是否导入完整
```
\dt
\d device
SELECT * FROM device;
```
- \dt 列出所有表
- \d table_name 查看特定表的详细信息