# String 参考手册


### 方法

|  方法                                                          | 描述                           |
|  ----                                                         | ----                           |
| [exists](string.html#typeobj-any)                               | 判断字符串是否存在                 |
| [equals](string.html#rawtypeobj-any)                         | 判断字符串是否相等              |
| [equalsIgnoreCase](string.html#isobjectobj-any)                       | 判断字符串是否相等，不考虑大小写        |
| [isEmpty](string.html#isobjectobj-any)                       | 判断是否为空字符串        |
| [isNotEmpty](string.html#isobjectobj-any)                       | 判断是否不为空字符串        |
| [isBlank](string.html#isobjectobj-any)                       | 判断是否为空白字符串        |


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


### **equals(str: string | undefined | null)**
* 类型：`Function`

* 功能描述：判断字符串是否相等

* 参数：str - `string | undefined | null` 与此 String 进行比较的对象

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


### **equalsIgnoreCase(str: string | undefined | null)**
* 类型：`Function`

* 功能描述：判断字符串是否相等，不考虑大小写

* 参数：str - `string | undefined | null` 与此 String 进行比较的对象

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


### **isEmpty()**
* 类型：`Function`

* 功能描述：判断是否为空字符串

* 参数：无

* 返回值：`boolean` 字符串为空，即长度为 0 返回 true；否则，返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = " ".isEmpty(); // false
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
    const result: boolean = new String("").isEmpty() // true
  }
});
</script>
```


### **isNotEmpty()**
* 类型：`Function`

* 功能描述：判断是否不为空字符串

* 参数：无

* 返回值：`boolean` 字符串不为空，即长度大于 0 返回 true；否则，返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = " ".isNotEmpty(); // true
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
    const result: boolean = new String("").isNotEmpty() // false
  }
});
</script>
```


### **isBlank()**
* 类型：`Function`

* 功能描述：判断是否为空白字符串

* 参数：无

* 返回值：`boolean` 字符串全为空白字符串（即：空格、回车、Tag 制表位、非打印字符）返回 true；否则，返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = " ".isBlank(); // true
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
    const result: boolean = new String("\t\n").isBlank() // true
  }
});
</script>
```