# วิธีทำ Global properties ใน Vue.js Version 3

## ใส่ในไฟล์ `main.js`
```javascript
// Version 2
import { Vue } from 'vue';
...
Vue.prototype.$testProperties = "test";


// Version 3
import { createApp } from 'vue';
import App from './App.vue';
...
const app = createApp(App);
app.config.globalProperties.$testProperties = "test";

app.use(router).mount('#app')
```

## วิธีเรียกใช้
```javascript
// Version 2
export default {
  mounted() {
    console.log(this.$testProperties);
    // Output: test
  },
}

// Version 3
export default {
  mounted() {
    console.log(this.$testProperties);
    // Output: test
  },
}
```
