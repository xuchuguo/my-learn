- Date.now(): 返回当前距离1970年1月1日00:00:00的毫秒数
    ```
    Date.now() //1584087697240
    ```

- Date.parse(): 用来解析日期字符串，返回距离1970年1月1日00:00:00的毫秒数

    日期字符串的格式应该完全或者部分符合YYYY-MM-DDTHH:mm:ss.sssZ格式，Z表示时区，是可选的
    
    如果解析失败，返回NaN
    ```
    Date.parse("January 26, 2011 13:51:50") //1296021110000
    ```

- new Date(): 使用Date构造函数创建一个Date的实例
    ```
    var d = new Date()
    console.log(d) //Fri Mar 13 2020 16:26:51 GMT+0800 (中国标准时间)
    d.getTime()         //返回实例对象距离1970年1月1日00:00:00对应的毫秒数
    d.getDay()          //返回星期，星期日为0，星期一为1，以此类推
    d.getFullYear()     //返回四位的年份
    d.getMonth()        //返回月份（0表示1月，11表示12月）
    d.getDate()         //返回实例对象对应每个月的几号（从1开始）
    d.getHours()        //返回小时(0~23)
    d.getMinutes()      //返回分钟（0-59）
    d.getSeconds()      //返回秒（0-59
    d.getMilliseconds() //返回毫秒（0-999）
    ```