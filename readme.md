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
