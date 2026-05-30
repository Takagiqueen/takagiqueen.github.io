# Ubuntu 部署笔记

## 方式一：本地构建后上传 dist

本地执行：

```bash
npm install
npm run build
```

然后把 `dist/` 上传到服务器，例如：

```txt
/var/www/personal-site
```

服务器安装 Nginx：

```bash
sudo apt update
sudo apt install nginx -y
```

把 `deploy/nginx-personal-site.conf` 按你的域名修改后放到：

```txt
/etc/nginx/sites-available/personal-site
```

启用配置：

```bash
sudo ln -s /etc/nginx/sites-available/personal-site /etc/nginx/sites-enabled/personal-site
sudo nginx -t
sudo systemctl reload nginx
```

## 方式二：服务器拉 GitHub 后构建

服务器需要安装 Git 和 Node.js。Node.js 建议用 nvm 安装 LTS 版本。
