# DanKe Docker Mirror

镜像中心网址：`hub.docker.danke666.top`

使用Github Action和Cloudflare等服务建立的Docker镜像服务，旨在为开发者提供及时，无审查，国内可用的开源容器镜像中心及下载方式



## 镜像来源

安装包使用Github Action每日同步官方安装包，容器镜像中心由cloudflare持续解析



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

| 可用平台                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------|
| [linux debian](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_linux_debian_x84_64.dmg) |
| [linux fedora](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_linux_fedora_x84_64.dmg) |
| [mac arm64](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_mac_arm64.dmg)              |
| [mac x84_64](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_mac_x84_64.dmg)            |
| [windows x86_64](https://github.com/DanKE123abc/MyDockerMirror/releases/download/latest/docker_desktop_installer_windows_x86_64.exe)    |

*由Github提供下载方式，无法访问请使用加速器*

