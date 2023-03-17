---
layout: post
title:  "animation"
date:   2023-03-17 17:35:12 +0900
categories: html+CSS
---

# animation
CSS 애니메이션은 시작해 끝내는 동안 원하는 곳 어디서든 스타일을 바꾸며 애니메이션을 정의할 수 있습니다. 이 때 애니메이션 중간에 스타일이 바뀌는 지점을 키프레임이라고 부릅니다.

### CSS 애니메이션에서 사용하는 속성

**@keyframes 속성**<br>

```@keframes <이름> {<선택자>{<스타일>}}```

```  <style>
        div{
            width:100px;
            height: 100px;
            background-color: blue;
            animation-name: change-bg;
            animation-duration: 3s;
        }
        @keyframes change-bg {
            from{
                background-color: blue;
                border:1px solid black;
            }
            to{
                background-color:#a5d6ff;
                border:1px solid blue;
                border-radius: 50%;
            }
        }
    </style>
</head>
<body>
    <div></div>
</body>
```
### animation-name 속성- 애니메이션 이름 지정하기

css로 애니메이션을 만들 때 @keyframe 속성을 이용해 여러개의 애니메이션을 정의하는데 animation-name 속성에서 지정한 애니메이션 이름으로 구분합니다.


```
 <style>
        div{
            display:  inline-block;
        }
        #box1 {
            width:100px;
            height:100px;
            background-color: #4cff00;
            border:1px solid black;
            animation-name: shape;
            animation-duration: 3s;
        }
        #box2 {
            
            width:100px;
            height:100px;
            background-color: #8f05b0;
            border: 1px solid black;
            animation-name: rotate;
            animation-duration: 3s;
        }

        @keyframes shape {
            from{
                border: 1px solid black;
            }
            to{
                border: 1px solid black;
                border-radius: 50%;
            }
        }

        @keyframes rotate {
            from {
                transform: rotate(0deg);
            }
            to{
                transform:rotate(45deg);
            }
        }
    </style>
</head>
<body>
    <div id = "box1"></div>
    <div id = "box2"></div>
</body>
```

### animation-duration 속성- 애니메이션 실행시간 설정하기

```
animation-duration:<시간>
```

애니메이션을 얼마 동안 재생할 지 설정합니다. 사용할 수 있는 값은 s나 ms입니다. 기본값이 0이므로 속성을 정의하지 않으면 애니메이션이 일어나지 않습니다.

### animation-direction속성-애니메이션 방향 지정하기

```
animation-direction: normal | alternate
```

normal은 애니메이션을 끝까지 실행하면 원래 있던 위치로 돌아갑니다. <br>
alternate 애니메이션을 끝까지 실행하면 왔던 방향으로 되돌아가면서 애니메이션을 실행합니다.



