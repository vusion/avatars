# UAvatar6 头像

<s-component-labels :labels="[
    'UI 组件', '行内展示',
]"></s-component-labels>

[![NPM Version][npm-img]][npm-url]
[![NPM Download][download-img]][download-url]

[npm-img]: http://img.shields.io/npm/v/@proto-ui/u-avatar-6.vue.svg?style=flat-square
[npm-url]: http://npmjs.org/package/@proto-ui/u-avatar-6.vue
[download-img]: https://img.shields.io/npm/dm/@proto-ui/u-avatar-6.vue.svg?style=flat-square
[download-url]: https://npmjs.org/package/@proto-ui/u-avatar-6.vue

顶部导航栏或页面中局部使用的用户头像。扩展自 [Proto UI 的 UAvatar 组件](https://vusion.github.io/proto-ui/u-avatar)。

<u-linear-layout gap="small">
    <u-avatar-6></u-avatar-6>
    <u-avatar-6 shape="square"></u-avatar-6>
</u-linear-layout>

## 示例
### 基本用法

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-6></u-avatar-6> 王小明</div>
</u-linear-layout>
```

### 大小扩展

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-6 size="mini"></u-avatar-6> 王小明（迷你）</div>
    <div><u-avatar-6 size="small"></u-avatar-6> 王小明（小）</div>
    <div><u-avatar-6></u-avatar-6> 王小明（正常）</div>
    <div><u-avatar-6 size="large"></u-avatar-6> 王小明（大）</div>
    <div><u-avatar-6 size="huge"></u-avatar-6> 王小明（大）</div>
</u-linear-layout>
```

### 自定义图片

``` html
<u-avatar-6><img src="~proto-ui.vusion/src/components/u-avatar.vue/assets/music.png"></u-avatar-6> 多多
```

### 配合 UBadge 使用

```html
<u-badge :value="3" corner dot>
    <u-avatar-6></u-avatar-6>
</u-badge>
<br/><br/>
<u-badge :value="3" corner dot>
    <u-avatar-6 shape="square"></u-avatar-6>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-6></u-avatar-6>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-6 shape="square"></u-avatar-6>
</u-badge>
```

### 配合 UNavbar 使用

``` html
<u-navbar>
    <u-navbar-item to="/components">组件</u-navbar-item>
    <u-navbar-item>概念</u-navbar-item>
    <u-navbar-item disabled>指令</u-navbar-item>
    <u-navbar-divider></u-navbar-divider>
    <u-navbar-item>配置</u-navbar-item>
    <div slot="right">
        <u-navbar-item>
            <u-avatar-6></u-avatar-6> 王小明
        </u-navbar-item>
    </div>
</u-navbar>
```

``` html
<u-navbar>
    <u-navbar-item to="/components">组件</u-navbar-item>
    <u-navbar-item>概念</u-navbar-item>
    <u-navbar-item disabled>指令</u-navbar-item>
    <u-navbar-divider></u-navbar-divider>
    <u-navbar-item>配置</u-navbar-item>
    <u-navbar-dropdown slot="right">
        <span slot="title"><u-avatar-6></u-avatar-6> 王小明</span>
        <u-navbar-menu>
            <u-navbar-menu-item>Basic</u-navbar-menu-item>
            <u-navbar-menu-item>Layout</u-navbar-menu-item>
            <u-navbar-menu-item>Navigation</u-navbar-menu-item>
        </u-navbar-menu>
    </u-navbar-dropdown>
</u-navbar>
```

``` html
<u-navbar>
    <u-navbar-item to="/components">组件</u-navbar-item>
    <u-navbar-item>概念</u-navbar-item>
    <u-navbar-item disabled>指令</u-navbar-item>
    <u-navbar-divider></u-navbar-divider>
    <u-navbar-item>配置</u-navbar-item>
    <u-navbar-dropdown slot="right">
        <span slot="title"><u-badge :value="120" :max="99" corner><u-avatar-6></u-avatar-6></u-badge> 王小明</span>
        <u-navbar-menu>
            <u-navbar-menu-item>Basic</u-navbar-menu-item>
            <u-navbar-menu-item>Layout</u-navbar-menu-item>
            <u-navbar-menu-item>Navigation</u-navbar-menu-item>
        </u-navbar-menu>
    </u-navbar-dropdown>
</u-navbar>
```

## API

### Props/Attrs

| Prop/Attr | Type | Default | Description |
| --------- | ---- | ------- | ----------- |
| shape | String | `'circle'` | 形状。可选值：`circle`, `square` 两种类型 |
| size | String | `'normal'` | 头像大小。可选值：`'mini'`、`'small'`、`'normal'`、`'large'`、`'huge'`。如需自定义大小，可以直接设置`style="width: 40px; height: 40px;"` |

### Slots

#### (default)

添加自定义图片或内容。
