环境
### Ubuntu/Debian 用户
# 安装 Node.js LTS 版本
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo bash -
sudo apt-get install -y nodejs
sudo apt-get install npm
# 验证安装
node --version

### macOS 用户
# 安装 Xcode 命令行工具（如果尚未安装）
sudo xcode-select --install

# 安装 Homebrew（如果尚未安装）
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

### **使用 `nvm` 管理 Node.js**
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc  # 或重新打开终端
nvm install --lts
npm install -g @anthropic-ai/claude-code

# 安装 Node.js

brew uninstall node
brew install node

brew reinstall node
# 验证安装
node --version

#### **使用 `nvm`**
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc  # 或重新打开终端
nvm install --lts
node --version
npm --version

node --version  # 应返回版本号（如 v20.x.x）
npm --version   # 应返回版本号（如 10.x.x）

安装 Claude Code
手动输入npm install -g @anthropic-ai/claude-code
npm install -g "@anthropic-ai/claude-code"


cd your-project-folder
手动输入
export ANTHROPIC_AUTH_TOKEN=sk-BCtcWj5rSA7SeVgw4MDvljrmUK3b1keSDJV7ks37bR5x0CIq
export ANTHROPIC_BASE_URL= https://anyrouter.top


为避免每次重复输入，可将环境变量写入 bash_profile 和 bashrc：
```bash
echo -e '\n export ANTHROPIC_AUTH_TOKEN=sk-FK3pXLjylALnBxjRraBljfIN5piDubYxysbtPtDMVdL52GVO' >> ~/.bash_profile
echo -e '\n export ANTHROPIC_BASE_URL=https://anyrouter.top' >> ~/.bash_profile
echo -e '\n export ANTHROPIC_AUTH_TOKEN=sk-FK3pXLjylALnBxjRraBljfIN5piDubYxysbtPtDMVdL52GVO' >> ~/.bashrc
echo -e '\n export ANTHROPIC_BASE_URL=https://anyrouter.top' >> ~/.bashrc
echo -e '\n export ANTHROPIC_AUTH_TOKEN=sk-FK3pXLjylALnBxjRraBljfIN5piDubYxysbtPtDMVdL52GVO' >> ~/.zshrc
echo -e '\n export ANTHROPIC_BASE_URL=https://anyrouter.top' >> ~/.zshrc
```


echo -e '\n export ANTHROPIC_AUTH_TOKEN=sk-...' >> ~/.bash_profile`
echo -e '\n export ANTHROPIC_BASE_URL=https://anyrouter.top' >> ~/.bash_profile`
echo -e '\n export ANTHROPIC_AUTH_TOKEN=sk-...' >> ~/.bashrc`
echo -e '\n export ANTHROPIC_BASE_URL=https://anyrouter.top' >> ~/.bashrc
**验证配置参**
echo $ANTHROPIC_AUTH_TOKEN
echo $ANTHROPIC_BASE_URL


### **在 WSL 中使用该 IP**
ipconfig | findstr "IPv4" 找到类似 `192.168.x.x` 的 IP
```bash
export HOST_IP=192.168.x.x  # 替换为你的 Windows IP
export http_proxy="http://$HOST_IP:7890"
export https_proxy="http://$HOST_IP:7890"
```
curl -v https://www.google.com



Kimi K2
```bash
curl -fsSL https://raw.githubusercontent.com/LLM-Red-Team/kimi-cc/main/install.sh -o install.sh

bash install.sh
```
windows下
```powershell
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/LLM-Red-Team/kimi-cc/main/install.sh" -OutFile "install.ps1"
./install.sh
```


## **使用 Git Bash**
```bash
# 下载脚本
curl -fsSL https://raw.githubusercontent.com/LLM-Red-Team/kimi-cc/main/install.sh -o install.sh

# 赋予执行权限（如果需要）
chmod +x install.sh

# 运行
./install.sh
```