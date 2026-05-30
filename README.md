# 希儿的个人网站 v0.1

技术栈：Astro + Tailwind CSS + TypeScript + MDX

定位：个人主页 / 博客 / 项目展示 / LeafVault 介绍页。

## 本地运行

```bash
npm install
npm run dev
```

打开终端显示的本地地址，一般是：

```txt
http://localhost:4321
```

## 构建部署

```bash
npm run build
```

构建后会生成：

```txt
dist/
```

把 `dist/` 里的内容部署到 Nginx、Netlify、Vercel、Cloudflare Pages 都可以。

## 推荐后续修改顺序

1. 修改 `src/components/Hero.astro` 的个人介绍。
2. 修改 `src/components/Projects.astro` 的项目卡片。
3. 修改 `src/content/blog/*.mdx` 的博客内容。
4. 替换 `public/images/` 里的项目截图。
5. 部署前修改 `astro.config.mjs` 里的 `site`。

## 设计方向

清新自然、淡绿色、浅蓝色、毛玻璃、柔和渐变、轻微动效，不做过重 3D 和复杂 WebGL。
