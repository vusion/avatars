# UAvatar1 头像

<s-component-labels :labels="[
    'UI 组件', '行内展示',
]"></s-component-labels>

[![NPM Version][npm-img]][npm-url]
[![NPM Download][download-img]][download-url]

[npm-img]: http://img.shields.io/npm/v/@proto-ui/u-avatar-1.vue.svg?style=flat-square
[npm-url]: http://npmjs.org/package/@proto-ui/u-avatar-1.vue
[download-img]: https://img.shields.io/npm/dm/@proto-ui/u-avatar-1.vue.svg?style=flat-square
[download-url]: https://npmjs.org/package/@proto-ui/u-avatar-1.vue

顶部导航栏或页面中局部使用的用户头像。扩展自 [Proto UI 的 UAvatar 组件](https://vusion.github.io/proto-ui/components/u-avatar)。

<u-linear-layout gap="small">
    <u-avatar-1></u-avatar-1>
    <u-avatar-1 type="female"></u-avatar-1>
</u-linear-layout>

## 准备

### 安装

``` shell
npm i --save @proto-ui/u-avatar-1.vue
```

### 引入

直接注册

``` js
import UAvatar from '@proto-ui/u-avatar-1.vue';

Vue.component('u-avatar', UAvatar);
```

或者使用 vusion-utils 安装（常用于同时安装多个组件）

``` js
import { install } from 'vusion-utils';
import UAvatar from '@proto-ui/u-avatar-1.vue';

install(Vue, { UAvatar });
```

### 使用

使用时，记得将示例中的组件名替换成你在项目中实际注册的组件名。

## 示例
### 基本用法

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-1></u-avatar-1> 王小明</div>
    <div><u-avatar-1 type="female"></u-avatar-1> 李小雪</div>
</u-linear-layout>
```

### 大小扩展

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-1 size="mini"></u-avatar-1> 王小明（迷你）</div>
    <div><u-avatar-1 size="small"></u-avatar-1> 王小明（小）</div>
    <div><u-avatar-1></u-avatar-1> 王小明（正常）</div>
    <div><u-avatar-1 size="large"></u-avatar-1> 王小明（大）</div>
    <div><u-avatar-1 size="huge"></u-avatar-1> 王小明（大）</div>
</u-linear-layout>
```

### 自定义图片

``` html
<u-avatar-1><img src="~proto-ui.vusion/src/components/u-avatar.vue/assets/music.png"></u-avatar-1> 多多
```

### 配合 UBadge 使用

```html
<u-badge :value="3" corner dot>
    <u-avatar-1></u-avatar-1>
</u-badge>
<br/><br/>
<u-badge :value="3" corner dot>
    <u-avatar-1 type="female"></u-avatar-1>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-1></u-avatar-1>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-1 type="female"></u-avatar-1>
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
            <u-avatar-1></u-avatar-1> 王小明
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
        <span slot="title"><u-avatar-1></u-avatar-1> 王小明</span>
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
        <span slot="title"><u-badge :value="120" :max="99" corner><u-avatar-1></u-avatar-1></u-badge> 王小明</span>
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
| type | String | `'male'` | 类型。可选值：`male`, `female` |
| shape | String | `'circle'` | 形状。可选值：`circle`, `square` |
| size | String | `'normal'` | 头像大小。可选值：`'mini'`、`'small'`、`'normal'`、`'large'`、`'huge'`。如需自定义大小，可以直接设置`style="width: 40px; height: 40px;"` |

### Slots

#### (default)

添加自定义图片或内容。

