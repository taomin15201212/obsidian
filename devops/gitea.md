https://go.dev/dl/
​**进入你的 WSL 终端，进入下载目录并解压**
cd ~
wget https://go.dev/dl/go1.21.0.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.21.0.linux-amd64.tar.gz

**将 Go 添加到 PATH**​编辑 `~/.bashrc` 或 `~/.zshrc`
sudo ~/.bashrc
export PATH=$PATH:/usr/local/go/bin

进入linux模式
source ~/.bashrc
```bash
go version
```


 前端开发环境已成功启动！

  已完成：

  1. 安装前端依赖 - 使用 npm install 成功安装了所有前端依赖包
  2. 构建前端资源 - Webpack 已编译并生成所有必要的JS和CSS文件
  3. 文件位置 - 所有构建文件位于 public/assets/ 目录下

  当前状态：

  - ✅ 前端依赖已安装 (node_modules/ 已创建)
  - ✅ Webpack 已构建所有资源文件
  - ✅ JavaScript 和 CSS 文件已生成到 public/assets/ 目录

  下一步：

  现在你可以：
  1. 启动后端服务器 - 运行 Gitea 应用以查看完整的网页界面
  2. 开始开发 - 修改 web_src/ 目录下的源文件，webpack 会自动重新编译
  3. 访问界面 - 通过浏览器访问 Gitea 应用

  常用命令：

  - 重新构建前端：npx webpack 或 npm run build
  - 开发模式（带热重载）：npx webpack --watch --progress
  - 启动后端：go run main.go web

  前端页面现在已经可以使用了！
