---
title: "Weekly 02: 汗颜无地"
date: 2023-11-19T00:19:47+08:00
draft: false
categories: ['weekly']
---
本篇是对2023/09/20-2023/11/16的总结，从落笔开篇到现在才动手发布新的周刊，笔者感到很惭愧，笔者的第一个目的督促自己学习没有达到好的效果, 当然这纯粹是笔者自己的问题, 接下来笔者会督促自己, 尽量每周完成应完成的周刊

## 2023-09-20
### SSH代理配置
因为家里通过`terminal`访问`github`时经常超时, 故研究了下如何设置SSH访问代理服务器.

通过编辑`vi ~/.ssh/config`配置文件, 配置`github`的`443/22`端口通过`ProxyCommand`连接 VPN Socket5 地址

## 2023-09-22
- [为什么读书无用](https://letters.geekplux.com/41/) #读后感 
	- 作者并非讲述读书无用论, 而是阐述读者读书时可能没有将其转换成自己的知识
	- 实践中学习才是最快的
		- 笔者学习新知识时反而很少做到边实践边学习, 后续可以考虑学习时加入实践看是否提高效率
	- 读书时需要调动自己的 元认知能力 消化知识
	- 知识类的传输(写作/视频)可以考虑减少读者调用 元认知能力 所耗费的精力

## 2023-09-27
- Chrome Load Overrides #chrome #DX 
	- Chrome 117 出的新特性, 支持拦截接口, 修改接口请求/响应; 适合前端同学本地开发项目时没有mock服务时使用
	- Chrome Devtool -> Network -> 选择`fetch/XHR`接口 -> 右键 Override headers/content
- Prompt 优化 #ai
	- 引导模型推理
		- 引导模型进行深入思考, 投入更多的时间逻辑思维
		- 例如: 问这个回答是否正确, 可以让模型先自己计算一遍结果, 并且与回答相互对照
	- 参考: https://guangzhengli.com/blog/zh/gpt-embeddings/

## 2023-10-07
- [The Uphill Battle of Memoization](https://tkdodo.eu/blog/the-uphill-battle-of-memoization) #React 
	- `React.memo`存在大量的心智负担, React比较`prop`是否相等是通过`Object.is`判断, 所以要求上层使用者使用该`Component`时考虑此问题, 很容易被上层使用者忽略导致其无效化
	- React`children`会破坏`React.memo`的优化能力, 每次`children`都会重新执行`React.createElement`创建新的对象, 导致`React.memo`无效化
- 了解到了握手相关的知识
  - 优点
    - 在动作上能体现双方的平等
  - 弊处
    - 受到医学界的诟病，病毒和细菌的传播很可能通过握手来实现
  - 注意点
    - 男女间握手时要轻握不全握
- 粥的营养含量很低

## 2023-10-12
- `Element.closest()`
	- 获取匹配特定选择器且离当前元素最近的祖先元素(包含其本身)
	- [Reference](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/closest)

## 2023-10-27
- [Thinking Locally with Signals](https://dev.to/this-is-learning/thinking-locally-with-signals-3b7h) #读后感 #Solid
	- 讲述了 Locality of Thinking - 局部性思维 对 Solid 的 Signal 实现的影响
	- 表现形式: 单向数据流/读写隔离
	- 其中的思想都是老生常谈的话题, 例如: 单向数据流的好处, 读写隔离的好处
	- 不过里面提到了 Signal 的响应式更新是细粒度更新, 变相验证了 VDOM 对于响应式而言只是纯粹的损耗, 可惜没有延伸开讲

## 2023-10-31
- Barrel file 的坏处很多, 平常项目内开发时应该避免使用
	- 可能导致`tree-shaking`失效
	- 会导致编译时模块`re-import`, 从而耗费更多的编译时间, 这在开发模式热更新的时候难以忍受

## 2023-11-14
-  [Take less information in, but do more with it](https://www.dsebastien.net/take-less-information-in-but-do-more-with-it/) #读后感 #学习方法论
	- 如何快速过滤“噪音”
		- 明确自己的目标和需求, 一旦知道自己想要什么就会知道是否应该阅读/忽略这些信息
		- 如果现在不需要它就可以忽略它 - Note: 这点有待商榷, 可以先将其归类到 bookmark, 等到需要的时候再看
	- 如何消费/处理这些信息
		1. 添加到笔记中并且备注其来源
		2. 粗读内容, 挑选出其中有深入研究价值的内容
		3. 当时间足够的时候, 暂停粗读, 对之前挑选出的内容进行深入研究
	- 如何从信息中获取更多价值
		- 有价值的信息往往意味着其信息源的其他信息也是高质量, 高质量文章的作者的其他文章大概率也是高质量的
		- 保留来源, 方便追溯以及参考
		- 实践更易用掌握知识, 并且更能有自己的思考
		- 将知识点原子化, 便于创建可靠的心智模型
		- 通过工具将知识点链接, 例如使用 obsidian 的 graph view
		- 输出, 对学习到的知识进行再加工, 并以自己的理解输出其概念

## 2023-11-15
- [57.心声特辑：重新养育自己，为自己提供不可动摇的爱与保护](https://open.spotify.com/episode/6ieVaMn2uJlNgjRXd1LPyD?si=b1e19c05d3c84824)
	- 安慰身边的人时, 常常会说你值得被爱, 这句是道理, 这时候可以再加上“比如我在爱你”, 这时候你让这句话不只是安慰而变成了暖心的事实

## 2023-11-16
- [Future of rendering in react](https://prateeksurana.me/blog/future-of-rendering-in-react/) #读后感 
	- 描述了现在 前端建站技术栈 的优劣, 指出 React 在未来为其做了哪些增强/支持
	- Suspense将支持 Stream SSR 并且为其提供 Hydration 即使其还处于 Streaming 阶段, 这一点不仅是减少了 TTFB 的时间, 还可以减少用户 TTI 的时间
	- 重点讲述了 React Server Component 的优势, 例如直接访问数据库, 减少 Client 端资源(例如部分非交互功能依赖于某个重型库, 此时就可以用 RSC 在服务端渲染该功能)

## 些许感悟

### 取法乎上，仅得其中 #名言
今天看《令人心动的Offer》的时候，史律提到了如何看待他人的成长, 可以是给出一个高的要求，但不要把期望拉满，他人有明显的成长即是好的

### Nobody can control mind, but you can pull it back. #名言
- 本期 podcast 笔者听到的一句特别有感触的一句话
- 你不能完全控制你的思想, 当你学习时你不能限制你不走神, 但是你可以在你发现你走神的时候把你自己拉回来
- Refer: 代码之外 第 3 集 | 英语学习经验、泰国禅修体验

### 如何以过来人的身份安慰当前经历者
- 本期 podcast 讲到了姐姐对弟弟目前遇到的问题时当时举止的思考, 我们容易站在过来人的立场上对他人当前的困境指手画脚, 没有对他人的焦虑予以充分尊重, 我们更应该做的是倾听和鼓励
- Refer: 展开讲讲 56.姐！发出我尊敬的声音

### 如何处理工作中不合理的任务
- 就事论事, 确保协作氛围不受影响；体现职业性, 如果你只是提意见的, 那么充分提出自己的建议即可；
- Refer：[代码之外 | 第 6 集](https://www.xiaoyuzhoufm.com/episode/64e2f4db3fa4090b74d2839f)
