---
title: '基于Astro.js + Netlify搭建个人博客.'
description: 'Astro.js提供了一个现代，高效，易于使用的框架，使得开发个人博客变得更加简单和直接'
publishDate: '2023-11-28'
tags: ['astro']
# draft: true
---

Astro.js提供了一个现代，高效，易于使用的框架，使得开发个人博客变得更加简单和直接。

## 主要特点：

-   组件群岛: 用于构建更快网站的全新 web 架构。
-   服务器优先的 API 设计: 移除客户端上高资源消耗的激活过程。
-   默认零 JS: 没有 JavaScript 运行时开销来减慢你的速度。
-   边缘就绪: 在任何地方部署，甚至像 Deno 或 Cloudflare 这样的全球边缘运行时。
-   可定制: Tailwind, MDX 和 100 多个其他集成可供选择。
-   不依赖特定 UI: 支持 React, Preact, Svelte, Vue, Solid, Lit 等等。

![Astro](https://storage.googleapis.com/papyrus_images/d7c2def7e919da60c45eaa3ae0db45b7.png)

## 你可以从0开始构建你的博客。

![Astro](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2Fb399a628d073d344f20d5742722e94dc.png&w=828&q=75)

我更加推荐从主题模板构建你的博客，下面我将介绍如何构建你的Astro博客；

## 主题商城中挑选出你感兴趣的主题

![Alt text](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2F69fc2f669aad18a600c93ecde4564eed.png&w=828&q=75)

## 选择主题，关联你新的博客仓库

我选择的主题是：[astro-theme-cactus](https://github.com/chrismwilliams/astro-theme-cactus#demo-%F0%9F%92%BB)
![Alt text](https://storage.googleapis.com/papyrus_images/f7c4700fb3b763876dea583a694133c5.png)

## 拉取刚刚关联仓库的代码

回到仓库目录安装依赖

```js
npm install
```

![Alt text](https://storage.googleapis.com/papyrus_images/f2fb6069ab1d43723e9bcb968b233b65.png)
这里注意，node版本必须 >=18.14.1，否则会报错
![Alt text](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2Fd1b05e425e370382da43d3de0e3938dd.png&w=828&q=75)

## 运行项目

```js
npm run dev
```

![Alt text](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2F721f8269569972363ae25d2bbc50869e.png&w=828&q=75)

这个时候astro的项目已在本地运行成功，接下来在src写构建你的博客内容，目录结构解释如下：

```js
-   .astro 这个目录是 Astro.js 项目的根目录，用于存放 Astro.js 的配置文件
    -   config.js Astro.js 的配置文件，用于指定全局配置选项，例如构建输出目录、插件等
-   components 这个目录用于存放 Astro.js 组件，组件是 Astro.js 中最基本的构建单元
    -   Layout.astro 一个示例组件，用于定义网页的布局和结构。
-   dist 这个目录是构建过程中生成的目标输出目录，包含最终生成的静态网页文件。
-   pages 这个目录用于存放网站的页面文件，每个页面对应一个 Astro.js 组件。
    -   index.astro 一个示例页面文件，表示网站的首页。
-   static 这个目录用于存放静态资源文件，例如图片、样式表、JavaScript 文件等。
-   package.json 这个文件是 Node.js 项目的配置文件，其中包含了项目的依赖项和脚本命令等信息。
-   README.md 这个文件是项目的说明文档，通常包含了项目的介绍、使用方法和其他相关信息。

```

更多配置项请阅读官网文档：[Astro](https://docs.astro.build/zh-cn/getting-started/)
![Alt text](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2Fa048f8c214f6cd9c676e63c5c6375dac.png&w=828&q=75)
![Alt text](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2F3f5547abc502915b2256584aeccb561e.png&w=828&q=75)

## 导入Netlify

进入Netlify 官网，导入刚刚的astro-blog仓库

![Alt text](https://storage.googleapis.com/papyrus_images/d110971508f39b7bfc49b68afd3a2530.png)

点击 ：Deploy astrojs-blog 开始构建项目
![Alt text](https://storage.googleapis.com/papyrus_images/a8684f9088b8e61783b4193609c88a19.png)

项目构建完成后，修改一下项目域名

```js
Site configuration > General > Site details > Change site name
```

![Alt text](https://paragraph.xyz/_next/image?url=https%3A%2F%2Fstorage.googleapis.com%2Fpapyrus_images%2F67d536258558c128d62052d03bb376ff.png&w=828&q=75)

这样基于astro的个人博客站点就构建好了，我们可以通过互联网访问刚刚配置的域名：https://astro-lzt.netlify.app/

## 自动化部署

接下来你只需要本地修改文件推送到你刚刚关联的仓库，Netlify就会自动检测并拉取你的最新代码进行自动部署，你要做的只是推送一下代码即可！
![Alt text](https://storage.googleapis.com/papyrus_images/27468ade99e05be73396a5093d90b81e.png)
![Alt text](https://storage.googleapis.com/papyrus_images/73d1a944788b4db9049a2d566fcc478e.png)
![Alt text](https://storage.googleapis.com/papyrus_images/3a40e22d8085b59d73251591e1b99da3.png)
