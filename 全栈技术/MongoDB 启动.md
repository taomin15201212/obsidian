进入根目录 shift + command +G 输入 /usr/local 

配置环境变量，打开终端，输入“open -e .bash_profile”

export PATH=${PATH}:/usr/local/MongoDB/bin 加入保存

source .bash_profile 生效

  

mongod -version

sudo mkdir -p /data/db

sudo mongod --dbpath=/data/db

mongod 启动

输入localhost:27017

mongo

【sudo chown keen /data/db】 >whoami

  

$ cd /usr/local/mongodb/bin $ ./mongo

  

  

  

[https://www.jianshu.com/p/7241f7c83f4a](https://www.jianshu.com/p/7241f7c83f4a)

[https://www.runoob.com/mongodb/mongodb-osx-install.html](https://www.runoob.com/mongodb/mongodb-osx-install.html)