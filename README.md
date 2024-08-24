在终端上演示《传送门》片尾曲效果的 Python 脚本程序。

## 使用条件

原有的 `still_alive_credit_legacy.py` 脚本使用 Python 3（推荐使用 python 3.9，如果没有，推荐使用 `micromamba` 并用 `env.yml` 创建一个虚拟环境），以下提到的 `pip` 多数情况下对应 `pip3` 命令
以调用 Python 3 的 `pip` 组件。

Windows 下需要使用 Windows terminal，MinTTY 等支持 ANSI 终端转义序列的终端模拟器。

为了播放音乐，需要用 `pip` 安装 `playsound`。`playsound` 在 Linux 下依赖 
`pygobject` 包（可以使用 pip 安装它）。在 MacOS 下还需要用 `pip` 安装 `PyObjC`。


`still_alive_credit.py` 修改为了使用 `boombox` 播放音乐，不再依赖 `playsound`，能够更好兼容新版本（3.10+）的 Python。

使用 `pip` 安装 `boombox` 即可。
## 使用方法

在当前目录下执行：

```
python3 still_alive_credit.py
```

脚本会读取 `TERM`，`COLUMNS` 和 `LINES` 环境变量来调整输出区域大小并决定是否启用终端颜色等
特性。如果希望在一台标准 VT100 终端上演示，应该运行：

```
TERM=vt100 python3 still_alive_credit.py
```

可以使用 `--no-sound` 参数不带音乐进行演示，此时脚本只依赖 Python 标准库：

```
python3 still_alive_credit.py --no-sound
```

或者可以运行原有的 `still_alive_credit_legacy.py` 脚本，只需要替换文件名即可。

---

A demo of the credit song 'Still Alive' of Portal 1 written in Python, running
in text terminal.

## Dependency

`still_alive_credit_legacy.py` is written with Python 3 (Python 3.9 is recommended, you can create a virtual env with `micromamba` and `env.yml`). In most cases the following
`pip` should be `pip3` command.

In Windows system, you need a teminal emulator supporting ANSI escape sequences
like Windows Terminal, MinTTY, Cmder or ConEmu。

For playing music, you need install `playsound` with `pip`. In Linux `playsound`
depends on `pygobject`(`python-gobject` for systemwide install) (you can use pip to install this). In macOS, you also need
to use `pip` to install `PyObjC`.

`still_alive_credit.py` is modified to use `boombox` to play music, no longer depends on `playsound`, and is more compatible with newer versions of Python (3.10+).
## Usage

In current directory, execute:

```
python3 still_alive_credit.py
```

The script will read environment variable `TERM`, `COLUMNS` and `LINES` to determine
the output area size and whether to enable features such as terminal color. If you
want run it on a standard VT100 terminal, you should execute:

```
TERM=vt100 python3 still_alive_credit.py
```

It's able to use `--no-sound` option to run the script without playing sound. In this
case, the script only depends on Python standard library:

```
python3 still_alive_credit.py --no-sound
```

Or you can run the original `still_alive_credit_legacy.py` script, just replace the filename.

## Linux 运行效果 / Snapshot on Linux

![](still_alive_linux.jpg)

## 演示视频 / demonstration video

![](still_alive_informer213.jpg)

<https://www.bilibili.com/video/BV1cU4y1A7ud>
