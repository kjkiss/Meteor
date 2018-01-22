# Meteor 部署的几种方式

## Windows 部署方式
### Mongodb 设置
启动Mongodb服务器<br>
```c:\mongod```<br>

shell登陆Mongodb服务器<br>
```c:\mongo```<br>

添加管理用户及权限，Meteor使用此帐号连接Mongodb服务器<br>
```> db.createUser({user:’admin’,pwd:’password’,roles:[‘readWrite’,’dbAdmin’]})```

重启Mongodb服务器，指定数据库和日志存放位置、端口号及认证选项<br>
```c:\mongod --dbpath=c:\data\db --logpath=c:\data\logs\mongodb.log --port=27017 --auth```

### 环境变量设置

设置环境变量（此电脑-属性-高级系统设置-环境变量）（win10）

变量 | 值
--|--
MONGO_URL | mongodb://admin:password@localhost:27017/databasename
ROOT_URL | http://localhost
PORT | 80

### Meteor 部署

进入WEB项目目录<br>
```c:\cd myweb```

部署到上级目录output<br>
```meteor build –server-only --directory ../output```

进入到相应目录<br>
```c:\cd output/bundle/programs/server```

安装依赖包，可以不联网<br>
```npm install```

进入相应目录<br>
```cd output/bundle```

启动服务<br>
```node main.js```

## Ubuntu 部署方式

## Docker 部署方式
