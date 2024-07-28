> [!IMPORTANT]
>
> Coze自动生成海报！！！

[toc]

### 一、准备阶段

#### 1.思路设计

（1）搭建MVP最小可行产品

（2）细节优化：交互体验

（3）支持批量操作

#### 2.物料准备

（1）海报底图

（2）海报文案

![image-20240711213628173](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240711213628173.png?AI_make_money=VX_AI19858122061)

### 二、最小MVP搭建

首先，登陆coze.cn，新建bot，命名：“海报生成器”。

其次，在“海报生成器”的bot开发页面，挑选：图像流，并点击右边的➕。



接着，点击“创建图像流”，来到图像流编辑页面。仔细看左边，是各种AI图片的风格模型，可以根据自己需要，选择合适的模型。

![image-20240711210300958](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240711210300958.png?AI_make_money=VX_AI19858122061)

注意：图像流和图片流分开了，这在软件工程中叫做：解耦；解耦是为了方便不同功能模块可以自由搭配。

从“开始”节点，录入基本的参数：用户昵称、活动名称、背景信息等需要在海报上展示的点。

![image-20240711211005967](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240711211005967.png?AI_make_money=VX_AI19858122061)

新增一个“添加文字”节点，并设置具体的参数。

![image-20240711211435019](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240711211435019.png?AI_make_money=VX_AI19858122061)

具体的参数设置情况。一方面来自“开始”节点，一方面从海报里提取出来的信息。

![image-20240711213152294](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240711213152294.png?AI_make_money=VX_AI19858122061)

海报提取信息，可以从：https://www.photopea.com/ 中获取。

![image-20240711213303663](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/%E7%9A%AE%E5%85%8B%E6%96%AF.png?AI_make_money=VX_AI19858122061)