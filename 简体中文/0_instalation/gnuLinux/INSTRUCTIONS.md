# 在 GNU/Linux 上安装

[视频教程(需要翻墙)](https://www.youtube.com/watch?v=z_WJaHYH66M)。


## 在终端上安装
打开终端并运行以下命令：

### 安装 LaTeX
Debian发行版：
```sh
$ sudo apt-get install texlive-full
```
Arch发行版：
```sh
$ sudo pacman -S texlive-most
```
Fedora发行版：
```sh
# yum -y install texlive-collection-latexextra
```

### 安装 python3.7
Debian发行版：
```sh
$ sudo apt-get install python3.7-minimal
```

Arch发行版：总是在更新。

Fedora发行版：
```sh
# yum install gcc openssl-devel bzip2-devel libffi-devel
# cd /usr/src
# wget https://www.python.org/ftp/python/3.7.3/Python-3.7.3.tgz
# tar xzf Python-3.7.3.tgz
# cd Python-3.7.3
# ./configure --enable-optimizations
# make altinstall
# rm /usr/src/Python-3.7.3.tgz
```

### 安装 pip
全部发行版:
```sh
$ mkdir pip
$ cd pip
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ python3.7 get-pip.py
```

### 安装 ffmpeg
Debian：
```sh
$ sudo apt-get install ffmpeg
```
Arch-Linux：
```sh
$ sudo pacman -S ffmpeg
```
Fedora：
```sh
$ sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
$ sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
$ sudo dnf install ffmpeg ffmpeg-devel
```


### 安装 sox
Debian：
```sh
$ sudo apt-get install sox
```
Arch-Linux (通过 AUR)：
```sh
$ aurman -S sox
```
Fedora：
在 https://pkgs.org/download/sox 下载。

### 安装 pycairo 依赖 (Debian 发行版)
只用于Debian发行版:
```sh
$ sudo apt-get install libcairo2-dev libjpeg-dev libgif-dev python3-dev libffi-dev
```

### 安装 pyreadline， pydub
全部发行版：
```sh
$ python3.7 -m pip install pyreadline
$ python3.7 -m pip install pydub
```

### 下载 [最新版](https://github.com/3b1b/manim) 或 [20190203版](https://github.com/3b1b/manim/tree/3b088b12843b7a4459fe71eba96b70edafb7aa78)的Manim。

<p align="center"><img src ="/English/0_instalation/gnuLinux/gifs/manimDescarga.png" /></p>

解压到一个没有空格(和中文)的路径下。

## 安装 requirements.txt 内的需求
在终端中打开 manim-master 目录并运行：

```sh
~/manim-master$
```

运行：

```sh
$ python3.7 -m pip install -r requirements.txt
```

# 运行 Manim

在 manim-master 目录下运行：

```sh
$ python3.7 -m manim example_scenes.py SquareToCircle -pl
```

