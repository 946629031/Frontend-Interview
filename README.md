# Frontend-Interview
Frontend-Interview 前端面试题


----

# 字节跳动面试
- ## 1-1 事件循环

    ```js
    const log = console.log;

    log(1);
    setTimeout(() => {
    log(2);
    });

    new Promise((r) => {
    log(3);
    r(4);
    log(5);
    }).then((res) => {
    log(res);
    });

    log(6);

    (async () => {
    log(7);
    await new Promise((r) => {
        log(8);
        r();
    });
    log(9);
    })();


    // 打印结果: 135678492
    ```




## 标题2 semver sort - 版本号排序

题目描述
- 有一组版本号如下 `['0.1.1', '2.3.3', '0.302.1', '4.2', '4.3.5', '4.3.4.5']`。
- 现在需要对其进行降序排序，排序的结果入如 `['4.3.5','4.3.4.5','4.2','2.3.3','0.302.1','0.1.1']​`

- 提示：关注两个版本号之间如何比较即可​
```js
const versions = ['0.1.1', '2.3.3', '0.302.1', '4.2', '4.3.5', '4.3.4.5'];​
versions.sort((a, b) => {​
// ...补全​
})​

console.log(versions)
```

```js
const versions = ['0.1.1', '2.3.3', '0.302.1', '4.2', '4.3.5', '4.3.4.5'];

function compare (aArr, bArr) {
  let res = undefined
  aArr.forEach((no, index) => {
      aNumber = parseInt(no)
      bNumber = parseInt(bArr[index])
      if (aNumber > bNumber) {
          res = -1
      } else if (aNumber < bNumber) {
          res = 1
      } else {
          res = 0
      }
  })
  return res
}
versions.sort((a, b) => {
  // ...补全
  let aArr = a.split('.');
  let bArr = a.split('.');

  return compare(aArr, bArr);
})

console.log(versions)
```






## 标题3
有效的括号

题目描述
给定一个只包括 '('，')'，'{'，'}'，'['，']' 的字符串 s ，判断字符串是否有效。​

有效字符串需满足：​

左括号必须用相同类型的右括号闭合。​
左括号必须以正确的顺序闭合。​
每个右括号都有一个对应的相同类型的左括号。​

输入：s = "()[]{}"​
输出：true​

输入：s = "(]"​
输出：false



```js
let str = "()[]{}";
let str2 = "(])[]{}"


function findStr (str, inputStr) {
    let targetStr = ''
    if (str === '(') {
        targetStr = ')'
    } else if (str === '{') {
        targetStr = '}'
    } else if (str === '[') {
        targetStr = ']'
    } else {
        return
    }
        
    let arr = inputStr.split('')
    for(let i = 0; i < arr.length; i++) {
        if (arr[i] === targetStr) {
            return 'true'
        }
    }
    return 'false'
}
console.log( findStr('(', str2) )
```












[2年经验前端应聘者，要价15k，我负责他的初面！还行！](https://www.bilibili.com/video/BV1eY411h7Xx/?spm_id_from=333.788&vd_source=8efdbeeec5a624102dde94b64d8c6ebc)

### 1、html5的语义化的好处是什么? 
### 2、css3实现毛玻璃背景效果怎么实现?
### 3、Promise的then方法为什么能链式调用? 
### 4、async/await是怎么做到串行执行异步操作的?
### 5、https比http安全在哪呢? 
### 6、快速排序和冒泡排序的时间复杂度是多少? 
### 7、vue中v-model是语法糖,不用v-mode用什么可以替代?
### 8、vue组件销毁时,所有自定义事件和原生事件都会跟着解绑吗? 
### 9、vue3是怎么解决vue2的响应式缺陷的?
### 10、nexttick是什么任务?为什么优先是微任务? 
### 11、JavaScript不同数据类型是怎么一个存储方式? 
### 12、一个超长字符串能存在栈内存里面吗?
### 13、赋值、浅拷贝、深拷贝的区别?
### 14、webworker开一个子线程,那怎么监听子线程挂了 
### 15、webpack的style-loader和css-loader的区别? 
### 16、webpack如何配置typescript的打包? 
### 17、webpack的三种hash值配置的区别?
### 29、DOMContentLoaded和load的区别?
### 30、强缓存和协商缓存的区别?





### 18、如何计算白屏时间呢?
### 19、本地服务代理为什么能解决跨域问题?跨域问题的其他解决方法了解过吗?
### 20、vue中二次封装时数据往下一层一层传递很麻烦,怎么才能一次性传下去?
### 21、vuex是怎么做到将数据注入到每一个组件里的?
### 22、vite很快,那他为什么快呢?有了解过吗?
### 23、axios拦截器如何拦截请求错误或者响应错误 
### 24、axios这个库是如何区分浏览器环境和node环境的? 
### 25、项目中哪些模块是你主导的?简单聊聊吧 
### 26、你觉得搭建一个组件库需要注意哪些事? 
### 27、有没有在项目中做过换肤的业务? 
### 28、有没有在项目中做过国际化语言切换?