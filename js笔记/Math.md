- Math.round(): 返回一个数字四舍五入后最接近的整数。
    ```
    a = Math.round(20.49)  //20
    b = Math.round(20.5)   //21
    c = Math.round(-20.5)  //-20
    d = Math.round(-20.51) //-21
    ```

- Math.abs()/max()/min()
    - abs方法返回参数值的绝对值
    - max方法返回最大的参数
    - min方法返回最小的参数
    ```
    Math.abs(1) // 1
    Math.abs(-1) // 1
    Math.max(2, -1, 5) // 5
    Math.min(2, -1, 5) // -1
    ```

- Math.floor()/ceil()
    - floor方法返回小于参数值的最大整数
    ```
    Math.floor(3.2) // 3
    Math.floor(-3.2) // -4
    ```
    - ceil方法返回大于参数值的最小整数
    ```
    Math.ceil(3.2) // 4
    Math.ceil(-3.2) // -3
    ```

- Math.random(): 该方法返回0到1之间的一个伪随机数，可能等于0，但是一定小于1
    ```
    Math.random() // 0.7151307314634323
    ```