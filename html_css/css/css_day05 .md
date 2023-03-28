## day05-第一次网页制作css

### 1-1 

#### 1-1 源码

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>学成在线网页</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<div class="header w">
<!--    1.头部开始了-->
<!-- 第一行logo部分-->
    <div class="logo">
        <img src="images/logo.png" alt="">
    </div>
<!--    第一行导航栏部分-->
    <div class="nav">
        <ul>
            <li><a href="#">首页</a></li>
            <li><a href="#">课程</a></li>
            <li><a href="#">职业规划</a></li>
        </ul>
    </div>
<!--    第一行搜索模块-->
    <div class="search">
        <input type="text" value="输入关键词">
        <button></button>
    </div>
<!--    第一行用户模块-->
    <div class="user">
        <img src="images/user.png">
        qq-lilei
    </div>
</div>
<!--    头部区结束啦-->
<!--    2.banner部分start-->
<div class="banner">
    <div class="w">
        <div class="subnav">
            <ul>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
                <li><a href="#">前端开发 <SPAN> &GT </SPAN></a></li>
            </ul>
        </div>

<!--        course 课程表模块-->
        <div class="course">
            <h2>我的课程表</h2>
            <div class="bd">
                <ul>
                    <li><h4>继续学习 程序语言设计</h4>
                        <p>正在学习-使用对象</p>
                    </li>
                    <li><h4>继续学习 程序语言设计</h4>
                        <p>正在学习-使用对象</p>
                    </li>
                    <li><h4>继续学习 程序语言设计</h4>
                        <p>正在学习-使用对象</p>
                    </li>
                </ul>
                <a href="#" class="more">全部课程</a>
            </div>

        </div>
    </div>
</div>
<!--    .banner部分ending-->
<!--3.精品推荐模块start-->
<div class="goods w">
    <h3>精品推荐</h3>
    <ul>
        <li><a href="#">jQuery</a></li>
        <li><a href="#">jQuery</a></li>
        <li><a href="#">jQuery</a></li>
        <li><a href="#">jQuery</a></li>
        <li><a href="#">jQuery</a></li>
    </ul>
    <a href="#" class="mod">修改兴趣</a>

</div>
<!--3.精品推荐模块end-->
<!--4.box核心内容区域开始了-->
<div class="box w">
    <div class="box-hd">
        <h3>精品推荐</h3>
        <a href="#">查看全部</a>
    </div>
    <div class="box-bd">
        <ul class="clearfix">
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
            <li>
                <img src="images/pic.png" alt="">
                <h4>
                    Think PHP 5.0 博客系统实战项目演练
                </h4>
                <div class="info">
                    <span>高级</span>• 1125人在学习
                </div>
            </li>
        </ul>
    </div>


</div>
<!--4.box核心内容区域结束了-->
<div class="footer">
    <div class="w">
        <div class="copyright">
            <img src="images/logo.png">
            <p>学成在线致力于普及中国最好的教育它与中国一流大学和机构合作提供在线课程。<br>
          © 2017年XTCG Inc.保留所有权利。-沪ICP备15025210号</p>
            <a href="#" class="app">下载APP</a>
        </div>
        <div class="links">
            <dl>
                <dt>关于学成网</dt>
                <dd><a href="#">关于</a></dd>
                <dd><a href="#">管理团队</a></dd>
                <dd><a href="#">工作机会</a></dd>
                <dd><a href="#">客户服务</a></dd>
                <dd><a href="#">帮助</a></dd>
            </dl>
            <dl>
                <dt>关于学成网</dt>
                <dd><a href="#">关于</a></dd>
                <dd><a href="#">管理团队</a></dd>
                <dd><a href="#">工作机会</a></dd>
                <dd><a href="#">客户服务</a></dd>
                <dd><a href="#">帮助</a></dd>
            </dl>
            <dl>
                <dt>关于学成网</dt>
                <dd><a href="#">关于</a></dd>
                <dd><a href="#">管理团队</a></dd>
                <dd><a href="#">工作机会</a></dd>
                <dd><a href="#">客户服务</a></dd>
                <dd><a href="#">帮助</a></dd>
            </dl>
        </div>
    </div>
</div>
</body>
</html>
```

#### 



### 1-2 

#### 1-2 源码

```css
*{
    margin: 0;
    padding: 0;
}
.w{
    width: 1200px;
    margin: auto;
}
body{
    background-color: #f3f5f7;
    height: 3000px;
}
li{
    list-style: none;
}
a{
    text-decoration: none;
}
.clearfix:before,.clearfix:after {
    content:"";
    display:table;
}
.clearfix:after {
    clear:both;
}
.clearfix {
    *zoom:1;
}

.header{
    height: 42px;
    /*background-color: pink;*/
    /* 注意此地方会层叠 w 里面的margin */
    margin: 30px auto;
}
.logo{
    float: left;
    width: 198px;
    height: 42px;
}
.nav{
    float: left;
    margin-left: 60px;
}
.nav ul li{
    float: left;
}
.nav ul li a{
    display: block;
    height: 42px;
    padding: 0 10px;
    line-height: 42px;
    font-size: 18px;
    color: #050505;
}
.nav ul li a:hover{
    border-bottom: 2px solid #00a4ff;
    color: #00a4ff;
}
/*search搜索模块*/
.search{
    float: left;
    width: 412px;
    height: 42px;
    margin-left: 50px;
}
.search input{
    float: left;
    width: 345px;
    height: 40px;
    border: 1px solid #00a4ff;
    border-right: 0;
    color: #bfbfbf;
    font-size: 14px;
    padding-left: 15px;
}
.search button{
    float: left;
    width: 40px;
    height: 42px;
    /* 按钮button默认有个边框需要我们手动去掉 */
    border: 0;
    background: url("images/btn.png");
}
.user{
    float: right;subnav
    line-height:42px;
    margin-right: 60px;
    font-size: 14px;
    color: #666;
}
/*banner*/
.banner{
    height:421px ;
    background-color: #1c036c;
}
.banner .w{
    height: 421px;
    background: url("images/banner2_qiqiu.png") no-repeat top center;
}
.subnav{
    float: left;
    width: 190px;
    height: 421px;
    background: rgba(0,0,0,.3);
}
.subnav ul li{
    height: 45px;
    line-height: 45px;
    padding: 0 20px;
}
.subnav ul li a{
    font-size: 14px;
    color: #fff;
}
.subnav ul li a span{
    float: right;
}
.subnav ul li a:hover{
    color: #00a4ff;
}
.course{
    float: right;
    width: 230px;
    height: 300px;
    background-color: #fff;
    /*浮动的盒子不会有外边距合并的问题*/
    margin-top: 50px;
}
.course h2{
    height: 48px;
    background-color: #9bceea;
    text-align: center;
    line-height: 48px;
    font-size: 18px;
    color: #fff;
}
.bd{
    padding: 0 20px;
}
.bd ul li{
    padding: 14px 0;
    border-bottom: 1px solid #ccc;
}
.bd ul li h4{
    font-size: 16px;
    color: #4e4e4e;
}
.bd ul li p{
    font-size: 12px;
    color: #a5a5a5;
}
.bd .more{
    display: block;
    height: 38px;
    border: 1px solid #00a4ff;
    text-align: center;
    line-height: 38px;
    color: #00a4ff;
    font-size: 16px;
    font-weight: 700;
}
/*精品推荐模块*/
.goods{
    height: 60px;
    background-color: #fff;
    margin-top: 10px;
    box-shadow: 0 4px 3px 3px rgba(0,0,0,.1);
    /*行高会继承给三个孩子*/
    line-height: 60px;
}
.goods h3{
    float: left;
    margin-left: 30px;
    margin-right:30px;
    font-size: 16px;
    color: #00a4ff;
}
.goods ul{
    float: left;
}
.goods ul li{
    float: left;
}
.goods ul li a{
    padding: 0 30px;
    font-size: 16px;
    color:#050505 ;
    border-left:1px solid #ccc ;
}
.mod{
    float: right;
    margin-right: 30px;
    font-size: 14px;
    color: #00a4ff;
}
/*4.box核心内容区域开始了*/
.box{
    margin-top: 30px;
}
.box-hd{
    height: 45px;
}
.box-hd h3{
    float: left;
    font-size: 20px;
    color: #494949;
}
.box-hd a{
    float: right;
    font-size: 12px;
    color: #a5a5a5;
    margin-top: 10px;
    margin-right: 30px;
}
/* 把li 的父亲ul 修改的足够宽一行能装开5个盒子就不会换行了 */
.box-bd ul{
    width: 1225px;
}
.box-bd ul li{
    float: left;
    width: 228px;
    height: 270px;
    background-color: #fff;
    margin-right: 15px;
    margin-bottom: 15px;
}
.box-bd ul li img{
    width: 100%;

}
.box-bd ul li h4{
    font-size: 14px;
    color: #050505;
    font-weight: 400;
    margin: 20px 20px 20px 25px;
}
.box-bd .info{
    font-size: 12px;
    color: #999;
    margin: 0 20px 0 25px;
}
.box-bd .info span{
    color:#ff7c2d ;
}
.footer{
    height: 451px;
    background-color: #ffffff;
}
.footer .w{
   padding-top: 35px;
}
.copyright{
    float: left;
}
.copyright p{
    font-size: 12px;
    color: #666;
    margin: 20px 0 15px 0px;
}
.copyright .app{
    display: block;
    width: 118px;
    height: 33px;
    font-size: 16px;
    border: 1px solid #00a4ff;
    text-align: center;
    line-height: 33px;
    color:  #00a4ff;
}
.links{
    float: right;
}
.links dl{
    float: left;
    margin-left: 100px;
}
.links dl dt{
    font-size: 16px;
    color: #333333;
    margin-top: 5px;
}
.links dl dd a{
    font-size: 12px;
    color: #333333;
}
```

#### 1-2 页面渲染

![image-20230328170443527](image/image-20230328170443527.png)

#### 1-3 页面渲染

![image-20230328170517641](image/image-20230328170517641.png)

#### 1-4 页面渲染

![image-20230328170558455](image/image-20230328170558455.png)

### 

