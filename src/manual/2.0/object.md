# Object 参考手册


### 方法

|  方法                                                          | 描述                           |
|  ----                                                         | ----                           |
| [type](object.html#typeobj-any)                               | 获取对象数据类型                 |
| [rawType](object.html#rawtypeobj-any)                         | 获取对象原始数据类型              |
| [isObject](object.html#isobjectobj-any)                       | 判断对象是否为 object 类型        |
| [isPlainObject](object.html#isplainobjectobj-any)             | 判断对象是否为简单 object 类型    |
| [isMap](object.html#ismapobj-any)                             | 判断对象是否为 Map 类型           |
| [isSet](object.html#issetobj-any)                             | 判断对象是否为 Set 类型           |
| [isSymbol](object.html#issymbolobj-any)                       | 判断对象是否为 Symbol            |
| [isPromise](object.html#ispromiseobj-any)                     | 判断对象是否为 Promise           |
| [isPrimitive](object.html#isprimitiveobj-any)                 | 判断对象是否为原始类型            |
| [isFunction](object.html#isfunctionobj-any)                   | 判断对象是否为函数                |
| [isArray](object.html#isarrayobj-any)                         | 判断对象是否为数组                |
| [isString](object.html#isstringobj-any)                       | 判断对象是否为字符串对象           |
| [isNumber](object.html#isnumberobj-any)                       | 判断对象是否为数字对象             |
| [isBoolean](object.html#isbooleanobj-any)                     | 判断对象是否为布尔对象             |
| [isRegExp](object.html#isregexpobj-any)                       | 判断对象是否为正则对象             |
| [isFile](object.html#isfileobj-any)                           | 判断对象是否为文件对象             |
| [isWindow](object.html#iswindowobj-any)                       | 判断对象是否为 windows 对象        |
| [isElement](object.html#iselementobj-any)                     | 判断对象是否为 Element            |
| [isEvent](object.html#iseventobj-any)                         | 判断对象是否为事件对象             |
| [isNull](object.html#isnullobj-any)                           | 判断对象是否为 null 对象           |
| [isUndefined](object.html#isundefinedobj-any)                 | 判断对象是否为未定义               |
| [isUndefinedOrNull](object.html#isundefinedornullobj-any)     | 判断对象是否为未定义或 null        |
| [clone](object.html#cloneobj-any)                             | 克隆对象                         |


---


### **type(obj: any)**
* 类型：`Function`

* 功能描述：获取对象数据类型

* 参数：obj - `any` 对象变量

* 返回值：`string` 对象数据类型

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.type(true); // boolean
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
    const result: string = Object.type(4.4) // number
  }
});
</script>
```


### **rawType(obj: any)**
* 类型：`Function`

* 功能描述：获取对象原始数据类型

* 参数：obj - `any` 对象变量

* 返回值：`string` 原始数据类型

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.type("4.4"); // String
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
    const result: string = Object.type(4.4) // Number
  }
});
</script>
```


### **isObject(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 object 类型

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为 object 类型返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isObject("1"); // false
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
    const result: boolean = Object.isObject(new String("1")) // true
  }
});
</script>
```


### **isPlainObject(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为简单 object 类型

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为简单 object 类型返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isPlainObject(new String("1")); // false
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
    const result: boolean = Object.isPlainObject({"a":"A"}) // true
  }
});
</script>
```


### **isMap(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 Map 类型

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为 Map 类型返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isMap(new Map()); // true
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
    const result: boolean = Object.isMap({"a":"A"}) // false
  }
});
</script>
```


### **isSet(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 Map 类型

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为 Set 类型返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isSet(new Set()); // true
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
    const result: boolean = Object.isSet({"a":"A"}) // false
  }
});
</script>
```


### **isSymbol(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 Symbol

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为 Symbol 返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isSymbol(new Set()); // true
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
    const result: boolean = Object.isSymbol({"a":"A"}) // false
  }
});
</script>
```


### **isPromise(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 Promise

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为 Promise 返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isPromise(new Set()); // true
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
    const result: boolean = Object.isPromise({"a":"A"}) // false
  }
});
</script>
```


### **isPrimitive(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为原始类型

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为原始类型返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isPrimitive(new Set()); // true
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
    const result: boolean = Object.isPromise({"a":"A"}) // false
  }
});
</script>
```


### **isFunction(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为函数

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为函数返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isFunction(new Set()); // true
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
    const result: boolean = Object.isFunction({"a":"A"}) // false
  }
});
</script>
```


### **isArray(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为数组

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为数组返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isArray(new Set()); // true
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
    const result: boolean = Object.isArray({"a":"A"}) // false
  }
});
</script>
```


### **isString(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为字符串对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为字符串返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isString(new Set()); // true
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
    const result: boolean = Object.isString({"a":"A"}) // false
  }
});
</script>
```


### **isNumber(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为数字对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为数字对象返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isNumber(new Set()); // true
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
    const result: boolean = Object.isNumber({"a":"A"}) // false
  }
});
</script>
```


### **isBoolean(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为布尔对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象为布尔对象返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isBoolean(new Set()); // true
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
    const result: boolean = Object.isBoolean({"a":"A"}) // false
  }
});
</script>
```


### **isRegExp(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为正则对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为正则对象返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isRegExp(new Set()); // true
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
    const result: boolean = Object.isRegExp({"a":"A"}) // false
  }
});
</script>
```


### **isFile(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为文件对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为文件对象返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isFile(new Set()); // true
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
    const result: boolean = Object.isFile({"a":"A"}) // false
  }
});
</script>
```


### **isWindow(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 windows 对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为 windows 对象返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isWindow(new Set()); // true
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
    const result: boolean = Object.isWindow({"a":"A"}) // false
  }
});
</script>
```


### **isElement(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 Element

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为 Element 返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isElement(new Set()); // true
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
    const result: boolean = Object.isElement({"a":"A"}) // false
  }
});
</script>
```


### **isEvent(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为事件对象

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为事件对象返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isEvent(new Set()); // true
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
    const result: boolean = Object.isEvent({"a":"A"}) // false
  }
});
</script>
```


### **isNull(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为 null

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为 null 返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isNull(new Set()); // true
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
    const result: boolean = Object.isNull({"a":"A"}) // false
  }
});
</script>
```


### **isUndefined(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为未定义

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为未定义返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isUndefined(new Set()); // true
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
    const result: boolean = Object.isUndefined({"a":"A"}) // false
  }
});
</script>
```


### **isUndefinedOrNull(obj: any)**
* 类型：`Function`

* 功能描述：判断对象是否为未定义或 null

* 参数：obj - `any` 对象变量

* 返回值：`boolean` 对象是否为未定义或 null 返回 true；否则返回 false

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.isUndefinedOrNull(new Set()); // true
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
    const result: boolean = Object.isUndefinedOrNull({"a":"A"}) // false
  }
});
</script>
```


### **clone(obj: any)**
* 类型：`Function`

* 功能描述：克隆对象

* 参数：obj - `any` 对象变量

* 返回值：`any` 新对象实例

示例：

原生 JavaScript
```javascript
<script type="text/javascript">
  var result = Object.clone(new Set()); // true
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
    const result: any = Object.clone({"a":"A"}) // false
  }
});
</script>
```