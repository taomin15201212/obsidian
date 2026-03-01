1 、`uv` 专注于提供快速的 Python 包管理  
https://docs.astral.sh/uv/guides/install-python/#getting-started

pip install uv
uv python list
uv python install 3.12

//创建并激活虚拟环境：
uv venv
// uv venv --python=/path/to/python3.12.9 myenv 
.venv/Scripts/activate     # Windows系统使用这个命令
uv pip install -r requirements.txt
python  main.py
  

2 、打开应用 anaconda Prompt, `conda` 提供更全面的包和环境管理，包括对非 Python 包的支持
conda env list
conda env remove -n py39

创建并激活虚拟环境
conda create -n py310 python=3.10
conda create -n ComfyUI python=3.9 -y
conda activate ComfyUI

  
3、python -m venv .venv
source .venv/bin/activate # Unix/macOS
.venv\Scripts\activate # Windows
pip install -r requirements.txt


4、pyenv
- 使用 `pyenv versions` 列出已安装的 Python 版本。
    
- 使用 `pyenv install --list` 列出所有可用的 Python 版本。
    
- 使用 `pyenv install <version>` 安装指定版本的 Python。
    
- 使用 `pyenv global <version>` 或 `pyenv local <version>` 切换 Python 版本。