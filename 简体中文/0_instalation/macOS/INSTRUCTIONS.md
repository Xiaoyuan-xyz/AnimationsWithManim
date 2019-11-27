# 在 MacOS 上安装

[视频教程(需要翻墙)](https://www.youtube.com/watch?v=uZj_GQc6pN4).

## 安装依赖

### 打开终端
在Spotlight里搜索“终端”。

<p align="center"><img src ="/English/0_instalation/macOS/gifs/terminal.png" /></p>

### 安装 Homebrew
复制 [Homebrew](https://brew.sh) 里的命令然后粘贴在终端中。

<p align="center"><img src ="/English/0_instalation/macOS/gifs/MacP1.gif" /></p>

### 安装 LaTeX (versión completa)
到 [MacTeX](http://www.tug.org/mactex/),上下载 .pkg 文件后安装([帮助](https://www.youtube.com/watch?v=5CNmIaRxS20))。

<p align="center"><img src ="/English/0_instalation/macOS/gifs/MacP2.gif" /></p>

### 安装 Python 3
在 [Python](https://www.python.org/)的官网上下载 python 3.7 ([帮助](https://www.youtube.com/watch?v=0hGzGdRQeak)).

<p align="center"><img src ="/English/0_instalation/macOS/gifs/MacP3.gif" /></p>

### 安装 PIP
运行如下的命令：

```sh
brew install curl
mkdir ManimInstall
cd ManimInstall
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
```

### 安装 FFmpeg， SoX 和 Cairo.
运行如下的命令：

#### FFmpeg
```sh
brew install ffmpeg
```
#### Sox
```sh
brew install sox
```
#### 其他
```sh
brew install cairo
```

如果安装失败的话：

```sh
brew install cairo --use-clang
```

```sh
brew install py2cairo
```

```sh
brew install pkg-config
```

<p align="center"><img src ="/English/0_instalation/macOS/gifs/MacP5.gif" /></p>

### 下载 [最新版](https://github.com/3b1b/manim) 或 [20190203版](https://github.com/3b1b/manim/tree/3b088b12843b7a4459fe71eba96b70edafb7aa78)的Manim。

<p align="center"><img src ="/English/0_instalation/macOS/gifs/DescargarManim.gif" /></p>

### 解压到一个没有空格(和中文)的路径下

<p align="center"><img src ="/English/0_instalation/macOS/gifs/pd.png" /></p>

### 安装 requirements.txt 内的需求
在终端中打开 manim-master 目录并运行：

```sh
python3 -m pip install -r requirements.txt
python3 -m pip install pyreadline
python3 -m pip install pydub
```

<p align="center"><img src ="/English/0_instalation/macOS/gifs/MacP6.gif" /></p>

# 运行 Manim

在 manim-master 目录下运行：

```sh
python3 -m manim example_scenes.py WriteStuff -pl
```

该命令会生成如下的视频：

<p align="center"><img src ="/English/0_instalation/macOS/gifs/MacP8.gif" /></p>

