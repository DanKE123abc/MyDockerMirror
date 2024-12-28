# DanKe Docker Mirror

镜像中心网址：
`hub.docker.danke666.top`
`docker.dkdk.us.kg`
`docker.dkdk.eu.org`

使用Github Action和Cloudflare等服务建立的Docker镜像服务，旨在为开发者提供及时，无审查，国内可用的开源容器镜像中心及下载方式

## 安装Docker

```shell
sudo curl -fsSL https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/linux.sh| bash -s docker --mirror Aliyun
```

**启动docker**

```shell
sudo service docker start
```

### Docker Desktop下载

![DockerDesktop](assets/dockerdesktop.svg)

| 可用平台                                                     |
| ------------------------------------------------------------ |
| [linux debian](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_linux_debian_x84_64.dmg) |
| [linux fedora](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_linux_fedora_x84_64.dmg) |
| [mac arm64](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_mac_arm64.dmg) |
| [mac x84_64](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_mac_x84_64.dmg) |
| [windows x86_64](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_windows_x86_64.exe) |

## 配置镜像

### Linux

运行以下命令配置镜像：

```
#!/bin/sh
cat <<-EOF > /etc/docker/daemon.json 
{
  "registry-mirrors": [
  	"https://hub.docker.danke666.top",
  	"https://docker.dkdk.us.kg",
  	"https://docker.dkdk.eu.org"
  	]
}
EOF
systemctl daemon-reload
systemctl restart docker
```

适用于Ubuntu 14.04、Debian、CentOS 6、CentOS 7、Fedora、Arch Linux、openSUSE Leap 42.1等系统。

### macOS（Docker For Mac）

通过以下步骤配置镜像：

1. 点击桌面顶栏的docker图标，选择Preferences。

2. 在 Daemon 标签下的 Registry mirrors 列表中加入以下镜像地址：

https://hub.docker.danke666.top
https://docker.dkdk.us.kg
https://docker.dkdk.eu.org

3. 点击Apply & Restart按钮使设置生效。

### Windows（Docker For Windows）

通过以下步骤配置镜像：

1. 在桌面右下角状态栏中右键docker图标，修改在Docker Daemon标签页中的json。
2. 将以下地址加入"registry-mirrors"的数组里

https://hub.docker.danke666.top
https://docker.dkdk.us.kg
https://docker.dkdk.eu.org

3. 点击Apply，重新生成Docker环境以使配置生效。

## 镜像来源

安装包使用Github Action每日同步官方安装包，容器镜像中心由cloudflare持续解析

*由Github提供下载方式，无法访问请使用加速器*
