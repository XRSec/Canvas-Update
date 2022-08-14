# [Immunity Canvas Docker Build](https://xrsec.vercel.app/Immunity%20Canvas%20Docker%20Build.html)

![version](https://img.shields.io/badge/Version-7.2-da282a)  [![Docker Automated Build](https://img.shields.io/docker/automated/xrsec/canvas?label=Build&logo=docker&style=flat-square)](https://hub.docker.com/r/xrsec/canvas) [![Canvas Update](https://github.com/XRSec/Canvas-Update/actions/workflows/Canvas_Docker_Build.yml/badge.svg)](https://github.com/XRSec/Canvas-Update/actions/workflows/Canvas_Docker_Build.yml)

> 前言：docker 容器来自 [gotoeasy](https://github.com/gotoeasy/docker-ubuntu-desktop) 的docker-ubuntu:18.04-vnc版 进行的二开
> 感谢 飞蓬 转载提供的  [Immunity Canvas压缩包](https://pan.baidu.com/s/1hiAjzrzQYExtgK5clRUEbw) 2emu / hacker1961
> 感谢 [NorahC_IV](https://www.cnblogs.com/charon1937/) [潇湘信安](https://mp.weixin.qq.com/s/Ri_MCXTKSsHqOKEGOse1Cw) [WgpSec](https://wiki.wgpsec.org/) 提供的技术支持 (排名不分先后)

## RUN 🚀

For details about screen parameters, see：[docker-ubuntu-desktop](https://github.com/gotoeasy/docker-ubuntu-desktop)

### Inter x86

```shell
docker run -d \
-p 55900:5900 \
-p 55022:22 \
-p 4445:4445 \
-p 4446:4446 \
-e PASSWD=123456 \
--name canvas \
--hostname canvas \
xrsec/canvas:latest
```

```ini
docker run -d \
-p 55900:5900 \
-p 55022:22 \
-p 4445:4445 \
-p 4446:4446 \
-e PASSWD=123456 \
--name canvas \
--hostname canvas \
xrsec/canvas:latest
```

## Start Canvas After VNC

```bash
/root/Desktop/canvas
```

## IP database

Not collected at present, need to download separately

## Bugs ❌

- 可能会遇见奇怪的bugs 重新下载在解压即可

- docker 没有 `root-->/canvas/canvas/installer/linux_installer.sh`

  ```shell
  AS_USER="sudo -u $SUDO_USER" >> AS_USER=""
  AS_USER="sudo" >> AS_USER=""
  $AS_USER "PATH=$VIRTUAL_ENV/bin:$PATH" libtoolize --force >>
  PATH="$VIRTUAL_ENV/bin:$PATH" libtoolize --force
  ```

- `pygame==1.9.2`
- 注意端口开放问题

- Email : [Jalapeno1868@outlook.com](mailto:Jalapeno1868@outlook.com?Subject=%5BImmunity Canvas搭建问题%5D&amp;)

> XRSec has the right to modify and interpret this article. If you want to reprint or disseminate this article, you must ensure the integrity of this article, including all contents such as copyright notice. Without the permission of the author, the content of this article shall not be modified or increased or decreased arbitrarily, and it shall not be used for commercial purposes in any way
