# 时间Date

## 1. 创建Date对象的方式

- 没有传入任何的参数，获取到当前时间

  ```
  var date1 = new Date();
  console.log(date1);
  ```

- 传入参数：时间字符串

  ```
  var date2 = new Date("2022-08-08");
  console.log(date2);
  ```

- 传入具体的年月日时分秒毫秒

  ```
  var date3 = new Date(2033, 10, 10, 09, 08, 07, 333);
  console.log(date3);
  ```

- 传入一个Unix时间戳

  ```
  var date4 = new Date(10004343433);
  console.log(date4);
  ```

## 2. Date的对象方法

```
var date = new Date();
```

- 获取想要的时间信息

  ```
  var year = date.getFullYear(); // 年
  var month = date.getMonth(); // 月
  var day = date.getDate(); // 日
  var hour = date.getHours(); // 时
  var minute = date.getMinutes(); // 分
  var second = date.getSeconds(); // 秒
  
  console.log(`${ year }/${ month + 1 }/${ day } ${ hour }:${ minute }:${ second }`);
  
  var weekday = date.getDay(); // 一周中的第几天
  console.log(weekday);
  ```

## 3. Date对象的两种表示标准

```
var date = new Date();
console.log(date);
console.log(date.toDateString());
console.log(date.toISOString());
```

## 4.获取Unix时间戳

```
var date = new Date();
var date2 = new Date("2033-03-03");

// 方法一：当前时间的时间戳
var timestamp1 = date.now();
console.log(timestamp1);

// 方法二/三将一个date对象转成时间戳
var timestamp2 = date.getTime();
var timestamp3 = date.valueOf();
console.log(timestamp2, timestamp3);

// 方法四：了解
console.log(+date);
```



