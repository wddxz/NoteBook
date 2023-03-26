## day04-css

### 1-1 新闻快报模块

#### 1-1 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>新闻快报模块</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .box{
            width: 248px;
            height: 163px;
            border: 1px solid #ccc;
            margin: 100px auto;
        }
        .box h3{
            height: 32px;
            line-height: 32px;
            border-bottom:1px dotted #ccc;
            font-size: 14px;
            font-weight: 400;
            padding-left:15px ;
        }
        li{
            /* 去掉li前面的小圆点 */
            list-style: none;

        }
        .box ul li a{
            font-size: 14px;
            color: #666;
            text-decoration: none;
        }
        .box ul li{
            height: 23px;
            line-height: 23px;
            padding-left: 10px;
        }
        .box ul li a:hover{
            text-decoration: underline;
        }
        .box ul{
            margin-top: 7px;
        }
    </style>
</head>
<body>
<div class="box">
<h3>品优购快报</h3>
    <ul>
        <li><a href="#">【特惠】爆款耳机5折秒！</a></li>
        <li><a href="#">【特惠】母亲节，健康好礼低至5折！</a></li>
        <li><a href="#">【特惠】爆款耳机5折秒</a></li>
        <li><a href="#">【特惠】9.9元洗100张照片！</a></li>
        <li><a href="#">【特惠】长虹智能空调立省1000</a></li>
    </ul>
</div>
</body>
</html>
```

#### 1-1 页面渲染

![image-20230325070551627](image/image-20230325070551627.png)

### 1-2 圆角边框

#### 1-2 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>圆角边框</title>
    <style>
        div{
            width: 300px;
            height: 150px;
            background-color: pink;
            border-radius: 10px;
        }
    </style>
</head>
<body>
<div></div>
</body>
</html>
```

#### 1-2 页面渲染

![image-20230325070858694](image/image-20230325070858694.png)

### 1- 3 圆角边框常用写法

#### 1-3 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>圆角边框常用写法</title>
    <style>
        .yuanxing {
            width: 200px;
            height: 200px;
            background-color: pink;
            /* border-radius: 100px; */
            /* 50% 就是宽度和高度的一半  等价于 100px */
            border-radius: 50%;
        }
        .juxing{
            width: 300px;
            height: 100px;
            background-color: pink;
            /* 圆角矩形设置为高度的一半 */
            border-radius: 50px;
        }
        .radius{
            width: 200px;
            height: 200px;
            background-color: pink;
            /* border-radius: 10px 20px 30px 40px; */
            /* border-radius: 10px 40px; */
            /*border-top-right-radius: 30px;*/
            border-bottom-left-radius: 50px;
        }
    </style>
</head>
<body>
1、圆形的做法：
<div class="yuanxing"></div>
2、圆角矩形的做法：
<div class="juxing"></div>
3、可以设置不同的圆角：
<div class="radius"></div>
</body>
</html>
```

#### 1-3 页面渲染

![image-20230325071807263](image/image-20230325071807263.png)

### 1- 4 盒子阴影

#### 1-4 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>盒子阴影</title>
    <style>
        div{
            width: 200px;
            height: 200px;
            background-color: pink;
            margin: 100px auto;
          /*box-shadow: 10px 10px; */
        }
        div:hover{
            box-shadow: 10px 10px 10px -4px rgba(0,0,0,.3);
        }
        /* 原先盒子没有影子,当我们鼠标经过盒子就添加阴影效果 */
    </style>
</head>
<body>
<div></div>
</body>
</html>
```

#### 1-4 页面渲染

![image-20230325072302761](image/image-20230325072302761.png)

### 1- 5文字阴影

#### 1-5 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>文字阴影</title>
    <style>
        div{
            font-size: 50px;
            color: red;
            font-weight: 700;
            text-shadow: 5px 5px 6px rgba(0,0,0,.3);
        }
    </style>
</head>
<body>
<div>你是阴影，我是火影</div>
</body>
</html>
```

#### 1- 5 页面渲染

![image-20230325072545369](image/image-20230325072545369.png)



### 1-6   行内块中间有缝隙

#### 1-6 源码

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>行内块中间有缝隙</title>
    <style>
        div{
            float: left;
            width: 150px;
            height: 200px;
            background-color: pink;
            /*display: inline-block;*/
        }
    </style>
</head>
<body>
<div>1</div>
<div>2</div>
<div>3</div>
</body>
</html>
```

#### 1-6 页面渲染

![image-20230325152330067](image/image-20230325152330067.png)

### 1-7  什么是浮动

#### 1-7 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>什么是浮动</title>
    <style>
        .left,
        .right{
            float: left;
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .right{
            float: right;
        }
    </style>
</head>
<body>
<div class="left">左左</div>
<div class="right">右右</div>
</body>
</html>
```

#### 1-7 页面渲染

![image-20230325153302557](image/image-20230325153302557.png)

### 1- 8浮动特性1

#### 1- 8 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动特性1</title>
    <style>
        /* 设置了浮动（float）的元素会：
        1. 脱离标准普通流的控制（浮）移动到指定位置（动）。
        2.浮动的盒子不在保留原先的位置 */
        .box1{
            float: left;
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .box2{
            width: 300px;
            height: 300px;
            background-color: rgb(0,153,255);
        }
    </style>
</head>
<body>
<div class="box1">浮动的盒子</div>
<div class="box2">标准流的盒子</div>
</body>
</html>
```

#### 1- 8 页面渲染

![image-20230325165950936](image/image-20230325165950936.png)

### 1-9   浮动元素特性-浮动元素一行显示

#### 1- 9 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动元素特性-浮动元素一行显示</title>
    <style>
        /*如果多个盒子都设置了浮动，则它们会按照属性值一行内显示并且顶端对齐排列*/
        /*如果想要在同一行显示，三个div都要设置浮动属性*/
        /*注意：浮动的元素是互相贴靠在一起（不会有缝隙）的，如果父子宽度装不下这些浮动的盒子，
        多出的盒子会另起一行对齐。*/
        div{
            float: left;
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .two{
            background-color: purple;
            height: 249px;
        }
        .four{
            background-color: skyblue;
        }

    </style>
</head>
<body>
<div>1</div>
<div class="two">2</div>
<div>3</div>
<div class="four">4</div>
</body>
</html>
```

#### 1-9  页面渲染

![image-20230325165913437](image/image-20230325165913437.png)

### 1-10  浮动的元素具有行内块元素特点

#### 1-10 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动的元素具有行内块元素特点</title>
    <style>
        /*任何元素都可以浮动，不管原先是什么样式的元素，添加浮动之后具有行内块元素相似的特性*/
        span,
        div{
            float: left;
            width: 200px;
            height: 100px;
            background-color: pink;
        }
        /*如果行内元素有了浮动，则不需要转换块级\行内块元素就可以直接给高度和宽度*/
        /*如果块级盒子没有设置宽度，默认宽度和父级一样宽，但是添加浮动后，它的大小根据内容来决定*/
        /*行内元素同理*/
        p{
            float: right;
            height: 200px;
            background-color: purple;
        }
    </style>
</head>
<body>
<span>1</span>
<span>2</span>
<div>div</div>
<p>pppppppppp</p>

</body>
</html>
```

#### 1-10 页面渲染

![image-20230325172359312](image/image-20230325172359312.png)

### 1- 11  浮动元素搭配标准流父盒子1

#### 1-11 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动元素搭配标准流父盒子1</title>
    <style>
        /*先用标准流的父元素排列上下位置，之后内部子元素采取浮动排列左右位置，符合网页布局第一准则*/
        .box{
            width: 1200px;
            height: 460px;
            background-color: pink;
            margin: 0 auto;
        }
        .left{
            float: left;
            width: 230px;
            height: 460px;
            background-color: skyblue;
        }
        .right{
            float: left;
            width: 970px;
            height: 460px;
            background-color: purple;
        }
    </style>
</head>
<body>
<div class="box">
    <div class="left">左侧</div>
    <div class="right">右侧</div>
</div>
</body>
</html>
```

#### 1-11 页面渲染

![image-20230325174106581](image/image-20230325174106581.png)

### 1- 12浮动元素搭配标准流父盒子2

#### 1- 12 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动元素搭配标准流父盒子2</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        li{
            list-style: none;
        }
        .box{
            width: 1226px;
            height: 285px;
            background-color: pink;
            margin: 0 auto;
        }
        .box li{
            width: 296px;
            height: 285px;
            background-color: purple;
            float: left;
            margin-right: 14px;

        }
        .box .last{
            margin-right: 0;
        }
    </style>
</head>
<body>
<ul class="box">
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li class="last">4</li>
</ul>
</body>
</html>
```

#### 1-12  页面渲染

![image-20230325180217147](image/image-20230325180217147.png)

### 1-  13 浮动布局练习3

#### 1-13 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动布局练习3</title>
    <style>
        .box{
            width: 1226px;
            height: 615px;
            background-color: pink;
            margin: 0 auto;
        }
        .left{
            float: left;
            width: 234px;
            height: 615px;
            background-color: skyblue;
        }
        .right{
            float: left;
            width: 992px;
            height: 615px;
            background-color: purple;
        }
        .right>div{
            float: left;
            width: 234px;
            height: 300px;
            background-color: pink;
            margin-left: 14px;
            margin-bottom: 14px;
        }
    </style>
</head>
<body>
<div class="box">
    <div class="left">左左</div>
    <div class="right">
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
        <div>6</div>
        <div>7</div>
        <div>8</div>
    </div>

</div>
</body>
</html>
```

#### 1-13  页面渲染

![image-20230325182218294](image/image-20230325182218294.png)

### 1-  14常见网页布局

#### 1- 14 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>常见网页布局</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        li{
            list-style: none;
        }
        .top{
            height: 50px;
            background-color: gray;
        }
        .banner{
            width: 980px;
            height: 150px;
            background-color: gray;
            margin: 10px auto;
        }
        .box{
            width: 980px;
            height: 300px;
            margin: 0 auto;
            background-color: pink;
        }
        .box li{
            float: left;
            width: 237px;
            height: 300px;
            background-color: gray;
            margin-right: 10px;
        }
        .box .last{
            margin-right: 0;
        }
        /*只要是通栏的盒子（和浏览器一样宽） 不需要指定宽度*/
        .footer{
            height: 200px;
            background-color: gray;
            margin-top: 10px;
        }
    </style>

</head>
<body>
<div class="top">top</div>
<div class="banner">banner</div>
<div class="box">
    <ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li class="last">4</li>
    </ul>
</div>
<div class="footer">footer</div>
</body>
</html>
```

#### 1- 14 页面渲染

![image-20230325184925338](image/image-20230325184925338.png)

### 1- 15 浮动注意点

#### 1- 15 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>浮动注意点</title>
    <style>
        /* 如果一个子元素浮动了,尽量其他盒子也浮动,这样保证这些子元素一行显示 */
        .box{
            width: 900px;
            height: 300px;
            background-color: pink;
            margin: 0 auto;
        }
        .damao{
            float: left;
            width: 200px;
            height: 200px;
            background-color: skyblue;
        }
        .ermao{
            float: left;
            width: 300px;
            height: 250px;
            background-color:purple;
        }
        .sanmao{
            float: left;
            width: 250px;
            height: 260px;
            background-color: #ff6700;
        }
    </style>
</head>
<body>
<div class="box">
    <div class="damao">大毛</div>
    <div class="ermao">二毛</div>
    <div class="sanmao">三毛</div>
</div>
</body>
</html>
```

#### 1- 15 页面渲染

![image-20230326042553460](image/image-20230326042553460.png)

### 1- 16  为什么需要清除浮动

#### 1- 16 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>为什么需要清除浮动</title>
    <style>
        .box{
            width: 980px;
            border: 1px solid blue;
            margin: 0 auto;
        }
        .damao{
            float: left;
            width: 350px;
            height: 200px;
            background-color: purple;
        }
        .ermao{
            float: left;
            width: 400px;
            height: 200px;
            background-color: pink;
        }
        .footer{
            height: 200px;
            background-color: #ff6700;
        }
    </style>
</head>
<body>
<div class="box">
    <div class="damao">大毛</div>
    <div class="ermao">二毛</div>
</div>
<div class="footer"></div>
</body>
</html>
```

#### 1- 16 页面渲染

![image-20230326044042815](image/image-20230326044042815.png)

### 1-  17 清除浮动之额外标签法

#### 1- 17 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>清除浮动之额外标签法</title>
    <style>
        .box{
            width: 980px;
            border: 1px solid blue;
            margin: 0 auto;
        }
        .damao{
            float: left;
            width: 300px;
            height: 200px;
            background-color: purple;
        }
        .ermao{
            float: left;
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .footer{
            height: 200px;
            background-color: #ff6700;
        }
        .clear{
            clear:both
        }
    </style>
</head>
<body>
<div class="box">
    <div class="damao">大毛</div>
    <div class="ermao">二毛1</div>
    <div class="ermao">二毛2</div>
    <div class="ermao">二毛2</div>
    <div class="ermao">二毛2</div>
    <!-- <div class="clear"></div> -->
    <!-- 这个新增的盒子要求必须是块级元素不能是行内元素 -->
    <span class="clear"></span>
</div>
<div class="footer"></div>
</body>
</html>
```

#### 1- 17 页面渲染

![image-20230326045510239](image/image-20230326045510239.png)

### 1- 18  为什么需要清除浮动

#### 1- 18 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>为什么需要清除浮动</title>
    <style>
        .box{
            overflow: hidden;
            width: 800px;
            border: 1px solid blue;
            margin: 0 auto;
        }
        .damao{
            float: left;
            width: 300px;
            height: 200px;
            background-color: purple;
        }
        .ermao{
            float: left;
            width: 200px;
            height: 200px;
            background-color:pink ;
        }
        .footer{
            height: 200px;
            background-color: black;
        }
    </style>
</head>
<body>
<div class="box">
    <div class="damao">大毛</div>
    <div class="ermao">二毛</div>
</div>
<div class="footer"></div>
</body>
</html>
```

#### 1-18  页面渲染

![image-20230326051014959](image/image-20230326051014959.png)

### 1-19   伪元素清除浮动

#### 1- 19 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>伪元素清除浮动</title>
    <style>
        .clearfix:after{
            content: "";
            display: block;
            height: 0;
            clear: both;
            visibility: hidden;
        }
        .clearfix{
            /* IE6、7 专有 */
            *zoom:1
        }
        .box{
            width: 900px;
            border: 1px solid blue;
            margin: 0 auto;
        }
        .damao{
            float: left;
            width: 300px;
            height: 200px;
            background-color: purple;
        }
        .ermao{
            float: left;
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .footer{
            height: 200px;
            background-color: black;
        }
    </style>
</head>
<body>
<div class="box clearfix">
    <div class="damao">damao</div>
    <div class="ermao">ermao</div>
</div>
<div class="footer"></div>
</body>
</html>
```

#### 1- 19 页面渲染

![image-20230326212818984](image/image-20230326212818984.png)

### 1-  20 清除浮动之双伪元素清除

#### 1- 20 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>清除浮动之双伪元素清除</title>
    <style>
        .clearfix:before,
        .clearfix:after{
            content: "";
            display: table;
        }
        .clearfix:after{
            clear: both;
        }
        .clearfix{
            *zoom:1
        }
        .box{
            width: 800px;
            border: 1px solid blue;
            margin:0 auto;
        }
        .damao{
            float: left;
            width: 300px;
            height: 200px;
            background-color: skyblue;
        }
        .ermao{
            float: left;
            width: 200px;
            height: 200px;
            background-color: #ff6700;
        }
        .footer{
            height: 200px;
            background-color: pink;
        }
    </style>
</head>
<body>
<div class="box clearfix">
    <div class="damao">damoa</div>
    <div class="ermao">ermao</div>
</div>
<div class="footer"></div>
</body>
</html>
```

#### 1- 20 页面渲染

![image-20230326215031586](image/image-20230326215031586.png)

