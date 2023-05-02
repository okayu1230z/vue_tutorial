vue tutorialのチュートリアルを淡々とこなしていく

# quick start

https://ja.vuejs.org/guide/quick-start.html をやる

## project初期化

```bash
$ npm init vue@latest
Need to install the following packages:
  create-vue@3.6.1
Ok to proceed? (y) y

Vue.js - The Progressive JavaScript Framework

✔ Project name: … vue-tutorial
✔ Add TypeScript? … No / Yes
✔ Add JSX Support? … No / Yes
✔ Add Vue Router for Single Page Application development? … No / Yes
✔ Add Pinia for state management? … No / Yes
✔ Add Vitest for Unit Testing? … No / Yes
✔ Add an End-to-End Testing Solution? › No
✔ Add ESLint for code quality? … No / Yes

Scaffolding project in /Users/okmt/plays/vue/vue_tutorial/vue-tutorial...

Done. Now run:

  cd vue-tutorial
  npm install
  npm run dev
```

## 起動

```bash
$ npm run dev
  VITE v4.3.4  ready in 250 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h to show help
```

![vue3](./documents/vue3.png)

## CDNのvueを利用する場合

```
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
```

## ファイルの分割

index.htmlを以下のように定義する

```html
<!-- index.html -->
<div id="app"></div>

<script type="module">
  import { createApp } from 'vue'
  import MyComponent from './my-component.js'

  createApp(MyComponent).mount('#app')
</script>
```

my-component.jsは以下の通り

```javascript
export default {
  data() {
    return { count: 0 }
  },
  template: `<div>count is {{ count }}</div>`
}
```

# tutorial

https://ja.vuejs.org/tutorial/#step-1 をやる

App.vue

```vue
<template>
  <h1>Hello World!</h1>
</template>
```

## 宣言的レンダリング