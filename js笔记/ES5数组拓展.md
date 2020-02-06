- Array.isArray(obj) : 用来判断一个对象是不是数组
    ```
    var a = [];
    var b = new Date();
    console.log(Array.isArray(a)); //true
    console.log(Array.isArray(b)); //false
    ```

- Array.indexOf / .lastIndexof : 该方法用于查找数组内指定元素的位置，查到第一个之后返回其索引，没有找到则返回-1。lastIndexOf反向搜索，查到第一之后，返回其索引，但顺序还是取正序。
    ```
    var arr = [2,3,4,"root","evenyao",3,8,7]
    console.log(arr.indexOf(3))   //1
    console.log(arr.indexOf(11))   //-1
    console.log(arr.lastIndexof(3))   //5
    ```

- Array.forEach(element, index, array) : 遍历数组，参数为一个回调函数，回调函数有三个参数
    - 当前元素
    - 当前元素索引值
    - 整个数组
    ```
    var arr = [1,2,3,4,5,6]
    arr.forEach(function(element,i,array){
        array[i]= element + 1
    })
    console.log(arr); //[2, 3, 4, 5, 6, 7]
    ```

- Array.map(function(element)) : 遍历数组，回调函数。返回值做操作之后组成一个新数组返回，新数组索引结构和原数组一致，原数组不变
    ```
    var arr = [1,2,3,4,5,6]
    var arr2 = arr.map(function(val){
        return val * val
    })
    console.log(arr)   //[1, 2, 3, 4, 5, 6]
    console.log(arr2)   //[1, 4, 9, 16, 25, 36]
    ```