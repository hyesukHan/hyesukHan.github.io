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

 ```
transition-timing-function : linear | ease | ease=in | ease-out | ease-in-out | cubic-beaier(n,n,n,n)
 ```
속성값  

linear : 시작부터 끝까지 같은 속도로 트랜지션을 진행합니다.
ease : 천천히 시작해서 점점 빨라지다가 마지막에는 천천히 끝냅니다. 기본값입니다.  
ease-in : 시작을 느리게 합니다.  
ease-out : 느리게 끝냅니다.  
ease-in-out : 느리게 시작하고 느리게 끝냅니다.  
cubic-bezier(n,n,n,n) : 베지에 함수를 직접 정의해 사용합니다.  

  ```
 transition-delay : <시간>
  ```  
이 속성에서 지정하는 시간만큼 기다렸다가 트렌지션이 시작됩니다.
사용할 수 있는 값은 s나 ms입니다.

 ```
 <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #ex{
            position:relative;
            width: 500px;
            height: 150px;
            margin: 0 auto;
            border : 1px black solid;
            border-radius: 30px;
            padding: 20px;
        }
        #ex:hover .box{
            transform:rotate(360deg);
            margin-left:420px;
        }
        .box{
            font-size: 12px;
            position:relative;
            width:60px;
            height:60px;
            margin-bottom:10px;
            background-color:#eee;

        }
        .box p {
            text-align: center;
            padding-top: 4px;
        }

        #no-delay{
            transition-duration: 3s;
            border : 1px solid #ff6a00;
        }

        
        #delay{
            transition-duration: 3s;
            transition-delay:1s;
            border : 1px solid #006aff;
        }
    </style>
</head>
<body>
    <div id ="ex">
        <div id = "no-delay" class="box"><p>no-delay</p></div>
        <div id = "delay" class = "box"><p>delay</p></div>
    </div>
</body>
 ```
 위 소스는 첫번째 상자는 지연시간 없이 트랜지션을 실행하고 두 번째 상자에는 1초동안 지연시간을 두고 트랜지션을 실행해 비교한 것입니다.

