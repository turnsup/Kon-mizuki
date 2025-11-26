# Mizuki 💮更美观的静态网页💮
原作者：https://github.com/matsuzaka-yuki 

<span style="background-color:#3498db; color:white; padding:2px 6px; border-radius:4px;">node.js=24.11.1</span>
<span style="background-color:#FFC0CB; color:white; padding:2px 6px; border-radius:4px;">pnpm=10.22.0</span>
<span style="background-color:#2ecc71; color:white; padding:2px 6px; border-radius:4px;">Astro=5.15.3</span>
<span style="background-color:#FFD700; color:white; padding:2px 6px; border-radius:4px;">TypeScript=5.9.3 </span>
<span style="background-color:#e74c3c; color:white; padding:2px 6px; border-radius:4px;">npm=11.6.2</span>
### 🎸按照自己的想法修改了一个轻音主题的mizuki网站
### 样例 K-on Mizuku
![网站样例](/sample/kon.png "kon")
我的放在了：8.148.86.13上，可以去看看。
## 🌼本地运行

### 第一步：
```bash
git clone https://github.com/matsuzaka-yuki/mizuki.git
cd mizuki
```
下载到本地，并进入目录
### 第二步
```bash
npm install -g pnpm
pnpm install
```
安装所需要的环境
### 第三步
根据需求修改相关文档

功能模块位于
`src/config.ts`进行修改
### 第四步
在mizuki路径下运行：
```bash
pnpm dev
```
点击http://localhost:4321进入网站

## 🌻功能修改
按照自己实际使用的一些修改：
### 🍓自我介绍
在``ProfileConfig``变量中，修改相关的信息，图片及链接。

图片链接放入在``assets/images/xxx.jpg``中进行引用。

在``announcementConfig``变量中，同样可以进行修改

### 🍒桌面背景

在``SiteConfig``的``banner``中修改背景，将需要的链接加入``public\assets\desktop-banner及mobile-banner``中，desktop为pc网页端壁纸，mobile为移动端网页壁纸

### 🍑音乐播放

在文件``src\components\widget\musicplayer.svelte``中，将``musicPlayerConfig.mode ?? "local"``修改为本地模式。

系统默认使用原作者的服务器音乐。
同时,需要在``localPlaylist``中出给相关本地音乐格式：
```	bash
	    id: 1,
		title: "ふわふわ時間",
		artist: "放課後ティータイム",
		cover: "assets/music/cover/fuwa.jpg",
		url: "assets/music/url/fuwa.mp3",
		duration: 240,
```
- id:该音乐编号
- title:音乐名称
- artisl:音乐作者
- cover:音乐封面,存放在``assets/music/cover/xxx.jpg``中
- url:音乐文件，存放在``assets/music/url/fuwa.mp3``中
- duration:音乐时长（s）

## 🌷其他功能
由于本人菜鸟，原作者大佬的一些功能感觉用不上就没有开启，如番剧界面，项目和技能界面等
### 🍊博客功能
在``src\content\posts``中新建文件夹，放入日记所需的图片和markdown文件。
markdown文件开头需要加入：
```BASH
---
title: EVA:终 观影
published: 2025-11-01
description: EVA:终 观影
tags: [comic, ACG,life]
category: Life
draft: false
---
```
- title:标题
- published:写作时间
- description:描述
- tags:标签
- category
- darft:草稿模式，关闭即可发布在网页上
### 🍍画廊功能
在```public\images\albums``中创建文件夹,
指定放入cover.jpg封面文件及其他图片，并且新建info.json文件：
```BASH
{
	"title": "KON gallery",
	"hidden": false,
	"description": "kon forever.",
	"date": "2025-11-17",
	"location": "shaft",
	"tags": ["Kawai", "Cute", "k-on"],
	"layout": "masonry",
	"columns": 3
}
```
- title:标题
- hidden: 是否隐藏
- description: 描述
- date: 发布时间
- location: 来源
- tags: 标签
- layout: 使用"masonry"的排列模板
- columns：布局列数

### 🍍日记功能
在```src/pages/diary.astro```中的``moments``,增加数据：
```BASH
	{
		id: 1,
		content: "K-ON forever!",
		date: "2025-11-17T16:30:00Z",
		images: ["/images/diary/kon_d.png"],
	},
```
- id: 序号
- content: 文字内容
- date: 编写时间
- images: 放置图片
图片放置于``public\images\diary``中


## 图片示例：
![样例1](/sample/s1.png "s1")

![样例2](/sample/s2.png "s2")

![样例3](/sample/s3.png "s3")

![样例4](/sample/s4.png "s4")