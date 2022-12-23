# Hugo-RSS-Only

This project uses Hugo only to generate [RSS](https://en.wikipedia.org/wiki/RSS).

英语不好憋不住了，来点中文：
本项目是对 Hugo 的大材小用，这里特别关闭了一些 RSS 用不到的特性，仅仅为生成 RSS 服务。
配置文件特别简单，除了 RSS 要用到的 `网站标题`、`作者` 外，其他的东西直接写到 `index.html` 里面就行。
如果要加 JS 或者 CSS，建议都写到该文件、或者使用外部 CDN，要不然还要按照 Hugo 文档匹配路径。

# Get-Start

To keep simple, Hugo-RSS-Only lacks some specific files for becoming a normal hugo-theme.

However, we can directly run it like this:

```bash
git clone https://github.com/qaqland/hugo-rss-only.git

cd hugo-rss-only

hugo # or hugo server
```

Then we look into detail:

```yaml
# config.yaml

baseurl: "/"                    # Keep default `/`, or change it to your domain.
title: "Welcome to qaqLand!"    # HTML and RSS title
author:
  name: qaqland                 # RSS will show author's name
  email: qaq@qaq.land           # HTML and RSS will show author's email
```

It's also easy for you to modify home page `index.html`.

```html
For online documentation and support please refer to
<a href="https://github.com/qaqland">github.com/qaqland</a>.<br />
```

Here is my GitHub name and address, just try to change it!

# Thanks to:

- `layout/index.html` edited from nginx's default html
- `layout/_default/rss.xml` copyed from [GithubGist/jdheyburn/hugo_rss.xml](https://gist.github.com/jdheyburn/a0a2c678f8f9795088b2779ec6af9920)
