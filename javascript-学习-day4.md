### 练习1. 写一对递增和递减的计数函数：

``` js
    var i = 0;
function increment() {
     i++;
     console.log(i);
}
function decrement() {
     i--;
     console.log(i);
}

```

### 练习2. 完成 makeCounter 函数：
``` js 
function makeCounter(count) {
 function increment() {
     count++;
     console.log(count);
     return count;
 }
 function decrement() {
     count--;
     console.log(count);
     return count;
 }
 return [increment,decrement];
}

```    