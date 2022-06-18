# String 参考手册


### 方法

|  方法                                                          | 描述                           |
|  ----                                                         | ----                           |
| [exists](string.html#typeobj-any)                               | 判断字符串是否存在                 |
| [equals](string.html#rawtypeobj-any)                         | 判断字符串是否相等，不考虑大小写              |
| [equalsIgnoreCase](string.html#isobjectobj-any)                       | 判断对象是否为 object 类型        |


---


### **exists(str: string)**
* 类型：`Function`

* 功能描述：判断字符串是否存在

* 参数：str - `string` 子字符串

* 返回值：`boolean` 子字符串存在返回 true；否则，返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "ABC".exists("A"); // true
</script>
```

vue
```html
<template>
  <div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  setup() {
    const result: boolean = "ABC".exists("a") // false
  }
});
</script>
```


### **equals(str: string)**
* 类型：`Function`

* 功能描述：判断字符串是否相等

* 参数：str - `string` 与此 String 进行比较的对象

* 返回值：`boolean` 字符串相等返回 true；否则，返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "A".equals(new String("A")); // true
</script>
```

vue
```html
<template>
  <div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  setup() {
    const result: boolean = "A".equals("a") // false
  }
});
</script>
```


### **equalsIgnoreCase(str: string)**
* 类型：`Function`

* 功能描述：判断字符串是否相等，不考虑大小写

* 参数：str - `string` 与此 String 进行比较的对象

* 返回值：`boolean` 字符串相等返回 true；否则，返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "A".equalsIgnoreCase("a"); // true
</script>
```

vue
```html
<template>
  <div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  setup() {
    const result: boolean = new String("a").equalsIgnoreCase("1") // false
  }
});
</script>
```