---
layout: post
title:  "flaot 적용했을 때 부모요소의 height"
date:   2023-04-10 21:35:12 +0900
categories: html+CSS
---
<h1>flaot 적용했을 때 부모요소의 height</h1>

html
```
 <div class="parent">
    <div class="box box1"></div>
    <div class="box box2"></div>
  </div>
  ```
css
```
body{
  background-color: orange;
}
.parent .box{
  width: 100px;
  height: 100px;
}

.parent .box.box1{
  background-color: blue;
}
.parent .box.box2{
  background-color: crimson;
}
```

box1,box2가 block레벨 요소일때(div는 블럭레벨 요소) 부모의 height 값이 자식의 height 값과 같다.

이때 .box1을 float:left 하게 되면 부모는 float된 요소의 height 값을 잃는다.

html
  같음

css
```
body{
  margin:0;
  background-color: orange;
}
.parent{
  background-color: antiquewhite;
}
.parent .box{
  width: 100px;
  height: 100px;
}

.parent .box.box1{
  background-color: blue;
  float:left;
}
.parent .box.box2{
  background-color: crimson;
}
```

box2를 float 하게되면 float 요소끼리는 정렬되지만 부모요소는 높이를 잃는다.  
css
```
.parent .box.box2{
  background-color: crimson;
  float:left;
}
```

이때 부모요소에게 overflow:hidden을 주게되면 다시 자식만큼의 높이를 가진다.  
css
```
.parent{
  background-color: antiquewhite;
  overflow : hidden;
}
````