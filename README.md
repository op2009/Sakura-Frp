# Sakura-Frp 服务端 一键安装卸载脚本
## 项目简介
- GitHub [ZeroDream-CN/SakuraFrp](https://github.com/ZeroDream-CN/SakuraFrp) 原版 SakuraFrp 内网穿透服务端 SakuraFrp 的一键安装卸载脚本支持 Linux 服务器等多种环境安装部署.
> *support for X86 and ARM* 




## 使用说明
由于 Sakura-Frp 服务端需要配置参数,本脚本为原版 frps.ini ,安装完毕后请自行编辑 frps.ini 配置端口,密码等相关参数并重启服务.同时你也可以 fork 本仓库后自行修改 frps.ini ,在进行一键安装也非常方便.后期也可自行配置 frps.ini 和调整 Sakura-Frp 的版本.

### 一键脚本(先运行脚本,在自行修改 frps.ini 文件.)
安装
```shell
wget https://raw.githubusercontent.com/op2009/Sakura-Frp/master/Sakura-Frp_linux_install.sh && chmod +x Sakura-Frp_linux_install.sh && ./Sakura-Frp_linux_install.sh
```

使用
```shell
vi /usr/local/frp/frps.ini
# 修改 frps.ini 配置
sudo systemctl restart frps
# 重启 frps 服务即可生效
```

卸载
```shell
wget https://raw.githubusercontent.com/op2009/Sakura-Frp/master/Sakura-Frp_linux_uninstall.sh && chmod +x Sakura-Frp_linux_uninstall.sh && ./Sakura-Frp_linux_uninstall.sh

```

### 自定义一键脚本(先 fork 本仓库,在自行修改 frps.ini 文件后运行脚本.)
> 同时支持 github 和 gitee 平台 fork

- 首先 fork 本仓库
- 配置 frps.ini
- 修改 frps_linux_install.sh 脚本
- 修改脚本链接并运行

#### 修改 Sakura-Frp_linux_install.sh 脚本
`FRP_VERSION="0.28.2"` 可根据原版项目更新自行修改为最新版本  
`REPO="op2009/frps"` 由于 **fork** 到你自己的仓库,需修改`op2009`为你的 GitHub 账号ID.

#### 运行一键脚本
修改以下脚本链接中的`op2009`为你的 GitHub ,运行即可.
```shell
wget https://raw.githubusercontent.com/op2009/Sakura-Frp/master/Sakura-Frp_linux_install.sh && chmod +x Sakura-Frp_linux_install.sh && ./Sakura-Frp_linux_install.sh
```
#### 卸载脚本
Sakura-Frp_linux_uninstall.sh 卸载脚本为通用脚本,可直接运行,也可同上方式修改链接后运行.
```shell
wget https://raw.githubusercontent.com/op2009/Sakura-Frp/master/Sakura-Frp_linux_uninstall.sh && chmod +x Sakura-Frp_linux_uninstall.sh && ./Sakura-Frp_linux_uninstall.sh
```

### Sakura-Frp相关命令
```shell
sudo systemctl start frps
# 启动服务 
sudo systemctl enable frps
# 开机自启
sudo systemctl status frps
# 状态查询
sudo systemctl restart frps
# 重启服务
sudo systemctl stop frps
# 停止服务
```

## 版本更新
- latest 为最新版
- Tags 为历史版本
- 原版frp项目 [fatedier/frp](https://github.com/fatedier/frp)
