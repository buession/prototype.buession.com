# Object 参考手册


### 方法

|  方法                                                                 | 描述                           |
|  ----                                                                | ----                           |
| [type](object.html#topaddedstringlength-number,-radix-number)        | 获取对象数据类型                  |
| [rawType](object.html#isoddnum-number)                               | 获取对象原始数据类型              |
| [isObject](object.html#isevennum-number)                             | 判断对象是否为 object 类型        |
| [isPlainObject](object.html#isevennum-number)                        | 判断对象是否为简单 object 类型     |
| [isMap](object.html#isevennum-number)                        | 判断对象是否为 Map 类型     |
| [isSet](object.html#isevennum-number)                        | 判断对象是否为 Set 类型     |
| [isSymbol](object.html#isevennum-number)                        | 判断对象是否为 Symbol     |
| [isPromise](object.html#isevennum-number)                        | 判断对象是否为 Promise     |
| [isPrimitive](object.html#isevennum-number)                        | 判断对象是否为原始类型     |
| [isFunction](object.html#isevennum-number)                        | 判断对象是否为函数     |
| [isArray](object.html#isevennum-number)                        | 判断对象是否为数组     |
| [isString](object.html#isevennum-number)                        | 判断对象是否为字符串对象     |
| [isNumber](object.html#isevennum-number)                        | 判断对象是否为数字对象     |
| [isBoolean](object.html#isevennum-number)                        | 判断对象是否为布尔对象     |
| [isRegExp](object.html#isevennum-number)                        | 判断对象是否为正则对象     |
| [isFile](object.html#isevennum-number)                        | 判断对象是否为文件对象     |
| [isWindow](object.html#isevennum-number)                        | 判断对象是否为 windows 对象     |
| [isElement](object.html#isevennum-number)                        | 判断对象是否为 Element     |
| [isEvent](object.html#isevennum-number)                        | 判断对象是否为事件对象     |
| [isNull](object.html#isevennum-number)                        | 判断对象是否为 null 对象     |
| [isUndefined](object.html#isevennum-number)                        | 判断对象是否为未定义     |
| [isUndefinedOrNull](object.html#isevennum-number)                        | 判断对象是否为未定义或 null     |
| [clone](object.html#isevennum-number)                        | 克隆对象     |


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

* 返回值：`boolean` 对象为 object 类型 true；否则返回 false

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

* 返回值：`boolean` 对象是否为简单 object 类型 true；否则返回 false

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