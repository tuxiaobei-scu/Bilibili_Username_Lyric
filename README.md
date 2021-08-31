# 全自动B站用户名组成歌词+视频渲染生成

### 介绍
全自动B站用户名组成歌词+视频渲染生成

自动调用 bilibili API 获取搜索结果

通过分词和加权贪心算法，智能生成最优组合结果

自动根据结果渲染视频，可在视频中显示头像、用户名、个人简介等信息

用户名选择原则：目标词必须在用户名中连续，且歌词不能漏掉任何一个字

### 安装教程

安装依赖
```
pip install -r requirement.txt
```

此外需要安装 `ffmpeg` 以合并图像与声音

### 使用说明

1.  下载歌词 `lrc` 格式文件，命名为 `music.lrc`，删去无关部分（如歌手信息，歌曲名称）放置于根目录
2.  下载视频 `mp4` 格式文件，命名为 `video.mp4`，放置于根目录
3.  运行 `python calc.py`，生成 `res.json` 中间文件，此文件为自动爬取并组成的用户名，可以进行修改
4.  运行 `python render.py`，渲染出视频 `final.mp4`

### 样例

![](example.jpg)

