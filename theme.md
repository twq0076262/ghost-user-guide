# Ghost 主题
开始创建属于你的 Ghost 主题

## 变更主题

Ghost 的主题放在 `content/themes/`

如果你想用其他主题替换缺省的 Casper 主题，可以看看我们的 [marketplace gallery](http://marketplace.ghost.org/) 上的这些自定义主题。下载你喜欢的主题，解压之后放进 `content/themes` 里，和 Casper 放一起。

如果你想自己做个主题，我们建议你复制 casper 文件夹，然后在复制的文件夹里修改模版，按你喜欢来做。

要切换到你新添加的主题：

1. 重启 Ghost 。Ghost 不会立即发现你往` content/themes` 新添加了文件夹，所以你需要重启 Ghost。
2. 登录 Ghost 管理后台，进入`/ghost/settings/general/`页面。
3. 在“Theme”下拉菜单里选择你的主题的名字。
4. 点“保存”。
5. 查看博客的前端，欣赏你的新主题吧！

## Handlebars 是什么？

[Handlebars](http://handlebarsjs.com/) 是 Ghost 使用的模版语言。

Handlebars 提供了可以使你轻松高效地建立语义模版的功能。

如果你正打算开始自己写主题，也许先熟悉熟悉 handlebars 的语法是个不错的选择。看看 [handlebars 文档](http://handlebarsjs.com/expressions.html)，或者看看 [Treehouse 上的教程](http://blog.teamtreehouse.com/getting-started-with-handlebars-js) —— 这样你就可以跳过开始的安装和使用步骤（我们帮你做好了一部分），同时避免和“基本表达”纠缠。

## 关于 Ghost 主题

Ghost 的主题旨在做到易于编写和维护。Ghost 主题推崇模版（HTML）和业务逻辑（JavaScript）之间的分离。Handlebars （几乎）是没有逻辑，并且强化了这个分离，同时提供部件来帮助用来显示内容的业务逻辑保持独立。这种分离使在制作主题时，开发者和设计师之间的合作更加容易。

Handlebars 模版是分等级的（一个模版可以扩展另一个），也支持模块化的模版。Ghost 拥有这些特性，使得代码的重复得以减少，同时每一个模版可以保持专注于实现单一功能，并且做到好。拥有良好架构的主题将很容易维护，而各个组成部分之间的分离使得他们可以在不同主题之间重复利用。

希望你喜欢我们构造主题的方法。

## Ghost 主题的文件架构

我们推荐如下架构：

```
.
├── /assets
|   └── /css
|       ├── screen.css
|   ├── /fonts
|   ├── /images
|   ├── /js
├── default.hbs
├── index.hbs [必需]
└── post.hbs [必需]
```