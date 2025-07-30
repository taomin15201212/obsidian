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


Windows就有点复杂了
1.安装gitbash git-scm.com
download/win
2.在 git bash 里运行bash -c"$(curl -fsSL https://raw.githubusercontent.comLLM-Red-Team/kimi-cc/refsheads/main/install.sh)"
3.npm install -g @anthropic-ai/claude-code --ignore-
scripts
4.npx win-claude-code@latest

文件.claude.json
"customApiKeyResponses": {  
  "approved": [  
    "sk-jOxpDsXFoNJJOyyq6mcELhTKDEaV8HwKWh6dGN1gRbg2zgGM",  
    "8HwKWh6dGN1gRbg2zgGM"  
  ],  
  "rejected": []  
},

文件.bashrc
#Claude Code environment variables
export ANTHROPIC_BASE_URL=https://api.moonshot.cn/anthropic/  
export ANTHROPIC_API_KEY=sk-jOxpDsXFoNJJOyyq6mcELhTKDEaV8HwKWh6dGN1gRbg2zgGM


文件C:\Users\TAOM\.claude\settings.json
{  
  "env": {  
    "HTTPS_PROXY": "http://127.0.0.1:7890",  
    "ANTHROPIC_BASE_URL": "https://api.moonshot.cn/anthropic/",  
    "ANTHROPIC_API_KEY": "sk-jOxpDsXFoNJJOyyq6mcELhTKDEaV8HwKWh6dGN1gRbg2zgGM"  
  },  
  "model": "opus"  
}


**Qwen3-Coder cc**
**[https://bailian.console.aliyun.com/](https://bailian.console.aliyun.com/)**
https://dashscope.aliyuncs.com/compatible-mode/v1
sk-904fd5652bc2456381983b6971faa61f
export OPENAI_MODEL="qwen3-coder-plus"


**[https://modelscope.cn/docs/model-service/API-Inference/intro](https://modelscope.cn/docs/model-service/API-Inference/intro)**
ModelScope offers 2,000 free
export OPENAI_API_KEY="your_api_key_here"
export OPENAI_BASE_URL="https://api-inference.modelscope.cn/v1"
export OPENAI_MODEL="Qwen/Qwen3-Coder-480B-A35B-Instruct"

**[https://modelstudio.console.alibabacloud.com/](https://modelstudio.console.alibabacloud.com/)**
export OPENAI_API_KEY="your_api_key_here"
export OPENAI_BASE_URL="https://dashscope-intl.aliyuncs.com/compatible-mode/v1"
export OPENAI_MODEL="qwen3-coder-plus"

**GLM-4.5**
open.bigmodel.cn/usercenter/proj-mgmt/apikeys
export ANTHROPIC_BASE_URL=https://open.bigmodel.cn/api/anthropic  
export ANTHROPIC_AUTH_TOKEN="3574a610f5bda1ec95fd14e4b4bdaa44.CverSrQxRm7LYqfx"





####使用three.js 生成一个由立方体组成的猫咪，然后猫咪在一个平面上原地奔跑的动画，所有代码放在一个html文件里面

创建一个 3D 粒子银河，包含旋转的星云和动态光照效果，ultrathink！

从零打造一款 广 告 投放智能仪表盘，支持实时刷新、自由配置与多图表联动展示。

- 核心数据用超大号中文粗体数字呈现，打造一眼可识别的视觉锚点
- 整体采用中英文混排风格：中文主导、英文作点缀，增强国际化科技氛围
- 页面布局强调视觉对比——重点内容用巨型数字、图形强化，次要信息则以细节形式缩小呈现
- 支持多种图表类型（柱状、折线、饼图等），实时变动的数据可用伪造数据模拟
- 数据视觉风格采用简洁线条构图，既突出信息，又保持界面清爽
- 利用高亮纯色 + 透明度渐变制造科技感，避免不同色之间渐变混色
- 页面滚动联动Apple 风格动效，每次向下滑动皆有过渡或内容浮现，基于 Framer Motion CDN 实现
- 全站构建技术栈为 HTML5 + Tailwind CSS 3.0+ + JavaScript，界面风格需保持统一性
- 所有图表组件（如 Chart.js 或 ECharts）必须融合整体视觉语言，不跳脱
- 图标统一引入自 Font Awesome / Material Icons，通过 CDN 方式加载使用