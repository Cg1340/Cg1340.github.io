---
layout: wiki
title: 我 Musicplayer 项目的教程
cate1: Projects
cate2:
description: Musicplayer 项目的教程
keywords: musicplayer
---

## 我 Musicplayer 项目的教程

现在这个项目有两个分支: C++ 版本和 Rust 版本。我推荐你用 C++ 版本，因为它更完善（Rust版本在开发中）

## 安装

直接从 Releases 里下载我编译好的安装包就行。

由于使用 Win32 API，所以 Linux 不能编译和运行。

## 使用

文件树如下，所有东西都不能删除，否则不能使用：

```
MusicPlayer.exe
一些 .dll 文件
src
  | music
  |   | 一些音乐文件
  | list.json
  | Minecraft AE.ttf
  | Minecraft Regular.otf
  | music_disc_13.png
  | toasts.png
```

### 增加/删除音乐

``list.json`` 的结构如下：

```json
{
  "version": 100,
  "show_warning": true,
  "mode": "random",
  "font": "Minecraft AE.ttf",
  "background_info": {
    "image": "toasts.png",
    "rect": [ 0, 0, 160, 32 ],
    "scale": [ 3.0, 3.0 ]
  },
  "background_warn": {
    "image": "toasts.png",
    "rect": [ 0, 64, 160, 32 ],
    "scale": [ 3.0, 3.0 ]
  },
  "music": [
    {
      "file": "file",
      "name": "display_name"
    },
  ]
}
```

其中 ``music`` 项其中的每一项都有两个键值对：
- ``file`` 键表示文件名，必须放在 ``music`` 文件夹里；
- ``name`` 键决定了要显示的名称是什么

### 键盘操作

- ``Alt+1`` 退出
- ``Alt+2`` 音量减小
- ``Alt+3`` 音量增大
