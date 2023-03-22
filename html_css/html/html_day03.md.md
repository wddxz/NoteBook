## day03-css

### 1_体验CSS语法规范

#### 1- 1  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>体验CSS语法规范</title>
    <style>
/*选择器改{样式}*/
/* 给谁改样式{ 改什么样式} */
 p {
     color: red;
     /* 修改了文字大小为12像素 */
     font-size:12px;
 }
    </style>
</head>
<body>
<p>有点意思</p>
</body>
</html>
```

#### 1- 1 页面渲染

![image-20230322033038569](image/image-20230322033038569.png)

### 2_基础选择器之标签选择器

#### 1- 2  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>基础选择器之标签选择器</title>
</head>
<style>
    /* 标签选择器：写上标签名*/
    p{
        color:green;
    }
    div{
        color: pink;
    }
</style>
<body>
<p>男生</p>
<p>男生</p>
<p>男生</p>
<div>女生</div>
<div>女生</div>
<div>女生</div>
</body>
</html>
```

#### 1-  2 页面渲染

![image-20230322040252105](image/image-20230322040252105.png)

### 3_ 基础选择器之类选择器

#### 1-3   源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>基础选择器之类选择器</title>
</head>
<style>
    /*类选择器口诀：样式点定义 结构类（class）调用 一个或多个 开发最常用*/
    .red{
        color: red;
    }
    .star-sing{
        color: aqua;
    }
    .memeda{
        color: blueviolet;
    }
</style>
<body>
 <ul>
     <li CLASS="red">骗子</li>
     <li CLASS="red">最幸运的幸运</li>
     <li> 李香兰</li>
     <li CLASS="memeda">余年</li>
     <li CLASS="star-sing">满足</li>
 </ul>
<div class="red">我是真的喜欢喜庆的颜色，大吉大利</div>
</body>
</html>
```

#### 1- 3 页面渲染

![image-20230322043229127](image/image-20230322043229127.png)

### 4_ 利用类选择器画三个盒子

#### 1-4   源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>利用类选择器画三个盒子</title>
</head>
<style>
    .red{
        width: 100px;
        height: 100px;
    /*    背景色*/
        background-color: red;
    }
    .green{
        width: 100px;
        height: 100px;
        background-color: green;
    }
</style>
<body>
<div class="red">红色</div>
<div class="green">绿色</div>
<div class="red">红色</div>
</body>
</html>
```

#### 1- 4 页面渲染

![image-20230322045102960](image/image-20230322045102960.png)

### 5_ 多类名的使用方式

#### 1- 5  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>类选择器多类名的使用</title>
</head>
<style>
    .red{
        color: red;
    }
    .font35{
        font-size: 35px;
    }
</style>
<body>
<div class="red font35"> 肖战</div>
</body>
</html>
```

#### 1-5  页面渲染

![image-20230322045606474](image/image-20230322045606474.png)

### 6_利用类选择器画三个盒子

#### 1- 6  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>多类名的使用场景</title>
</head>
<style>
    .box{
        width: 150px;
        height: 100px;
        font-size: 30px;
    }
    .red{
        width: 150px;
        height: 100px;
        background-color: red;
    }
    .green{
        width: 150px;
        height: 100px;
        background-color: green;
    }
</style>
<body>
<div class=" box red">红色</div>
<div class=" box green">绿色</div>
<div class=" box red">红色</div>
</body>
</html>
```

#### 1-6  页面渲染

![image-20230322050336018](image/image-20230322050336018.png)

### 7_ 基础选择器之id选择器

#### 1- 7  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>基础选择器之id选择器</title>
</head>
<style>
    /*id选择器的口诀：样式#定义，结构id调用，只能调用一次，别人切务使用*/
    #red{
        color: red;
    }
</style>
<body>
<div id="red">肖战</div>
<div>肖战老婆</div>
</body>
</html>
```

#### 1- 7 页面渲染

![image-20230322050801423](image/image-20230322050801423.png)

### 8_基础选择器之通配符选择器

#### 1- 8  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>通配符选择器</title>
</head>
<style>
    *{
        color: red;
    }
    /* *这里把html body div span li等等的标签都改为了红色*/
</style>
<body>
<div>肖战</div>
<span>疾冲</span>
<ul>
    <li>方天泽都是我的</li>
</ul>
</body>
</html>
```

#### 1- 8 页面渲染

![image-20230322051558443](image/image-20230322051558443.png)

### 9_ CSS字体属性之字体系列

#### 1- 9  源码

```html
<head>
    <meta charset="UTF-8">
    <title>CSS字体属性之字体系列</title>
</head>
<style>
    h2{
        /*font-family: "Microsoft YaHei UI";*/
        font-family: "Microsoft YaHei UI";
    }
    p{
        font-family: "Times New Roman",Times,serif
    }
</style>
<body>
<h2>最幸运的幸运</h2>
<p>你问我要怎么形容你</p>
<p>空洞的词都不配比喻</p>
<p>没说完的那颗真心</p>
<p>会用余生证明</p>
<p>只给你最好看的风景</p>
<p>只给你我最大的偏心</p>
</body>
</html>
```

#### 1- 9 页面渲染

![image-20230322052506734](image/image-20230322052506734.png)

### 10_CSS字体属性之字体大小

#### 1- 10  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS字体属性之字体大小</title>
</head>
<style>
    body{
        font-size: 16px;
    }
    /*标题标签比较特殊，需要单独指定文字大小*/
    h2{
        font-size: 16px;
    }
</style>
<body>
<h2>最幸运的幸运</h2>
<p>你问我要怎么形容你</p>
<p>空洞的词都不配比喻</p>
<p>没说完的那颗真心</p>
<p>会用余生证明</p>
<p>只给你最好看的风景</p>
<p>只给你我最大的偏心</p>
</body>
</html>
```

#### 1- 10 页面渲染

![image-20230322052919013](image/image-20230322052919013.png)

### 11_CSS字体属性之字体大小

#### 1- 11  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS字体属性之字体粗细</title>
</head>
<style>
    .bold{
        /*font-weight: bold;*/
        /*这个700的后面不用跟单位 等价于 bold 都是加粗的效果*/
        /*实际开发中，我们提倡使用数字 表示加粗或者变细*/
        font-weight: 700;
    }
    h2{
        font-weight: 400;
        /*font-weight: normal;*/
    }
</style>
<body>
<h2>最幸运的幸运</h2>
<p>你问我要怎么形容你</p>
<p>空洞的词都不配比喻</p>
<p>没说完的那颗真心</p>
<p>会用余生证明</p>
<p class="bold">只给你最好看的风景</p>
<p>只给你我最大的偏心</p>
</body>
</html>
```

#### 1- 11 页面渲染

![image-20230322053945886](image/image-20230322053945886.png)

### 12_CSS字体属性之文字样式(风格)

#### 1- 12  源码

```html
<head>
    <meta charset="UTF-8">
    <title>CSS字体属性之文字样式(风格)</title>
</head>
<style>
    p{
        /*italic 浏览器会显示斜体的字体*/
        font-style: italic;
    }
    em{
        /*让倾斜的字体不用倾斜，就是赶紧脉动回来 em就是倾斜*/
        font-style: normal;
    }
</style>
<body>
<p>最幸运的幸运</p>
<em>我只喜欢肖战</em>
</body>
</html>
```

#### 1- 12 页面渲染

![image-20230322054356909](image/image-20230322054356909.png)

### 13_CSS字体属性之复合属性

#### 1- 13  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS字体属性之复合属性</title>
</head>
<style>
    /*想要div文字变倾斜 加粗 字号设置为16px 并且 是微软雅黑*/
    div{
        /*font-style: italic;
       font-weight:700;
       font-size:16px;
       font-family:"microsoft yahei" */
        /*font: font-style font-weight font-size/line-height font-family;*/
        /*font: italic 700 16px "microsoft yahei";*/
        font: 30px"黑体";
    }
</style>
<body>
<div>是非在己，得失不论，毁誉由人</div>
</body>
</html>
```

#### 1- 13 页面渲染

![image-20230322055653144](image/image-20230322055653144.png)

### 14_CSS文本外观属性之颜色

#### 1- 14  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS文本外观属性之颜色</title>
</head>
<style>
    div{
        /*color: deeppink;*/
        /*color: #cc00ff;*/
        color: blue;
    }
</style>
<body>
<div>无爱一生轻，有风无风都自由，甘愿挣脱了枷锁</div>
</body>
</html>
```

#### 1- 14 页面渲染

![image-20230322060018195](image/image-20230322060018195.png)

### 15_CSS文本外观之文字对齐

#### 1- 15  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS文本外观之文字对齐</title>
</head>
<style>
    h1{
        /*本质是让盒子里面的文字水平居中对齐*/
        /*text-align: left;right;等*/
        text-align: center;
    }
</style>
<body>
<h1>居中对齐的标题-最幸运的幸运</h1>
</body>
</html>
```

#### 1- 15 页面渲染

![image-20230322060602156](image/image-20230322060602156.png)

### 16_CSS文本外观之装饰文本

#### 1- 16  源码

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>css文本外观之装饰文本</title>
    <style>
        div{
            /*下划线*/
            /*text-decoration:underline ;*/
            /*删除线*/
            /*text-decoration:line-through ;*/
            /*上划线*/
            text-decoration: overline;
        }
        a{
            text-decoration: none;
            color: red;
        }
    </style>
</head>
<body>
<div>阳光下的星星</div>
<a href="#">最幸运的幸运</a>
</body>
</html>
```

#### 1- 16 页面渲染

![image-20230322165209788](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20230322165209788.png)

### 17_CSS文本外观之文本缩进

#### 1- 17  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS文本外观之文本缩进</title>
</head>
<style>
    p{
        font-size: 24px;
/*文本的第一行首行缩进 多少距离*/
/*text-indent: 20px;*/
/*如果此时写了2em 则是缩进当前元素 2个文字大小的距离*/
        text-indent: 2em;
    }
</style>
<body>
<p>做一个清心寡欲的侠客</p>
<p>我们都在奋斗的路上前行</p>
<p>沿途的风景一定是最美的</p>
</body>
</html>
```

#### 1- 17 页面渲染

![image-20230322142109787](image/image-20230322142109787.png)

### 18_CSS文本外观之行间距

#### 1- 18  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS文本外观之行间距</title>
</head>
<style>
    div{
        line-height: 26px;
    }
    p{
        line-height: 25px;
    }
</style>
<body>
<div>趟过山 跨过海</div>
<p>做一个清心寡欲的侠客</p>
<p>我们都在奋斗的路上前行</p>
<p>沿途的风景一定是最美的</p>
</body>
</html>
```

#### 1- 18 页面渲染

![image-20230322142735069](image/image-20230322142735069.png)

### 19_内部样式表

#### 1- 19  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>内部样式表</title>
</head>
<style>
    div{
        color: red;
    }
</style>
<body>
<div>所谓内部样式表，就是在html页面内部写样式，但是单独写到style标签里面去</div>

</body>
</html>
```

#### 1- 19 页面渲染

![image-20230322143458857](image/image-20230322143458857.png)

### 20_行内样式表

#### 1- 20  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>行内样式表</title>
</head>
<body>
<h2 style="color: red;font-size: 20px;text-indent: 2em">最幸运的幸运</h2>
<p>你问我要怎么形容你</p>
<p>空洞的词都不配比喻</p>
<p>没说完的那颗真心</p>
<p>会用余生证明</p>
<p>只给你最好看的风景</p>
<p>只给你我最大的偏心</p>
</body>
</html>
```

#### 1- 20 页面渲染

![image-20230322143714833](image/image-20230322143714833.png)

### 21_外部样式表

#### 1- 21  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>外部样式表</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<div>人生得意须尽欢，一首情歌两难</div>
</body>
</html>
```

#### 1- 21 页面渲染

![image-20230322144734053](image/image-20230322144734053.png)

### 22_综合案例-新闻页面

#### 1- 22  源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>综合案例-新闻页面</title>
</head>
<style>
    body{
        /*font-size: 16px(文字大小）/30px;（行高）*/
        font: 16px/30px "microsoft yahei";
    }
    h1{
        /*文字不加粗*/
        font-weight: 400;
        /*让h1里面的文字水平居中对齐*/
        text-align: center;
    }
    .gray{
        color: #888888;
        font-size: 12px;
        text-align: center;
    }
    a{
        text-decoration: none;
    }
    .search{
        color: #666666;
        width: 170px;
    }
    .btn{
        font-weight: 700;
    }
    p{
        /*首行缩进两个字的距离：2em*/
        text-indent: 2em;
    }
    .pic{
        /*想要图片居中对齐，则是让它的父亲p标签添加 水平居中的代码*/
        text-align: center;
    }
    .footer{
        color: #888888;
        font-size: 12px;
    }
</style>
<body>
<h1>北方高温明日达鼎盛 京津冀多地地表温度将超60℃</h1>
<div class="gray">2019-07-03 16:31:47 来源: <a href="#">中国天气网</a>　 <input type="text" value="请输入查询条件..." class="search">  <button class="btn">搜索</button></div>
<hr>
<p>中国天气网讯 今天（3日），华北、黄淮多地出现高温天气，截至下午2点，北京、天津、郑州等地气温突破35℃。预报显示，今后三天（3-5日），这一带的高温天气将继续发酵，
    高温范围以及强度将在4日达到鼎盛，预计北京、天津、石家庄、济南等地明天的最高气温有望突破38℃，其中北京和石家庄的最高气温还有望创今年以来的新高。</p>

<h4>气温41.4℃！地温66.5！北京强势迎七月首个高温日</h4>
<p class="pic"><img src="images/pic.jpeg"/></p>

<p>今天，华北、黄淮一带的高温持续发酵，截至今天下午2点，陕西北部、山西西南部、河北南部、北京、天津、山东西部、河南北部最高气温已普遍超过35℃。大城市中，北京、天津、郑州均迎来高温日。</p>

<p>在阳光暴晒下，地表温度也逐渐走高。今天下午2点，华北黄淮大部地区的地表温度都在50℃以上，部分地区地表温度甚至超过60℃。其中，河北衡水地表温度高达68.3℃，天津站和北京站附近的地表温度分别高达66.6℃和66.5℃。</p>

<h4>明日热度再升级！京津冀携手冲击38℃+</h4>

<p>中国天气网气象分析师王伟跃介绍，明天（4日），华北、黄淮地区35℃以上的高温天气还将继续升级，并进入鼎盛阶段，高温强度和范围都将发展到最强。
    明天，北京南部、天津大部、河北中部和南部、山东中部和西部、山西南部局地、河南北部、东北部分地区的最高气温都将达到或超过35℃。</p>

<p>不过，专家提醒，济南被雨水天气完美绕开，因此未来一周，当地的高温还会天天上岗。在此提醒当地居民注意防暑降温，防范持续高温带来的各种不利影响。</p>

<p class="footer">（文/张慧 数据支持/王伟跃 胡啸 审核/刘文静 张方丽）</p>
</body>
</html>
```

#### 1- 22 页面渲染

![image-20230322163010470](image/image-20230322163010470.png)
