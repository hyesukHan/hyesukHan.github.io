---
layout: post
title:  "transition"
date:   2023-03-15 17:35:12 +0900
categories: jekyll update
---

트랜지션이란?

웹 요소의 스타일 속성이 바뀌는 것 

transition-property : 트랜지션의 대상 설정  
transition-duration : 트랜지션 진행 시간 설정  
transition-timing-function : 트랜지션 속도 곡선 설정  
transition-delay : 트랜지션 지연 시간 설정  
transition : 위 속성들을 한번에 설정  

transition-property  

 ```
transition-property: all | none | <속성이름>  
 ```

속성값  
all : 기본 값으로 모든 속성이 트랜지션 대상이 됩니다.  
none : 트랜지션동안 아무 속성도 바뀌지 않습니다.  
<속성이름> : 원하는 대상을 골라 지정할 수 있습니다.    

transition-duration  

 ```
transition-duration: <시간>
 ```

트랜지션의 진행 시간은 지정하지 않으면 0초입니다. 트랜지션 대상이 되는 속성이 여러개라면 ,로 구분해 순서대로 여러 개를 지정할 수 있습니다.

 ```
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .tr1{
            width: 100px;
            height:100px;
            background-color:blue;
            border: 1px solid black;
            transition-property: width,height;
            transition-duration: 2s,1s;
        }
        .tr1:hover{
            width:200px;
            height:120px;
        }
    </style>
</head>
<body>
    <div class="tr1"></div>
</body>
 ```
요소에 마우스 호버가 되면 넓이와 높이가 2초, 1초에 걸쳐서 바뀌는 소스입니다.