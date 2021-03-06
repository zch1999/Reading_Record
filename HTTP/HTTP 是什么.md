# HTTP 协议是什么

HTTP（HyperText Transfer Protocol）：超文本传输协议

## HTTP 是什么

三个部分：“超文本”、“传输” 和 “协议”

### 协议

- 协议：HTTP 首先是一个协议
  1. 协议必须要有两个或多个参与者
  2. 协议是对参与者的一种行为约定和规范
- HTTP 是一个用在计算机世界里的协议
- **它使计算机能够理解的语言确立了一种计算机之间交流通信的规范，以及相关的各种控制和错误处理方式**

### 传输

HTTP 是一个传输协议，“传输”意味着把一堆东西从 A 搬到 B，或者从 B 搬到 A，即：A <===> B

- **HTTP 是一个 “双向协议”**

  有两个最基本的参与者 A 和 B，数据在 A 和 B 之间不是单项流动的。上网的时候双方约定用 HTTP 协议来通信，浏览器把一些数据发送给网站，网站再把一些数据发回给浏览器展示在屏幕上

- 数据虽然在 A 和 B 之间传世，但并不仅限于 A 和 B 两个角色，可以有 “中转” 或者 “接力”

  也就是 A <=> X <=> Y <=> Z <=> B

  A 到 B 的传输过程中可以存在任意多个 “中间人”，他们都遵循 HTTP 协议，只要不打扰基本的数据传输，就可以任意添加额外的功能，例如：安全认证、数据压缩、编码转换等

**HTTP 是一个在计算机世界里专门用来在两点之间传输数据的约定和规范**

### 超文本

- **文本：**文本表示 HTTP 传输的不是 TCP/UDP 那种被切分的二进制包，而是完整有意义的数据，可以被浏览器、服务器处理

  互联网早期，文本只是简单的字符文本，但在现在的 HTTP 眼里，图片、音频、视频、甚至是压缩包都可以算作是文本

- **超文本：**超越了普通文本的文本，是文字、图片、音频和视频等的混合体，**最近关键的是含有 “超链接”**，可以从一个 “超文本” 跳跃到另一个 “超文本”，形成复杂的非线性、网状的结构关系

- HTML 就是超文本，本身是纯文字文件，但内部有很多标签定义了对图片、音频、视频等的链接

**HTTP 是一个在计算机世界里专门在两点之间传输文字、图片、音频、视频等超文本数据的约定和规范**

## HTTP 不是什么

HTTP 是一个协议和通信规范，**不存在 “单独的实体”**

- HTTP 不是互联网

  超文本资源使用 HTTP，普通文件使用 FTP，电子邮件使用 SMTP 和 POP3

  HTTP 是构建互联网一块重要拼图，而且是占比最大的那一块

- HTTP 不是编程语言

  HTTP 是计算机和计算机沟通交流的语言，无法使用 HTTP 编程，但是可以用编程语言实现 HTTP

- HTTP 不是 HTML

  HTML 是超文本的载体，HTTP 传输的最多的就是 HTML

- HTTP 不是一个孤立的协议

  HTTP 通常跑在 TCP/IP 协议栈之上，依靠 IP 协议实现寻址和路由、TCP 协议实现可靠数据传输、DNS 协议实现域名查找、SSL/TLS 协议实现安全通信。WebSocket 和 HTTPDNS 协议依赖于 HTTP

## HTTPS 

**HTTP over SSL/TLS**

互联网上不仅有 "美女"，也有 "野兽" 

假设你打电话找小明要一份广告创意，很不幸，电话被商业间谍给窃听了，他立刻动用种种手段偷窃了你的快递，就在你还在等包裹的时候，他抢先发布了这份广告，给你的公司造成了无形或有形的损失

可以使用加密的方式防止这种情况 

例如： 

> 你：“喂，小明啊，接下来我们改用火星文通话吧。” 
>
> 小明：“好啊好啊，就用火星文吧。” 
>
> 你：“巴拉巴拉巴拉巴拉……” 
>
> 小明：“巴拉巴拉巴拉巴拉……” 



如果你和小明说的火星文只有你们两个才懂，那么即使窃听到了这段谈话，他也不会知道你们到底在说什么，也就无从破坏你们的通话过程。

HTTPS 就相当于这个比喻中的“火星文”，它的全称是“HTTP over SSL/TLS”，也就是运行在 SSL/TLS 协议上的 HTTP。

HTTPS 相当于 “HTTP+SSL/TLS+TCP/IP”