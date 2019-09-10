# 头像组件集

本组件库是一些各种各样头像组件的集合。

<u-avatar></u-avatar>
<u-avatar-1 v-on:click="$router.push('components/u-avatar-1')"></u-avatar-1>
<u-avatar-2 v-on:click="$router.push('components/u-avatar-2')"></u-avatar-2>
<u-avatar-3 v-on:click="$router.push('components/u-avatar-3')"></u-avatar-3>
<u-avatar-4 v-on:click="$router.push('components/u-avatar-4')"></u-avatar-4>
<u-avatar-5 v-on:click="$router.push('components/u-avatar-5')"></u-avatar-5>
<u-avatar-7 v-on:click="$router.push('components/u-avatar-7')"></u-avatar-7>

## 准备

### 安装

``` shell
npm i --save @proto-ui/u-avatar-5.vue
```

### 引入

直接注册

``` js
import UAvatar from '@proto-ui/u-avatar-5.vue';

Vue.component('u-avatar', UAvatar);
```

或者使用 vusion-utils 安装（常用于同时安装多个组件）

``` js
import { install } from 'vusion-utils';
import UAvatar from '@proto-ui/u-avatar-5.vue';

install(Vue, { UAvatar });
```

### 使用

使用时，记得将示例中的组件名替换成你在项目中实际注册的组件名。

``` html
<u-avatar-5></u-avatar-5> 王小明
```
