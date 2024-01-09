# 源码打包运行

- 下载配置java11环境，这里不介绍
- 安装yarn和npm环境，对应thingsboard中pom.xml的版本
- 到msa下web-ui目录，到msa下javascript目录，以及ui-ngx目录下
- 执行,并生成target目录，里面有node等文件
```
yarn install
```
- 项目根目录，执行以下命令进行打包
```
mvn install -DskipTests
```
- 进入application目录中的target，选择对应的部署方式进行部署

