---
name: my-design-system
description: "我的品牌 的设计系统（基于 Google Material Design 3）。为「我的品牌」做任何网页、App 界面、原型或海报时使用：所有颜色、字体、圆角、阴影和组件都从这里取，不要自己发明新样式。"
---

# 我的品牌 设计系统

> 基于 Google Material Design 3（m3.material.io），令牌名字和官方一致。由 Feeling Futures「设计系统生成器」生成于 2026-11-18。

## 品牌

- 名字：我的品牌

## 给 AI 的规则（必须遵守）

1. 页面最外层加 `class="m3"`；深色模式用 `class="m3 dark"`。把同一个文件夹里的 `design-system.css` 用 `<link>` 引入；如果不能引用文件，就把它的内容整段放进 `<style>`。
2. 颜色只用颜色角色变量 `var(--md-sys-color-…)`，**不要写死 #色值**，也不要发明新颜色。
3. 文字或图标放在某个颜色上，就用对应的 `on-` 颜色：primary 上用 on-primary，primary-container 上用 on-primary-container，以此类推。
4. 文字只用 15 个字体角色类（`.m3-display-large` … `.m3-label-small`），不要自己设字号。
5. 圆角、阴影、间距、动效都用令牌（`--md-sys-shape-corner-*`、`--md-sys-elevation-level*`、`--md-sys-motion-*`）。
6. 一个区域里最多一个 filled 按钮；其它按钮用 tonal / outlined / text。一屏最多一个 FAB。
7. 先用下面已有的组件。确实没有的，用同样的令牌拼一个新的，保持同样的圆角、描边和阴影风格，类名用 `m3-` 开头。
8. 图标用 Material Symbols：`<span class="m3-icon">图标英文名</span>`（名字在 https://fonts.google.com/icons 查）。只有图标的按钮要写 `aria-label`。
9. 能点的东西至少 48×48px；文字和背景的对比度至少 4.5:1（用配套的 on- 颜色就一定够）。
10. 间距用 4 的倍数：4、8、12、16、24、32、48px。

## 颜色

配色方式：忠于原色，种子色 `#ff7a1a`。

| 角色 | 变量 | 浅色 | 深色 | 用在哪 |
|---|---|---|---|---|
| primary | `--md-sys-color-primary` | `#ff7a1a` | `#ffb690` | 最重要的按钮（filled）、选中状态、链接、进度条 |
| on-primary | `--md-sys-color-on-primary` | `#331200` | `#542200` | 放在 primary 上的文字和图标 |
| primary-container | `--md-sys-color-primary-container` | `#ffdbc9` | `#773300` | 要突出但不刺眼的地方：FAB、重点卡片的图片区、头像底色 |
| on-primary-container | `--md-sys-color-on-primary-container` | `#331200` | `#ffdbc9` | 放在 primary-container 上的文字和图标 |
| secondary | `--md-sys-color-secondary` | `#fbba60` | `#fbba60` | 不那么重要的元素、焦点框 |
| on-secondary | `--md-sys-color-on-secondary` | `#2a1800` | `#452b00` | 放在 secondary 上的文字和图标 |
| secondary-container | `--md-sys-color-secondary-container` | `#ffddb3` | `#633f00` | tonal 按钮、选中的 chip、分段按钮、导航指示器 |
| on-secondary-container | `--md-sys-color-on-secondary-container` | `#2a1800` | `#ffddb3` | 放在 secondary-container 上的文字和图标 |
| tertiary | `--md-sys-color-tertiary` | `#e68484` | `#ffb3b2` | 点缀色：平衡主色、标出特别的内容 |
| on-tertiary | `--md-sys-color-on-tertiary` | `#400009` | `#640a18` | 放在 tertiary 上的文字和图标 |
| tertiary-container | `--md-sys-color-tertiary-container` | `#ffdad9` | `#7f282e` | 点缀区域的底色 |
| on-tertiary-container | `--md-sys-color-on-tertiary-container` | `#400009` | `#ffdad9` | 放在 tertiary-container 上的文字和图标 |
| error | `--md-sys-color-error` | `#c00000` | `#ffb4a8` | 错误、删除、必填提示、徽标 |
| on-error | `--md-sys-color-on-error` | `#ffffff` | `#690000` | 放在 error 上的文字和图标 |
| error-container | `--md-sys-color-error-container` | `#ffdad4` | `#930000` | 错误提示框的底色 |
| on-error-container | `--md-sys-color-on-error-container` | `#410000` | `#ffdad4` | 放在 error-container 上的文字和图标 |
| surface | `--md-sys-color-surface` | `#fef8f5` | `#171210` | 页面背景 |
| on-surface | `--md-sys-color-on-surface` | `#1f1b18` | `#e7e1de` | 主要文字、标题 |
| surface-variant | `--md-sys-color-surface-variant` | `#ece0d9` | `#4f4540` | 少量需要和背景区分的区域 |
| on-surface-variant | `--md-sys-color-on-surface-variant` | `#4f4540` | `#d0c4be` | 次要文字、图标、占位文字 |
| surface-dim | `--md-sys-color-surface-dim` | `#dfd9d5` | `#171210` | 比背景暗一点的背景 |
| surface-bright | `--md-sys-color-surface-bright` | `#fef8f5` | `#3d3836` | 比背景亮一点的背景 |
| surface-container-lowest | `--md-sys-color-surface-container-lowest` | `#ffffff` | `#110d0b` | 最低一层容器 |
| surface-container-low | `--md-sys-color-surface-container-low` | `#f8f2ef` | `#1f1b18` | elevated 卡片 |
| surface-container | `--md-sys-color-surface-container` | `#f3ece9` | `#231f1c` | 导航栏、菜单 |
| surface-container-high | `--md-sys-color-surface-container-high` | `#ede7e4` | `#2e2927` | 对话框、搜索栏 |
| surface-container-highest | `--md-sys-color-surface-container-highest` | `#e7e1de` | `#393431` | filled 卡片、filled 输入框、开关轨道 |
| outline | `--md-sys-color-outline` | `#80756f` | `#9a8e89` | 输入框、outlined 按钮、分段按钮的边框 |
| outline-variant | `--md-sys-color-outline-variant` | `#d0c4be` | `#4f4540` | 分割线、outlined 卡片和 chip 的边框 |
| inverse-surface | `--md-sys-color-inverse-surface` | `#342f2d` | `#e7e1de` | 消息条、提示的底色 |
| inverse-on-surface | `--md-sys-color-inverse-on-surface` | `#f6efec` | `#342f2d` | 放在 inverse-surface 上的文字 |
| inverse-primary | `--md-sys-color-inverse-primary` | `#ffb690` | `#9b4500` | 放在 inverse-surface 上的按钮文字 |
| shadow | `--md-sys-color-shadow` | `#000000` | `#000000` | 阴影 |
| scrim | `--md-sys-color-scrim` | `#000000` | `#000000` | 弹窗后面的遮罩（用 32% 透明度） |

## 字体

- 标题字体（display / headline / title-large）：Roboto — `'Roboto','Noto Sans SC',sans-serif`
- 正文字体（其它所有）：Roboto — `'Roboto','Noto Sans SC',sans-serif`

| 类名 | 字号 / 行高 | 粗细 | 用在哪 |
|---|---|---|---|
| `.m3-display-large` | 57 / 64px | 400 | 超大的展示文字：首屏口号、大数字 |
| `.m3-display-medium` | 45 / 52px | 400 | 超大的展示文字：首屏口号、大数字 |
| `.m3-display-small` | 36 / 44px | 400 | 超大的展示文字：首屏口号、大数字 |
| `.m3-headline-large` | 32 / 40px | 400 | 页面和区块的大标题 |
| `.m3-headline-medium` | 28 / 36px | 400 | 页面和区块的大标题 |
| `.m3-headline-small` | 24 / 32px | 400 | 页面和区块的大标题 |
| `.m3-title-large` | 22 / 28px | 400 | 卡片、对话框、列表、顶部栏的标题 |
| `.m3-title-medium` | 16 / 24px | 500 | 卡片、对话框、列表、顶部栏的标题 |
| `.m3-title-small` | 14 / 20px | 500 | 卡片、对话框、列表、顶部栏的标题 |
| `.m3-body-large` | 16 / 24px | 400 | 正文、说明文字 |
| `.m3-body-medium` | 14 / 20px | 400 | 正文、说明文字 |
| `.m3-body-small` | 12 / 16px | 400 | 正文、说明文字 |
| `.m3-label-large` | 14 / 20px | 500 | 按钮、标签、导航上的小字 |
| `.m3-label-medium` | 12 / 16px | 500 | 按钮、标签、导航上的小字 |
| `.m3-label-small` | 11 / 16px | 500 | 按钮、标签、导航上的小字 |

## 形状

| 令牌 | 值 |
|---|---|
| `--md-sys-shape-corner-none` | 0px |
| `--md-sys-shape-corner-extra-small` | 4px |
| `--md-sys-shape-corner-small` | 8px |
| `--md-sys-shape-corner-medium` | 12px |
| `--md-sys-shape-corner-large` | 16px |
| `--md-sys-shape-corner-extra-large` | 28px |
| `--md-sys-shape-corner-full` | 全圆 |

每个组件用哪一级：

- 按钮、图标按钮、分段按钮、搜索栏、开关、导航指示器：`full`（全圆）→ `--md-comp-button-shape`
- 悬浮按钮 FAB：`full`（全圆）→ `--md-comp-fab-shape`
- 标签 Chip：`large`（大）→ `--md-comp-chip-shape`
- 输入框：`small`（小）→ `--md-comp-field-shape`
- 卡片：`large`（大）→ `--md-comp-card-shape`
- 对话框：`medium`（中）→ `--md-comp-dialog-shape`

## 阴影 · 密度 · 描边 · 动效

- 阴影风格：柔和。Level 0 平放，1 卡片，2 菜单/导航，3 FAB/对话框，4 悬停，5 拖动。
- 密度：4px（所有按钮、输入框、列表项的高度都会加上这个数）。
- 描边粗细：1px。
- 动效：短 100ms（悬停、按下）/ 中 250ms（展开、切换）/ 长 400ms（页面转场），缓动 `cubic-bezier(.2,0,0,1)`。
- 默认输入框样式：outlined。

## 组件

### 原子 Atoms

#### 按钮 Button

5 种，按重要程度从高到低：filled → tonal → elevated → outlined → text。一个区域里只放一个 filled 按钮。

```html
<button class="m3-btn">Filled 主要</button>
<button class="m3-btn tonal">Tonal 次要</button>
<button class="m3-btn elevated">Elevated</button>
<button class="m3-btn outlined">Outlined</button>
<button class="m3-btn text">Text 文字</button>
<button class="m3-btn" disabled>不可用</button>
```

#### 带图标的按钮 Button + icon

图标放在文字前面，18px。图标名字在 fonts.google.com/icons 里找。

```html
<button class="m3-btn"><span class="m3-icon">add</span>新建书单</button>
<button class="m3-btn tonal"><span class="m3-icon">share</span>分享</button>
<button class="m3-btn outlined"><span class="m3-icon">edit</span>编辑</button>
```

#### 图标按钮 Icon button

只有图标、没有文字的按钮。一定要写 aria-label，告诉读屏软件它是干嘛的。

```html
<button class="m3-icon-btn" aria-label="菜单"><span class="m3-icon">menu</span></button>
<button class="m3-icon-btn on" aria-label="已收藏"><span class="m3-icon">favorite</span></button>
<button class="m3-icon-btn filled" aria-label="添加"><span class="m3-icon">add</span></button>
<button class="m3-icon-btn tonal" aria-label="书签"><span class="m3-icon">bookmark</span></button>
<button class="m3-icon-btn outlined" aria-label="分享"><span class="m3-icon">share</span></button>
```

#### 悬浮按钮 FAB

页面上最重要的那一个动作，浮在右下角。一屏只放一个。

```html
<button class="m3-fab small" aria-label="添加"><span class="m3-icon">add</span></button>
<button class="m3-fab" aria-label="写书评"><span class="m3-icon">edit</span></button>
<button class="m3-fab extended"><span class="m3-icon">edit</span>写书评</button>
```

#### 标签 Chip

用来筛选、分类、或者表示已经输入的内容。选中时加 .on。

```html
<button class="m3-chip"><span class="m3-icon">star</span>推荐</button>
<button class="m3-chip on"><span class="m3-icon">check</span>小说</button>
<button class="m3-chip">科幻</button>
<span class="m3-chip">林小绿<span class="m3-icon end">close</span></span>
```

#### 复选框 · 单选 · 开关 Selection

开关是“马上生效”；复选框是“选好再提交”；单选是“几个里只能选一个”。

```html
<label class="m3-check"><input type="checkbox" checked>记住我</label>
<label class="m3-check"><input type="radio" name="fmt" checked>纸质书</label>
<label class="m3-check"><input type="radio" name="fmt">电子书</label>
<label class="m3-switch"><input type="checkbox" checked><i></i>夜间模式</label>
```

#### 滑块 · 进度 Slider · Progress

进度条用 --value 控制长度，比如 style="--value:70%"。

```html
<input class="m3-slider" type="range" value="60" aria-label="字号">
<div class="m3-progress" style="--value:40%"><i></i></div>
<div class="m3-spinner" role="progressbar" aria-label="加载中"></div>
```

#### 徽标 Badge

小红点 = 有新东西；数字 = 有几个。超过 99 写 99+。

```html
<span class="m3-badged"><span class="m3-icon">notifications</span><span class="m3-badge dot"></span></span>
<span class="m3-badged"><span class="m3-icon">mail</span><span class="m3-badge">3</span></span>
<span class="m3-badged"><span class="m3-icon">shopping_cart</span><span class="m3-badge">99+</span></span>
```

### 分子 Molecules

#### 输入框 Text field

标签会浮上去。placeholder=" " 不能删（它让标签知道框里有没有字）。出错时加 .error。outlined 线框 / filled 填充 两种。

```html
<label class="m3-field outlined"><input placeholder=" "><span>邮箱</span><small>我们不会把邮箱给别人</small></label>
<label class="m3-field outlined error"><input placeholder=" " value="lin@"><span>邮箱</span><small>邮箱格式不对</small></label>
```

#### 搜索栏 Search bar

图标 + 输入框 + 图标。

```html
<div class="m3-search"><span class="m3-icon">menu</span><input placeholder="搜书名、作者" aria-label="搜索"><span class="m3-icon">search</span></div>
```

#### 分段按钮 Segmented button

几个按钮拼成一组，只能选一个。选中的加 .on。

```html
<div class="m3-seg"><button class="on"><span class="m3-icon">check</span>全部</button><button><span class="m3-icon">check</span>未读</button><button><span class="m3-icon">check</span>收藏</button></div>
```

#### 标签页 Tabs

在同一页里切换几组内容。

```html
<div class="m3-tabs"><button class="on">新书</button><button>排行</button><button>书单</button></div>
```

#### 列表 List

头像 + 两行文字 + 右边的补充信息。

```html
<ul class="m3-list">
<li><span class="lead">林</span><div class="txt"><b>林小绿</b><span>这本书我读了三遍，每次都会哭。</span></div><span class="trail">3 分钟</span></li>
<li><span class="lead">周</span><div class="txt"><b>周一一</b><span>推荐给所有长大了的小孩。</span></div><span class="trail">1 小时</span></li>
</ul>
```

#### 菜单 Menu

点“更多”之后弹出来的选项。危险的操作放最后，用分割线隔开。

```html
<div class="m3-menu"><button><span class="m3-icon">edit</span>编辑</button><button><span class="m3-icon">share</span>分享</button><hr><button><span class="m3-icon">delete</span>删除</button></div>
```

#### 消息条 · 提示 Snackbar · Tooltip

消息条在屏幕底部出现几秒，可以带一个“撤销”。提示在鼠标停留时出现。

```html
<div class="m3-snackbar"><span>已加入购物车</span><button class="m3-btn text">撤销</button></div>
<span class="m3-tooltip">收藏这本书</span>
```

### 有机体 Organisms

#### 顶部应用栏 Top app bar

返回 + 标题 + 右边 1～3 个图标按钮。

```html
<header class="m3-topbar"><button class="m3-icon-btn" aria-label="返回"><span class="m3-icon">arrow_back</span></button><h1 class="m3-title-large title">小王子</h1><button class="m3-icon-btn on" aria-label="收藏"><span class="m3-icon">favorite</span></button><button class="m3-icon-btn" aria-label="更多"><span class="m3-icon">more_vert</span></button></header>
```

#### 底部导航栏 Navigation bar

手机 App 最下面的 3～5 个入口。当前页加 .on。

```html
<nav class="m3-navbar"><a class="on"><span class="ind"><span class="m3-icon">home</span></span>首页</a><a><span class="ind"><span class="m3-icon">search</span></span>发现</a><a><span class="ind"><span class="m3-icon">shopping_cart</span><span class="m3-badge">2</span></span>购物车</a><a><span class="ind"><span class="m3-icon">person</span></span>我的</a></nav>
```

#### 卡片 Card

三种：elevated 浮起、filled 填充、outlined 线框。一个页面里最好只用一种。

```html
<div class="m3-card elevated"><div class="media"><span class="m3-icon">menu_book</span></div><div class="content"><h3 class="m3-title-medium">小王子</h3><p class="m3-body-medium sub">圣埃克苏佩里</p><div class="actions"><button class="m3-btn text">详情</button><button class="m3-btn">购买</button></div></div></div>
<div class="m3-card filled"><div class="media secondary"><span class="m3-icon">star</span></div><div class="content"><h3 class="m3-title-medium">三体</h3><p class="m3-body-medium sub">刘慈欣</p><div class="actions"><button class="m3-btn tonal">加入书单</button></div></div></div>
<div class="m3-card outlined"><div class="media tertiary"><span class="m3-icon">favorite</span></div><div class="content"><h3 class="m3-title-medium">活着</h3><p class="m3-body-medium sub">余华</p><div class="actions"><button class="m3-btn outlined">试读</button></div></div></div>
```

#### 对话框 Dialog

打断用户、要他马上做决定时才用。按钮用 text 按钮，确认放右边。

```html
<div class="m3-dialog" role="dialog" aria-label="删除书单"><span class="m3-icon">delete</span><h3 class="m3-headline-small">删除这个书单？</h3><p>书单里的 12 本书和你的笔记会一起删掉，删了就找不回来了。</p><div class="actions"><button class="m3-btn text">取消</button><button class="m3-btn text">删除</button></div></div>
```

#### 登录表单 Sign-in form

标题 + 输入框 ×2（分子）+ 复选框 + 按钮。

```html
<form class="m3-card outlined m3-form"><h3 class="m3-headline-small">登录</h3><label class="m3-field outlined"><input placeholder=" "><span>手机号</span></label><label class="m3-field outlined"><input type="password" placeholder=" "><span>密码</span><small>至少 8 位</small></label><label class="m3-check"><input type="checkbox">记住我</label><button class="m3-btn block" type="button">登录</button><button class="m3-btn text block" type="button">忘记密码？</button></form>
```

## 一个页面的骨架

```html
<body class="m3">
  <header class="m3-topbar">…</header>
  <main style="padding:16px;display:flex;flex-direction:column;gap:16px">
    <h1 class="m3-headline-medium">页面标题</h1>
    …组件…
  </main>
  <nav class="m3-navbar">…</nav>
</body>
```

## 文件

- `design-system.css`：完整的令牌和组件样式
- `tokens.json`：所有令牌（可以导入 Figma 的 Tokens Studio 插件）
- `example.html`：双击打开，看所有组件长什么样
