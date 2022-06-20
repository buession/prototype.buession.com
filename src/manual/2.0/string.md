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
| [repeat](string.html#isobjectobj-any)                       | 重复一个字符串        |
| [left](string.html#isobjectobj-any)                       | 截取字符串左边边指定数目的字符串        |
| [right](string.html#isobjectobj-any)                       | 截取字符串右边指定数目的字符串        |
| [truncation](string.html#isobjectobj-any)                       | 截取字符串，超出部分用 truncation 替代        |
| [ltrim](string.html#isobjectobj-any)                       | 删除字符串开头的空白字符        |
| [rtrim](string.html#isobjectobj-any)                       | 删除字符串结尾的空白字符        |


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


### **repeat(count: number)**
* 类型：`Function`

* 功能描述：重复一个字符串

* 参数：count - `number` 重复次数

* 返回值：`string` 重复后的字符串

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "A".repeat(3); // AAA
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
    const result: string = "Abc".repeat(3) // AbcAbcAbc
  }
});
</script>
```


### **left(length: number)**
* 类型：`Function`

* 功能描述：截取字符串左边边指定数目的字符串

* 参数：length - `number` 截取长度

* 返回值：`string` 子字符串，length 如果为负数，则返回空字符串

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "Abc".left(1); // A
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
    const result: string = "Abc".left(-1) // ""
  }
});
</script>
```


### **right(length: number)**
* 类型：`Function`

* 功能描述：截截取字符串右边指定数目的字符串

* 参数：length - `number` 截取长度

* 返回值：`string` 子字符串，length 如果为负数，则返回空字符串

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "Abc".right(1); // c
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
    const result: string = "Abc".right(-1) // ""
  }
});
</script>
```


### **truncation(length: number, truncation: string)**
* 类型：`Function`

* 功能描述：截取字符串，超出部分用 truncation 替代

* 参数：length - `number` 截取长度
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;truncation - `string` 替换字符串

* 返回值：`string` 截取后的字符串；实际截取长度：当 length 小于等于 truncation 的长度时为，length；当 length 大于 truncation 的长度时为，length - truncation.length

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = "Abc".truncation(1, "..."); // A...
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
    const result: string = "Abc".truncation(6, "...") // Abc
  }
});
</script>
```


### **ltrim()**
* 类型：`Function`

* 功能描述：删除字符串开头的空白字符（包括：空格、制表位、换行以及其它非打印字符）

* 参数：无

* 返回值：`string` 删除了字符串最左边的空白字符的字符串

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = " Abc".ltrim(); // "Abc"
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
    const result: string = new String(" Abc ").isEmpty() // "Abc "
  }
});
</script>
```


### **rtrim()**
* 类型：`Function`

* 功能描述：删除字符串结尾的空白字符（包括：空格、制表位、换行以及其它非打印字符）

* 参数：无

* 返回值：`string` 删除了字符串最右边的空白字符的字符串

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = " Abc".rtrim(); // " Abc"
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
    const result: string = new String(" Abc ").isEmpty() // " Abc"
  }
});
</script>
```