# [Plus](https://www.npmjs.com/package/@h5plus/core)

[![](https://img.shields.io/npm/l/@h5plus/core.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/core) [![](https://img.shields.io/npm/v/@h5plus/core.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/core) [![](https://img.shields.io/npm/dm/@h5plus/core.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/core)

> `设备相关的常用api`

### 安装

```bash
npm install @h5plus/core --save

yarn add @h5plus/core
```

### 基本使用

```javascript
import Vue from 'vue'
import plus from '@h5plus/core'
Vue.use(plus)
```

> `其方法中的this指向组件`

#### - event Vue 选项

`Events模块管理客户端事件，包括系统事件，如扩展API加载完毕、程序前后台切换等。`

1.  "plusready": 扩展 API 加载完成事件
1.  "pause": 运行环境从前台切换到后台事件
1.  "resume": 运行环境从后台切换到前台事件
1.  "netchange": 设备网络状态变化事件
1.  "newintent": 新意图事件
1.  "plusscrollbottom": 窗口滚动到底部事件
1.  "error": 页面加载错误事件
1.  "background": 应用切换到后台运行事件
1.  "foreground": 应用切换到前台运行事件
1.  "trimmemory": 应用需要清理内存事件
1.  "splashclosed": 应用启动界面已关闭事件

#### - listener Vue 选项

`用于监听自定义的事件广播`

#### - $api

> `全局window中扩展$api，包含常用api，与设备无关的`

#### - $plus

> `全局window中扩展$plus，包含设备相关的api`

#### - 示例

```javascript
export default {
  name: 'app',
  // Events模块管理客户端事件，包括系统事件，如扩展API加载完毕、程序前后台切换等。
  // "plusready": 扩展API加载完成事件
  // "pause": 运行环境从前台切换到后台事件
  // "resume": 运行环境从后台切换到前台事件
  // "netchange": 设备网络状态变化事件
  // "newintent": 新意图事件
  // "plusscrollbottom": 窗口滚动到底部事件
  // "error": 页面加载错误事件
  // "background": 应用切换到后台运行事件
  // "foreground": 应用切换到前台运行事件
  // "trimmemory": 应用需要清理内存事件
  // "splashclosed": 应用启动界面已关闭事件
  event: {
    // plusready，设备加载完成
    plusready() {
      console.log('test组件 设备加载完成')
    }
  },
  // 自定义窗体监听选项
  listener: {
    // “customEvent”为事件名称
    customEvent(e) {
      // e.detail：事件传递的数据
      alert('test:' + JSON.stringify(e.detail))
    }
  },
  methods: {
    // 广播消息 
    send: function() {
      $plus.msg.send('customEvent', { a: 1 }, { self: true })
    }
  }
}
```

### 自定义扩展

```javascript
import Vue from 'vue'
import plus from 'h5pa-vue'
Vue.use(plus, {
  // 全局指定hbuild的错误页地址
  errorPage: '/error.html',
  // 是否需要模拟
  isSim: true
})
```

### 参考

- [Vue2 中文](https://cn.vuejs.org/v2/guide/index.html)
- [html5plus](http://www.html5plus.org/doc/h5p.html)

# [Api](https://www.npmjs.com/package/@h5plus/api)

[![](https://img.shields.io/npm/l/@h5plus/api.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/api) [![](https://img.shields.io/npm/v/@h5plus/api.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/api) [![](https://img.shields.io/npm/dm/@h5plus/api.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/api)

> `与设备无关的常用api`

### 安装

```shell
npm install @h5plus/api --save
yarn add @h5plus/api
```

### 基本使用

```javascript
import '@h5plus/api'
```

### 参考

- [decimal.js](https://github.com/MikeMcl/decimal.js)
- [accounting.js](https://github.com/openexchangerates/accounting.js)
- [validator.js](https://github.com/chriso/validator.js)
- [color](https://github.com/Qix-/color)
- [qs](https://github.com/ljharb/qs)
- [linqjs](https://github.com/joaom182/linqjs)


# [Persist](https://www.npmjs.com/package/@h5plus/persist)

[![](https://img.shields.io/npm/l/@h5plus/persist.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/persist) [![](https://img.shields.io/npm/v/@h5plus/persist.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/persist) [![](https://img.shields.io/npm/dm/@h5plus/persist.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/persist)

> `基于Vuex的持久化保存，加入了HTML5+ 的 plus.storage 支持`

# [Touch](https://www.npmjs.com/package/@h5plus/touch)

[![](https://img.shields.io/npm/l/@h5plus/touch.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/touch) [![](https://img.shields.io/npm/v/@h5plus/touch.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/touch) [![](https://img.shields.io/npm/dm/@h5plus/touch.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/touch)

> `基于Vue的touch插件`

# [Bus](https://www.npmjs.com/package/@h5plus/bus)

[![](https://img.shields.io/npm/l/@h5plus/bus.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/bus) [![](https://img.shields.io/npm/v/@h5plus/bus.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/bus) [![](https://img.shields.io/npm/dm/@h5plus/bus.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/bus)

> `基于Vue的事件总线`

# [img-ui](https://www.npmjs.com/package/@h5plus/img-ui)

[![](https://img.shields.io/npm/l/@h5plus/img-ui.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/img-ui) [![](https://img.shields.io/npm/v/@h5plus/img-ui.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/img-ui) [![](https://img.shields.io/npm/dm/@h5plus/img-ui.svg?style=flat-square)](https://www.npmjs.com/package/@h5plus/img-ui)

> `跟图像有关的组件,例如二维码、html保存图片等`
