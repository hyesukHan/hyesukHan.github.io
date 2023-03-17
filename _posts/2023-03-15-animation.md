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





