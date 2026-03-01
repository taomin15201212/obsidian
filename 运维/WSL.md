
打开启用或关闭windows功能
☑️Hyper-V
☑️适用于Linux的windows子系统

wsl install
wsl --list --online
>wsl.exe --install Ubuntu-24.04 或者 Microsoft Store中下载Ubuntu


wsl -l -v
wsl启动
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
command -v nvm

```sh
nvm install --lts
```

|                               |              |
| ----------------------------- | ------------ |
| `wsl --list`                  | 查看已安装的发行版    |
| `wsl --set-default-version 2` | 设置WSL 2为默认版本 |
| `wsl --shutdown`              | 终止所有WSL实例    |
| `wsl -u root`                 | 以root身份进入WSL |
