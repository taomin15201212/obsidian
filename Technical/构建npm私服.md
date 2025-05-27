### 构建npm私服

npm install verdaccio -g

  
#创建账号  
npm adduser --registry http://localhost:4873/  
# 账号 密码 邮箱

  
# 发布npm  
npm publish --registry [http://localhost:4873/](http://localhost:4873/)  
  

#指定开启端口 默认 4873  
verdaccio --listen 9999  
  

# 指定安装源  
npm install --registry http://localhost:4873  
  

# 从本地仓库删除包  
npm unpublish <package-name> --registry http://localhost:4873