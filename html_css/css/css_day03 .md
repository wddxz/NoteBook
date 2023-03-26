## day04-css

### 1-1 CSS层叠性

#### 1-1 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS层叠性</title>
    <style>
        div{
            /*这里颜色冲突，字体大小不存在，继续保留*/
            color: red;
            font-size: 35px;
        }
        div{
            /*就近原则，这里颜色是粉色*/
            color: pink;
        }
    </style>
</head>
<body>
  <div> 相同的选择器给设置相同的样式，就会有一个样式覆盖（层叠）另一个样式，层叠主要是解决样式冲突</div>
</body>
</html>
```

#### 1-1 页面渲染

![image-20230324173150742](image/image-20230324173150742.png)

### 1-2 CSS继承性

#### 1-2 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS继承性</title>
    <style>
        div{
            color: pink;
            font-size: 20px;
        }
    </style>
</head>
<body>
<div>
    <p>子标签会继承父标签的样式（text-,font-,line-,以及color属性）</p>
</div>
</body>
</html>
```

#### 1-2 页面渲染

![image-20230324173611087](image/image-20230324173611087.png)

### 1- 3 行高的继承

#### 1-3 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>行高的继承</title>
    <style>
        body{
            color: pink;
            font: 12px/1.5 "micrisoft yahei"
        }
        div{
            /*子元素继承了父元素 body 的行高1.5*/
            /*这个1.5 就是当前元素文字大小 font-size 的1.5倍 所以当前div 的行高就是21像素*/
            font-size: 14px;
        }
        p{
            /*1.5*16=24 当前的行高*/
            font-size: 16px;
        }
        /* li 么有手动指定文字大小  则会继承父亲的 文字大小  body 12px 所以 li 的文字大小为 12px

        当前li 的行高就是  12 * 1.5  =  18
        */
        li 么有手动指定文字大小 则会继承父亲的文字大小
    </style>
</head>
<body>
<div>我想要一个粉色的回忆</div>
<!--    我是段落，这里同ul同级-->
    <p>我也想拥有粉色的回忆 </p>
    <ul>
        <li>关系中我是孙子，没有指定文字大小</li>
    </ul>


</body>
</html>
```

#### 1-3 页面渲染

![image-20230324175030883](image/image-20230324175030883.png)

### 1- 4 CSS优先级

#### 1-4 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>css优先级</title>
  <style>
    /*权重是有四组数字组成，但是不会有进位*/
    /*类选择器大于元素选择器，id选择器永远大于类选择器*/
    /*等级判断从左到右，如果某一位数值相同，则判断下一位*/
    /*继承的权重为0，如果该元素没有直接被选中，不管父元素权重多高，子元素得到的权重都是0*/
    .test{
        color: red;
    }
    div{
        color: pink !important;
    }
    #demo{
        color: black;
    }
  </style>
</head>
<body>
<div class="test" id="demo" style="color: purple" >你笑起来真好看</div>
</body>
</html>
```

#### 1-4 页面渲染

![image-20230324182233665](image/image-20230324182233665.png)

### 1- 5 css权重注意点 

#### 1-5 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>css权重注意点</title>
    <style>
        /* 父亲的权重是 100  */
        #father{
            color: purple!important;
        }
        /* p继承的权重为 0 */
        /* 所以以后我们看标签到底执行那个样式,就先看这个标签有么有直接被选出来 */
        p{
            color: pink;
        }
        body{
            color: red;
        }
        a{
            /* a链接浏览器默认制定了一个样式 蓝色的 有下划线  a {color: blue;}*/
            color: green;
        }
    </style>
</head>
<body>
<div id="father">
    <p>你笑起来还是很好看</p>
</div>
<a href="#">我想要一个单独的样式</a>
</body>
</html>
```

#### 1- 5 页面渲染

![image-20230324183024957](image/image-20230324183024957.png)



### 1-6 权重的叠加  

#### 1-6 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>权重的叠加</title>
    <style>
        /* 复合选择器会有权重叠加的问题 */
        /* 权重虽然会叠加,但是永远不会有进位 */
        /* ul li 权重  0,0,0,1 + 0,0,0,1  =  0,0,0,2     2 */
        ul li{
            color: pink;
        }
        /* li 的权重是 0,0,0,1    1 */
        li{
            color: red;
        }
        /* .nav li  权重    0,0,1,0  +  0,0,0,1  =  0,0,1,1    11 */
        .nav li{
            color: green;
        }
    </style>
</head>
<body>
<ul class="nav" >
    <li>大猪蹄子</li>
    <li>大肘子</li>
    <li>猪尾巴</li>
</body>
</html>
```

#### 1-6 页面渲染

![image-20230324183852195](image/image-20230324183852195.png)

### 1-7  CSS权重练习 

#### 1-7 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS权重练习</title>
    <style>
        .nav{
            color: red;
        }
        /* 继承的权重是0 */

        li{
            color: pink;
        }
    </style>
</head>
<body>
<ul class="nav" >
    <li>人生四大悲</li>
    <li>家里没宽带</li>
    <li>网速不够快</li>
    <li>手机没流量</li>
    <li>学校没wifi</li>
</ul>
</body>
</html>
```

#### 1-7 页面渲染

![image-20230324184319928](image/image-20230324184319928.png)

### 1- 8 CSS权重练习2

#### 1- 8 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS权重练习2</title>
    <style>
        /* .nav li  权重是 11 */
        .nav li{
            color: red;
        }
        li{
            color: green;
        }
        /* 需求把第一个小li 颜色改为 粉色加粗 ? */
        /* .pink  权重是 10    .nav .pink  20  */
        .nav .pink{
            color: pink;
            font-weight: 700;
        }
    </style>
</head>
<body>
<ul class="nav">
    <li class="pink">人生四大悲</li>
    <li>家里没宽带</li>
    <li>网速不够快</li>
    <li>手机没流量</li>
    <li>学校没wifi</li>
</ul>
</body>
</html>
```

#### 1- 8 页面渲染

![image-20230324184646952](image/image-20230324184646952.png)

### 1-9   盒子模型之边框

#### 1- 9 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>盒子模型之边框</title>
    <style>
        /*border边框；conten内容；paddin内边距；margin外边距（盒子与盒子）*/
        div{
            width: 300px;
            height: 200px;
            /* border-width 边框的粗细  一般情况下都用 px */
            border-width: 5px;
            /* border-style 边框的样式  solid 实线边框   dashed 虚线边框  dotted 点线边框*/
            border-style: solid;
            /* border-style: dashed; */
            /* border-style: dotted; */
            /* border-color 边框的颜色  */
            border-color: red;
        }
    </style>
</head>
<body>
<div></div>
</body>
</html>
```

#### 1-9  页面渲染

![image-20230324185055038](image/image-20230324185055038.png)

### 1-10   边框的复合写法

#### 1-10 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>边框的复合写法</title>
    <style>
        div{
            width: 300px;
            height: 200px;
            /*border-width: 5px;
            border-style: solid;
            border-color: red;*/
            /* 边框的复合写法 简写:  */
            /* border: 5px solid pink; */
            /* 上边框 */
            border-top: 5px solid red ;
            /* 下边框 */
            border-bottom: 10px dashed purple;
        }
    </style>
</head>
<body>
<div></div>
</body>
</html>
```

#### 1-10 页面渲染

![image-20230324190504914](image/image-20230324190504914.png)

### 1- 11  边框的练习

#### 1-11 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>边框的练习</title>
    <style>
        /* 请给一个 200*200 的盒子，设置上边框为红色，其余边框为蓝色 */
        div{
            width: 200px;
            height: 200px;
            /* border-top: 1px solid red;
            border-bottom: 1px solid blue;
            border-left: 1px solid blue;
            border-right: 1px solid blue; */
            /* border包含四条边 */
            border: 5px solid blue;
            /* 层叠性 只是层叠了 上边框啊 */
            border-top: 5px solid red;
        }
    </style>
</head>
<body>
<div></div>
</body>
</html>
```

#### 1-11 页面渲染

![image-20230324190759528](image/image-20230324190759528.png)

### 1- 12 今日小说排行榜

#### 1- 12 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>细线表格今日小说排行榜案例</title>
    <style>
        table{
            width: 500px;
            height: 260px;
        }
        th{
            height: 30px;
        }
        table,
        td,th{
            border: 1px solid blue;
            /* 合并相邻的边框 */
            border-collapse: collapse;
            font-size: 18px;
            text-align: center;
        }
    </style>
</head>
<body>
<table align="center" cellspacing="0">
    <thead>
    <tr>
    <th>排名</th>
    <th>关键词</th>
    <th>趋势</th>
    <th>进入搜索</th>
    <th>最近七日</th>
    <th>相关链接</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <th>1</th>
        <th>剑来</th>
        <th><img src="up.jpg"></th>
        <th>456</th>
        <th>123</th>
        <th><a href="#">贴吧</a><a href="#">图片</a><a href="#">百科</a></th>
    </tr>

    <tr>
        <th>1</th>
        <th>遮天</th>
        <th><img src="up.jpg"></th>
        <th>456</th>
        <th>123</th>
        <th><a href="#">贴吧</a><a href="#">图片</a><a href="#">百科</a></th>
    </tr>

    <tr>
        <th>1</th>
        <th>神印王座</th>
        <th><img src="down.jpg"></th>
        <th>456</th>
        <th>123</th>
        <th><a href="#">贴吧</a><a href="#">图片</a><a href="#">百科</a></th>
    </tr>

    <tr>
        <th>1</th>
        <th>斗罗大陆</th>
        <th><img src="down.jpg"></th>
        <th>456</th>
        <th>123</th>
        <th><a href="#">贴吧</a><a href="#">图片</a><a href="#">百科</a></th>
    </tr>

    <tr>
        <th>1</th>
        <th>雪中悍刀行</th>
        <th><img src="down.jpg"></th>
        <th>456</th>
        <th>123</th>
        <th><a href="#">贴吧</a><a href="#">图片</a><a href="#">百科</a></th>
    </tr>

    </tbody>
</table>

</body>
</html>
```

#### 1-12  页面渲染

![image-20230324192246469](image/image-20230324192246469.png)

### 1-  13 边框会影响盒子的实际大小

#### 1-13 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>边框会影响盒子的实际大小</title>
    <style>
        div{
            /* 我们需要一个200*200的盒子, 但是这个盒子有10像素的红色边框 */
            width: 200px;
            height: 200px;
            border: 10px solid red;
            background-color: pink;
            
        }
    </style>


</head>
<body>
<div></div>
</body>
</html>
```

#### 1-13  页面渲染

![image-20230324192718988](image/image-20230324192718988.png)

### 1-  14 盒子模型之内边距

#### 1- 14 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>盒子模型之内边距</title>
    <style>
        /*设置一个200*200的盒子，背景是粉色，内边距：左20px，顶部是30px*/
        div{
            width: 200px;
            height: 200px;
            background-color: pink;
            padding-left: 20px;
            padding-top: 30px;
        }
    </style>
</head>
<body>
<div>盒子内容是content盒子内容是content盒子内容是content盒子内容是content</div>
</body>
</html>
```

#### 1- 14 页面渲染

![image-20230324193414409](image/image-20230324193414409.png)

### 1- 15 盒子模型之内边距

#### 1- 15 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>盒子模型之内边距复合写法</title>
    <style>
        /*设置一个200*200的盒子，背景是粉色，内边距：顶部是5px 右10px 下20px 左30px，*/
        div{
            width: 200px;
            height: 200px;
            background-color: pink;
            /* padding-left: 5px;
            padding-top: 5px;
            padding-bottom: 5px;
            padding-right: 5px; */
            /* 内边距复合写法(简写) */
            /* padding: 5px;（上下左右所有都是5px） */
            /* padding: 5px 10px;（上下5px 左右10px）*/
            /* padding: 5px 10px 20px; （上5px 左右10px 下20px）*/
            /*内边距：四个值，上 右 下 左 顺时针*/
            padding: 5px 10px 20px 30px;
        }
    </style>
</head>
<body>
<div>盒子内容是content盒子内容是content盒子内容是content盒子内容是content</div>

</body>
</html>
```

#### 1- 15 页面渲染

![image-20230324194133928](image/image-20230324194133928.png)

### 1- 16 内边距会影响盒子实际大小 

#### 1- 16 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>内边距会影响盒子实际大小</title>
    <style>
        div{
            width: 160px;
            height: 160px;
            background-color: pink;
            padding: 20px;
        }
    </style>
</head>
<body>
<div>
    padding会影响盒子实际大小padding会影响盒子实际大小padding会影响盒子实际大小padding会影响盒子实际大小
</div>
</body>
</html>
```

#### 1- 16 页面渲染

![image-20230324194335988](image/image-20230324194335988.png)

### 1-  17 新浪导航

#### 1- 17 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>padding应用-新浪导航</title>
    <style>
        /*1. 上边框为3像素，颜色为#ff8500*/
        /*2. 下边框为1像素，颜色#edeef0*/
        /*3. 盒子高度为41像素，背景颜色为#fcfcfc*/
        /*4. 文字颜色为#4c4c4c*/
        .nav{
            height: 41px;
            border-top: 3px solid #ff8500;
            border-bottom: 1px solid #edeef0;
            background-color: #fcfcfc;
            line-height: 41px;
        }
        .nav a{
            /* a属于行内元素 此时必须要转换 行内块元素 */
            display: inline-block;
            height: 41px;
            padding: 0 20px;
            font-size: 20px;
            color: #4c4c4c;
            text-decoration: none;
        }
        .nav a:hover{
            background-color: #eee;
            color: #ff8500;
        }
    </style>
</head>
<body>
<div class="nav">
<a href="#">新浪导航</a>
<a href="#">手机新浪网</a>
<a href="#">移动客户端</a>
<a href="#">微博</a>
<a href="#">三个字</a>
</div>
</body>
</html>
```

#### 1- 17 页面渲染

![image-20230324195608884](image/image-20230324195608884.png)

### 1- 18  简单版小米侧边栏

#### 1- 18 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>简单版小米侧边栏</title>
    <style>
        /* 1. 把a转换为块级元素 */
        a{
            display: block;
            width: 200px;
            height: 40px;
            background-color: #55585a;
            font-size: 18px;
            color: #fff;
            text-decoration: none;
            padding-left: 30px;
            line-height: 40px;
        }
        /* 2 鼠标经过链接变换背景颜色 */
        a:hover{
            background-color: #ff6700;
        }
    </style>
</head>
<body>
<a href="#">手机 电话卡</a>
<a href="#">电视 盒子</a>
<a href="#">笔记本 平板</a>
<a href="#">出行 穿戴</a>
<a href="#">智能 路由器</a>
<a href="#">健康 儿童</a>
<a href="#">耳机 音响</a>
</body>
</html>
```

#### 1-18  页面渲染

![image-20230324200150057](image/image-20230324200150057.png)

### 1-19   padding不会影响盒子大小的情况

#### 1- 19 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>padding不会影响盒子大小的情况</title>
    <style>
        h1{
            /*width: 100px;*/
            height: 200px;
            background-color: pink;
            padding: 30px;
        }
        div{
            width: 300px;
            height: 100px;
            background-color: purple;
        }
        div p{
            padding: 30px;
            background-color: red;
        }
    </style>
</head>
<body>
<h1></h1>
<div>
    <p></p>
</div>
</body>
</html>
```

#### 1- 19 页面渲染

![image-20230324200739495](image/image-20230324200739495.png)

### 1-  20 盒子模型之外边距margin

#### 1- 20 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>盒子模型之外边距margin</title>
    <style>
        div{
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        /*.one{
            margin-bottom: 20px;
        }*/
        .two{
            /*margin-top: 20px;*/
            /*margin: 30px;*/
            margin: 30px 50px;
        }
    </style>
</head>
<body>
<div class="one">1</div>
<div class="two">2</div>
</body>
</html>
```

#### 1- 20 页面渲染

![image-20230324201618623](image/image-20230324201618623.png)

### 1-21  块级盒子水平居中对齐

#### 1- 21 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>块级盒子水平居中对齐</title>
    <style>
        /*外边距可以让块级盒子水平居中，但是必须满足两个条件：
        1.盒子必须指定了宽度（width）
         2.盒子左右的外边距都设置为auto(自动）*/
        .header{
            width: 900px;
            height: 200px;
            background-color: pink;
            margin: 100px auto ;
        }
    </style>
</head>
<body>
<div class="header"></div>
</body>
</html>
```

#### 1- 21 页面渲染

![image-20230324203628484](image/image-20230324203628484.png)

### 1- 22  行内元素/行内块元素水平居中对齐

#### 1-22  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>行内元素/行内块元素水平居中对齐</title>
  <style>
    .header{
      width: 900px;
      height: 200px;
      background-color: pink;
      margin: 20px auto;
      text-align: center;
    }
    /* 行内元素或者行内块元素水平居中给其父元素添加 text-align:center 即可 */
  </style>
</head>
<body>
<div class="header">
  <span>里面的文字</span>
</div>
<div class="header">
  <img src="down.jpg" alt="">
</div>
</body>
</html>
```

#### 1- 22 页面渲染

![image-20230324204910527](image/image-20230324204910527.png)

### 1- 23  外边距合并-相邻块级元素垂直外边距合并

#### 1-23  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>外边距合并-相邻块级元素垂直外边距合并</title>
    <style>
        .damao, .ermao{
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .damao{
            margin-bottom: 100px;
        }
        .ermao{
            margin-top: 200px;
        }
    </style>
</head>
<body>
<div class="damao">大毛</div>
<div class="ermao">二毛</div>
</body>
</html>
```

#### 1-23  页面渲染

![image-20230324205816049](image/image-20230324205816049.png)

### 1- 24  外边距合并-嵌套块级元素垂直外边距塌陷

#### 1- 24 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>外边距合并-嵌套块级元素垂直外边距塌陷</title>
    <style>
        /*对于两个嵌套关系（父子）的块元素，父元素有上外边距同时子元素也有上外边距，
       此时父元素会塌陷较大的外边距值*/
        /*解决方案：
       1.可以为父元素定义上边框；
       2为父元素定义上内边距
       3为父元素添加overflow：hidden*/
        .father{
            width: 400px;
            height: 400px;
            background-color: purple;
            margin-top: 50px;
            /*border: 1px solid red;*/
            /*border:1px solid transparent ;*/
            /*padding: 1px;*/
            overflow: hidden;
        }
        .son{
            width: 200px;
            height: 200px;
            background-color: pink;
            margin-top: 100px;
        }
    </style>
</head>
<body>
<div class="father">
    <div class="son"></div>
</div>
</body>
</html>
```

#### 1- 24 页面渲染

![image-20230324211032312](image/image-20230324211032312.png)

### 1-  25 清除内外边距

#### 1- 25 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>清除内外边距</title>
    <style>
        /*这句话也是我们css 的第一行代码*/
        *{
            /*清除外边距*/
            margin: 0;
            /*清除内边距*/
            padding: 0;
        }
        /*注意：行内元素为了照顾兼容性，尽量只设置左右内外边距，不要设置上下内外边距。但是转换为块级和内快元素就可以了*/
        span{
            background-color: pink;
            margin: 20px;
        }
    </style>
</head>
<body>
123
<ul>
    <li>abcd</li>
</ul>
<span>行内元素尽量只设置左右的内外边距</span>
</body>
```

#### 1-25  页面渲染

![image-20230324212349748](image/image-20230324212349748.png)

### 1- 26  综合案例-产品模块

#### 1-26  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>综合案例-产品模块</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .box{
            width: 298px;
            height: 415px;
            background-color: #fff;
            /*让块级的盒子水平居中对齐*/
            margin: 100px auto;
        }
        .box img{
            /* 图片的宽度和父亲一样宽 */
            width: 100%;
        }
        .review{
            height: 70px;
            font-size: 14px;
            /* 因为这个段落没有 width属性 所有 padding不会撑开盒子的宽度 */
            padding: 0 28px;
            margin-top: 30px;
        }
        .appraise{
            font-size: 12px;
            color: #b0b0b0;
            margin-top: 20px;
            padding: 0 28px;
        }
        a{
            text-decoration: none;
            color: black;
        }
        .info{
            font-size: 14px;
            margin-top: 15px;
            padding: 0 28px;
        }
        .info h4{
            display: inline-block;
            font-weight: 400;
        }
        .info span{
            color: #ff6700;
        }
        .info em{
            font-style: normal;
            color:#ebe4e0 ;
            margin: 0 6px 0 15px;
        }
    </style>
</head>
<body>
<div class="box">
    <img src="images/img.jpg" alt="">
    <p class="review">快递牛，整体不错蓝牙可以说秒连。红米给力</p>
    <div class="appraise">来自于 117384232 的评价</div>
    <div class="info">
        <h4><a href="#">Redmi AirDots真无线蓝...</a></h4>
        <em>|</em>
        <span>99.9元</span>
    </div>

</div>
</body>
</html>
```

#### 1-26  页面渲染

![image-20230324215503693](image/image-20230324215503693.png)
