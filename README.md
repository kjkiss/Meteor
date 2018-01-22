# Meteor 部署的几种方式

## Windows 部署方式
### Mongodb 设置
启动Mongodb服务器<br>
```c:\mongod```<br>

shell登陆Mongodb服务器<br>
```c:\mongo```<br>

添加管理用户及权限，Meteor使用此帐号连接Mongodb服务器<br>
```> db.createUser({user:’admin’,pwd:’password’,roles:[‘readWrite’,’dbAdmin’]})```<br>

重启Mongodb服务器，指定数据库和日志存放位置、端口号及认证选项<br>
```c:\mongod --dbpath=c:\data\db --logpath=c:\data\logs\mongodb.log --port=27017 --auth<br>

### 环境变量设置
### Meteor 部署

## Ubuntu 部署方式

## Docker 部署方式
