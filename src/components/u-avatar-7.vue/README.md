# UAvatar7 头像

顶部导航栏或页面中局部使用的用户头像。

## 准备

### 安装

``` shell
npm i --save @proto-ui/u-avatar-7.vue
```

### 引入

直接注册

``` js
import UAvatar from '@proto-ui/u-avatar-7.vue';

Vue.component('u-avatar', UAvatar);
```

或者使用 vusion-utils 安装

``` js
import { install } from 'vusion-utils';
import UAvatar from '@proto-ui/u-avatar-7.vue';

install(Vue, { UAvatar });
```

## 示例
### 基本用法

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-7></u-avatar-7> 云小明</div>
</u-linear-layout>
```

### 大小扩展

``` html
<u-linear-layout direction="vertical">
    <div><u-avatar-7 size="mini"></u-avatar-7> 云小明（迷你）</div>
    <div><u-avatar-7 size="small"></u-avatar-7> 云小明（小）</div>
    <div><u-avatar-7></u-avatar-7> 云小明（正常）</div>
    <div><u-avatar-7 size="large"></u-avatar-7> 云小明（大）</div>
    <div><u-avatar-7 size="huge"></u-avatar-7> 云小明（大）</div>
</u-linear-layout>
```

### 配合 UBadge 使用

```html
<u-badge :value="3" corner dot>
    <u-avatar-7></u-avatar-7>
</u-badge>
<br/><br/>
<u-badge :value="3" corner dot>
    <u-avatar-7 shape="square"></u-avatar-7>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-7></u-avatar-7>
</u-badge>
<br/><br/>
<u-badge :value="120" :max="99" corner>
    <u-avatar-7 shape="square"></u-avatar-7>
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
            <u-avatar-7></u-avatar-7> 云小明
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
        <span slot="title"><u-avatar-7></u-avatar-7> 云小明</span>
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
        <span slot="title"><u-badge :value="120" :max="99" corner><u-avatar-7></u-avatar-7></u-badge> 云小明</span>
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
| size | String | `'normal'` | 头像大小。可选值：`'mini'`、`'small'`、`'normal'`、`'large'`、`'huge'`。如需自定义大小，可以直接设置`style="width: 40px; height: 40px;"` |
| shape | String | `'circle'` | 形状。可选值：`circle`, `square` 两种类型 |

### Slots

#### (default)

无
