# 知识如果不记录，就会流失90%

[![License](https://img.shields.io/github/license/zhukunpenglinyutong/notes.svg)](LICENSE)
[![repo-size](https://img.shields.io/github/repo-size/zhukunpenglinyutong/notes.svg)](repo-size)
[![CodeTriage](https://www.codetriage.com/zhukunpenglinyutong/notes/badges/users.svg)](CodeTriage)
[![提交活动](https://img.shields.io/github/commit-activity/m/zhukunpenglinyutong/notes.svg)](提交活动)
[![最后一次提交](https://img.shields.io/github/last-commit/zhukunpenglinyutong/notes.svg)](最后一次提交)

<img src="https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1559637808&di=b2b7de8007a8e1c5e3ea07f3b2ae0192&src=http://5b0988e595225.cdn.sohucs.com/images/20171230/a540bdf43bdc49828f40a8a0e50ae762.jpeg" />

---

# 更佳体验 🚀

要想获得更佳体验，请访问 [notes.itzkp.com](https://notes.itzkp.com)

---

# 项目特殊情况公示

- ~~2019.6.20 开发者去拿毕业证了，今天一天没办法维护库，21号回复正常，并将实践 性能优化内容~~

---

# 项目说明 📚

### 🔥项目核心思想说明（推荐阅读）

- [查看项目核心思想](https://notes.itzkp.com/2.note/0.%E9%A1%B9%E7%9B%AE%E6%96%B9%E5%90%91%E6%8C%87%E5%8D%97/0.%E9%A1%B9%E7%9B%AE%E6%A0%B8%E5%BF%83%E6%80%9D%E6%83%B3.html)

### 1.quickcheck（速查）

放着系统性的知识笔记系统，熟悉内容之后，可以快速查阅内容，极大的提高开发效率

### 2.note（笔记）

主要放着项目规划，每日记录，还有一些知识笔记，后期可与速查产生关联，作为速查笔记的拓展内容，进行拓展阅读

### 4.项目更新日志

[查看更新日志](https://github.com/zhukunpenglinyutong/notes/blob/master/record.md)

---

# 网站构建（notes.itzkp.com） 🌳

### 1.构建过程

```js

git clone https://github.com/zhukunpenglinyutong/notes.git

npm install

npm run dev（预览，VuePress会启动一个预览的网址）

npm run build（打包，打包后资源在 docs/.vuepress/dist下）

```

**构建原理说明**：根据app.js 书写匹配规则和进行目录调整，达到VuePress能够识别的程度

**环境依赖：node**
- [notes.itzkp.com node安装教程（更快速的安装 Centos系统下）](https://notes.itzkp.com/1.quickcheck/3.%E8%BF%90%E7%BB%B4/1.Centos%E4%B8%8B%E5%AE%89%E8%A3%85%E5%90%84%E7%A7%8D%E8%BD%AF%E4%BB%B6.html#_1-%E5%AE%89%E8%A3%85nodejs)
- [node官方下载](https://nodejs.org/en/download/)

---

### 2.CI/CD实现（基础版）

**环境依赖：Jenkins**

[notes.itzkp.com 安装Jenkins教程](https://notes.itzkp.com/1.quickcheck/3.%E8%BF%90%E7%BB%B4/1.Centos%E4%B8%8B%E5%AE%89%E8%A3%85%E5%90%84%E7%A7%8D%E8%BD%AF%E4%BB%B6.html#_7-%E5%AE%89%E8%A3%85-jenkins)


**GitHub pull触发自动构建实现**

[资料网址](https://www.cnblogs.com/weschen/p/6867885.html)

**因为Jenkins用的比较浅，所以用shell的方式进行Jenkins的操作**

```js
// notes-job 执行的 shell 脚本内容示例
npm install
npm run build
rm -rf /notes/dist
cp -r ./docs/.vuepress/dist/ /notes/
```
---

### 3.网站的意义 && 以后的规划 && 其他

**网站的意义**

[notes.itzkp.com对于我的意义...待完善](https://notes.itzkp.com/2.note/4.%E5%85%B6%E4%BB%96%E9%9B%B6%E6%95%A3%E7%AC%94%E8%AE%B0/notes.itzkp.com%E5%AF%B9%E4%BA%8E%E6%88%91%E7%9A%84%E6%84%8F%E4%B9%89.html)

**以后的规划**

- [v0.3方向指南...待完善](https://notes.itzkp.com/2.note/0.%E9%A1%B9%E7%9B%AE%E6%96%B9%E5%90%91%E6%8C%87%E5%8D%97/v0.3%E6%96%B9%E5%90%91%E6%8C%87%E5%8D%971.html)
- [v0.4方向指南...待完善](https://notes.itzkp.com/2.note/0.%E9%A1%B9%E7%9B%AE%E6%96%B9%E5%90%91%E6%8C%87%E5%8D%97/v0.4%E6%96%B9%E5%90%91%E6%8C%87%E5%8D%97.html)

**CI/CD 拓展（未完成）**

- 构建完成之后邮箱提醒
- 构建错误的补救
- ......

**网站详细构建过程**

- [朱昆鹏的掘金文章....书写中](https://juejin.im/post/5d03cee16fb9a07ea33c12d7)

---

### 4.网站访问通知

- ❗️2019.6.21 凌晨12点 - 2019.6.21 6点，将再次试验前端性能优化，届时notes.itzkp.com网站可能不可访问

---


# 不足与指教 🌛

因为入行的时间太短（2019.6.20日大学毕业，目前已实习一年），所以项目会有很多地方不完善。各位前行者，大佬们，如果看出这个项目有的地方可以完善，或者有的地方不好，我拜求各位的指点，我会以很快的速度验证，然后更改的。我会时刻以谦逊姿态请教学习，高调的热情创造宣传，我期待各位大佬们能指出我的不足，我定会虚心请教，牢记恩情。（很多思想不是我不用，是我不知道，所以拜求指教）

**个人微信，拜求指点，不胜感激**

<img src="https://itzkp-1253302184.cos.ap-beijing.myqcloud.com/notes/%E5%85%B6%E4%BB%96/3.png">

---

# 致谢 🦀

致谢所有 star 和 关注我的 朋友们，多谢你们的鼓励和支持 🦀🦀🦀 ，维护一个项目是一个长跑 🏃，这比的是谁能够坚持下去，多谢各位的行动给我的鼓励，我会继续加油的，以掘金阴明（创造了技术交流圈）为偶像，向偶像看齐!!! 并致力于打造技术工具链，节省时间，本项目是为了节省自己开发效率而制作的，也是为了另一个项目 no996happy 进行的前置尝试，敬请期待。
