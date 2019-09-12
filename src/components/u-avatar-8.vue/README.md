# UAvatar8 头像

<s-component-labels :labels="[
    'UI 组件', '行内展示',
]"></s-component-labels>

[![NPM Version][npm-img]][npm-url]
[![NPM Download][download-img]][download-url]

[npm-img]: http://img.shields.io/npm/v/@proto-ui/u-avatar-8.vue.svg?style=flat-square
[npm-url]: http://npmjs.org/package/@proto-ui/u-avatar-8.vue
[download-img]: https://img.shields.io/npm/dm/@proto-ui/u-avatar-8.vue.svg?style=flat-square
[download-url]: https://npmjs.org/package/@proto-ui/u-avatar-8.vue

顶部导航栏或页面中局部使用的用户头像。扩展自 [Proto UI 的 UAvatar 组件](https://vusion.github.io/proto-ui/components/u-avatar)。

<u-linear-layout gap="small" direction="vertical">
    <u-linear-layout gap="small">
        <u-avatar-8 size="huge"></u-avatar-8>
        <u-avatar-8 size="huge" type="2"></u-avatar-8>
        <u-avatar-8 size="huge" type="3"></u-avatar-8>
        <u-avatar-8 size="huge" type="4"></u-avatar-8>
    </u-linear-layout>
    <u-linear-layout gap="small">
        <u-avatar-8 size="huge" type="5"></u-avatar-8>
        <u-avatar-8 size="huge" type="6"></u-avatar-8>
        <u-avatar-8 size="huge" type="7"></u-avatar-8>
        <u-avatar-8 size="huge" type="8"></u-avatar-8>
    </u-linear-layout>
    <u-linear-layout gap="small">
        <u-avatar-8 size="huge" type="9"></u-avatar-8>
        <u-avatar-8 size="huge" type="10"></u-avatar-8>
        <u-avatar-8 size="huge" type="11"></u-avatar-8>
        <u-avatar-8 size="huge" type="12"></u-avatar-8>
    </u-linear-layout>
    <u-linear-layout gap="small">
        <u-avatar-8 size="huge" type="13"></u-avatar-8>
        <u-avatar-8 size="huge" type="14"></u-avatar-8>
        <u-avatar-8 size="huge" type="15"></u-avatar-8>
        <u-avatar-8 size="huge" type="16"></u-avatar-8>
    </u-linear-layout>
</u-linear-layout>

## 准备

### 安装

``` shell
npm i --save @proto-ui/u-avatar-8.vue
```

### 引入

直接注册

``` js
import UAvatar from '@proto-ui/u-avatar-8.vue';

Vue.component('u-avatar', UAvatar);
```

或者使用 vusion-utils 安装

``` js
import { install } from 'vusion-utils';
import UAvatar from '@proto-ui/u-avatar-8.vue';

install(Vue, { UAvatar });
```

## 示例
### 基本用法

``` html
<u-linear-layout direction="vertical">
    <u-linear-layout gap="small">
        <span><u-avatar-8></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="2"></u-avatar-8> 李小雪</span>
        <span><u-avatar-8 type="3"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="4"></u-avatar-8> 李小雪</span>
    </u-linear-layout>
    <u-linear-layout gap="small">
        <span><u-avatar-8 type="5"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="6"></u-avatar-8> 李小雪</span>
        <span><u-avatar-8 type="7"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="8"></u-avatar-8> 李小雪</span>
    </u-linear-layout>
    <u-linear-layout gap="small">
        <span><u-avatar-8 type="9"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="10"></u-avatar-8> 李小雪</span>
        <span><u-avatar-8 type="11"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="12"></u-avatar-8> 李小雪</span>
    </u-linear-layout>
    <u-linear-layout gap="small">
        <span><u-avatar-8 type="13"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="14"></u-avatar-8> 李小雪</span>
        <span><u-avatar-8 type="15"></u-avatar-8> 王小明</span>
        <span><u-avatar-8 type="16"></u-avatar-8> 李小雪</span>
    </u-linear-layout>
</u-linear-layout>
```

### 大小扩展

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-8 size="mini"></u-avatar-8> 王小明（迷你）</div>
    <div><u-avatar-8 size="small"></u-avatar-8> 王小明（小）</div>
    <div><u-avatar-8></u-avatar-8> 王小明（正常）</div>
    <div><u-avatar-8 size="large"></u-avatar-8> 王小明（大）</div>
    <div><u-avatar-8 size="huge"></u-avatar-8> 王小明（大）</div>
</u-linear-layout>
```

### 自定义图片

``` html
<u-avatar-8><img src="~proto-ui.vusion/src/components/u-avatar.vue/assets/music.png"></u-avatar-8> 多多
```

### 配合 UBadge 使用

```html
<u-badge :value="3" corner dot>
    <u-avatar-8></u-avatar-8>
</u-badge>
<br/><br/>
<u-badge :value="3" corner dot>
    <u-avatar-8></u-avatar-8>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-8></u-avatar-8>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-8></u-avatar-8>
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
            <u-avatar-8></u-avatar-8> 王小明
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
        <span slot="title"><u-avatar-8></u-avatar-8> 王小明</span>
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
        <span slot="title"><u-badge :value="120" :max="99" corner><u-avatar-8></u-avatar-8></u-badge> 王小明</span>
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
| type | String | `'boy'` | 头像类型。请参考上面的示例 |
| shape | String | `'circle'` | 形状。可选值：`circle`, `square` 两种类型 |
| size | String | `'normal'` | 头像大小。可选值：`'mini'`、`'small'`、`'normal'`、`'large'`、`'huge'`。如需自定义大小，可以直接设置`style="width: 40px; height: 40px;"` |

### Slots

#### (default)

添加自定义图片或内容。
