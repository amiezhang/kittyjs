# KittyJS

KittyJS is a super lightweight but complete AMD-compliant module loader with:

- Loader Plugin supported;
- Common Config supported, include BaseUrl、paths、packages、map、config and shim.

it was originally named as 'SimpleAndNaiveJS', since its implement is really simple. In fact, it just has about 600 source code lines, but it actually works. If you want to know how AMD loader works, you can try to read it, it's easier to understand.

## KittyJS vs requireJS
| Item      |  KittyJS | requireJS  | esl |
| :-- | --:| --: | --: |
| Size      | 2.8kb  |  6.2kb | 3.7kb |
| Performance  | - |  almost  | same |
| Shim support | YES | YES | NO |
| Timeout handler| NO | YES | YES |

## Test

fully tested by the [AMD Tests](https://github.com/amdjs/amdjs-tests) and [ESL Tests](https://github.com/zengjialuo/kittyjs/tree/master/test)

## Usage

```html
<script src="http://rigel.baidustatic.com/wg_biz/kitty/kitty.js"></script>
```

config options is same with requireJS, just try to replace the scirpt src.

## 异步请求
```js
window.require(["https://demo/test.js"], (res) => {
    console.log(res); // 打印出来一个es module
    window.define('包名1', res); // 定义到全局，其他包使用时，通过require('包名')就可以使用该module
})
```
打印出来一个es module
![image](https://user-images.githubusercontent.com/15716269/170341794-e79d7166-26b1-4a99-8099-c41a65814c76.png)


