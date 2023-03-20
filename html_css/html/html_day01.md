## day01

### 这是我的第一个html页面

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>第一个页面</title>
</head>
<body>
    这是我的第一个html页面
</body>
</html>
```

#### 页面渲染

![image-20230319160025943](image/image-20230319160025943.png)

### 利用vscode创建的页面

#### 源码



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>利用vscode创建的页面</title>
</head>
<body>
    我是谁
</body>
</html>
```

#### 页面渲染

![image-20230319161859468](image/image-20230319161859468.png)

### 标题标签

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>新闻标题</title>
</head>
<body>

</body>
</html>
```

#### 页面渲染

![image-20230319164335251](image/image-20230319164335251.png)

### 段落和换行标签

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>段落和换行标签</title>
</head>
<body>
  <p>段落标签，<br>换行标签，没有闭合标签，强制换行
  </p>

</body>
</html>
```

#### 页面渲染

![image-20230319164626491](image/image-20230319164626491.png)

### 06_体育新闻

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>新闻标题</title>
</head>
<body>
    <h1>水花61分伊戈达拉制胜抢断 西决勇士再胜开拓者总分2-0</h1>
    <h4>数据统计：水花兄弟合砍61分</h4>
    <p></p>库里22投11中，三分14投4中，罚球11罚全中得到37分8篮板8助攻，职业生涯季后赛得分30+次数来到35次，超过哈登排名现役第3位，仅次于詹姆斯和杜兰特。

    汤普森22投8中，三分8投4中得到24分3篮板2助攻，德拉蒙德-格林得到16分10篮板7助攻5盖帽，凯文-鲁尼得到14分7篮板2助攻，今天勇士有7名替补出场。</p>

    <h4>兄弟对决升级：小库里给哥哥造成压力</h4>
    <p>库里兄弟是NBA历史上第一对在分区决赛相遇的兄弟。在西决第1场中，小库里没有给哥哥造成压力，他出场19分钟，7投1中只得到3分3篮板2助攻，在场期间输掉10分。</p>
    <p>作者: pink老师</p><br/>
    <p>2019-8-8</p>
</body>
</html>
```

#### 页面渲染

![image-20230320033747629](image/image-20230320033747629.png)

### 07-文本格式化标签

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>文本格式化标签</title>
</head>
<body>
    我是<strong>加粗</strong>的文字
    我是<b>也是加粗</b>的文字
    我是<em>倾斜</em>嗯们 歪了的文字
    我是<del>删除线</del>要不你还是把我删了吧的文字 得了del就是删除
    我是<s>删除线</s> 不是你死就是我死 都想生，S就是删除线
    我是<u>下划线</u> 有点under的意思，下划线就是u
</body>
</html>
```

#### 页面渲染

![image-20230320034709540](image/image-20230320034709540.png)

### 08-div和span标签

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>div和span标签</title>
</head>
<body>
  <div>我是一个div标签，我一个人单独占一行</div> 没有语意，就是喜欢独处，装内容的大盒子
  <div>我是一个div标签，我一个人单独占一行</div> 表示分割
  <span>百度</span> 我也没有语意，我是可以和大家一起生活在一排的小盒子
  <span>新浪</span> 我可以跨度和跨行
  <span>搜狐</span>
</body>
</html>
```

#### 页面渲染

![image-20230320035740980](image/image-20230320035740980.png)

### 09-图像标签

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图像标签</title>
</head>
<body>
  <h4>图像标签的使用：</h4>
<img src="xz.jpg"/>
<h4>alt 替换文本 图像显示不出来的时候用文字替换：</h4>
<img src="xz.jpg" alt="我是肖战老婆"/>
<h4>title 提示文本 鼠标放到头像上，提示的文字：</h4>
<img src="xz.jpg" title="我是肖战老婆棒棒哒" alt="我是肖战老婆"/>

<h4> width 给图像设定宽度：</h4>
<img src="xz.jpg" alt="我是肖战老婆" title="我是肖战老婆" width="520"/>
<h4>height 给图像设定高度：</h4>
<img src="xz.jpg" alt="我是肖战老婆" title="我是肖战老婆" height="105"/>
<img src="xz.jpg" alt="我是肖战老婆" title="我是肖战老婆" width="520" border="15"

</body>
</html>
```

#### 页面渲染

![image-20230320043747414](image/image-20230320043747414.png)

### 10-demo

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>图像标签demo</title>
</head>
<body>
<h4>图像标签属性需要注意的点：</h4>
<p>图像标签拥有多个属性，必须在标签名的后面</p>
<img src="xz.jpg"  title="我是肖战老婆" width="520"/>
<img src="xz.jpg"  title="我是肖战老婆" height="105"/>

<p>属性之间不分先后顺序，标签名与属性、属性与属性之间均以空格分开</p>
<img src="xz.jpg"  title="我是肖战老婆" alt="我是肖战老婆"/>
<img src="xz.jpg"  alt="我是肖战老婆" title="我是肖战老婆" />
<p>属性采取键值对的格式，即key= "value",即属性="属性值"</p>

<h4>图像标签重点掌握点：</h4>
<p>第一个，src属性是一定要写的，它决定引入那张照片或者哪个路径</p>
<p>第二个，alt和title的区别是：<br/>首先出现的时机不一样；alt为替换文本，
    当图片显示不出来，alt文本直接显示在网页中；<br/> title是提示文本，鼠标放在照片上会有文本提示</p>
</body>
</html>
```

#### 页面渲染

![image-20230320050644997](image/image-20230320050644997.png)

### 11-同一级路径

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>相对路径-同一级路径</title>
</head>
<body>
<h4>相对路径:以引用文字所在位置为参考，而建立出的目录路径</h4>
<p>就是图片相对于html页面的位置</p>
 <h4>同一路径显示为：</h4>
<img src="xz1.jpg"/>
<p></p>在同一个文件夹里面，图像文件位于html文件同一级，无需转换，
 可以直接输入src=xz.jpg 反引号</p>
</body>
</html>
```

页面渲染

![image-20230320055418320](image/image-20230320055418320.png)

### 12-下一级路径

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>相对路径-下一级路径</title>
</head>
<body>
<h4>相对路径:以引用文字所在位置为参考，而建立出的目录路径</h4>
<p>就是图片相对于html页面的位置</p>
<h4>下一路径显示为：</h4>
    <img src="image/xz1.jpg">
<p>此文件和image处于同一路径下，而图片属于image目录里的子文件时</p>
<p>图像文件位于html文件下一级，图片代码为：image/xz1.jpg(某照片）</p>
</body>
</html>
```

#### 页面渲染

![image-20230320055652864](image/image-20230320055652864.png)

### 上一级路径

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>相对路径-上一级路径</title>
</head>
<body>
<h4>相对路径:以引用文字所在位置为参考，而建立出的目录路径</h4>
<p>就是图片相对于html页面的位置</p>
<h4>上一路径显示为：</h4>
<img src="../image/xz1.jpg"/
>
<p>图像文件和html文件夹处于同一路径下，而.html属于html目录里的子文件时</p>
<p>图像文件位于html文件上一级，图片代码为：../image/xz1.jpg(某照片）</p>
</body>
</html>
```

####  页面渲染

![image-20230320061325756](image/image-20230320061325756.png)

![image-20230320061734932](image/image-20230320061734932.png)

### 13-绝对路径



#### 源码

#### 页面渲染

### 14-超链接标签

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接标签</title>
</head>
<body>
<h4>1.外部链接</h4>
<a href="http://www.qq.com" target="_blank">腾讯</a>
target 打开窗口的方式 默认的值是_self 当前窗口打开页面 _blank 新窗口打开页面
<h4>2.内部链接：网站内部页面之间的相互链接</h4>
<a href="http://www.itcast.cn" target="_blank">公司简介</a>
<h4>3.空链接：#</h4>
<a href="#">公司地址</a>
<h4>4.下载链接：地址复制链接的是 文件 .exe 或者是 zip 等压缩包形式</h4>
<a href="img.zip">下载文件</a>
<h4>5.网页元素的链接</h4>
<a href="http://www.baidu.com"><img src="xz1.jpg">/a>
</body>
</html>
```

#### 页面渲染

![image-20230320065010522](image/image-20230320065010522.png)

### 15-锚点定位

#### 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>锚点定位</title>
</head>
<body>
<h2>目录</h2>
1 早年经历<br/>
2 演艺经历<br/>
3 <a href="#live">个人生活</a><br/>
4 <a href="#zuopin">主要作品</a><br/>
5 社会活动<br/>
6 获奖记录<br/>
7 人物评价<br/>

<h3>早年经历</h3>

<p >肖战，1991年10月5日出生于重庆市，中国内地男演员、歌手。肖战的父母原本想给肖战取名为“肖赞”，但母亲担心“赞”字难写，父亲就把“赞”改成了“战”。肖战的父亲很注重肖战除了文化以外的兴趣爱好培养，所以在肖战小时候让他学习很多东西，如画画、小提琴等。</p>
<img src="xz1.jpg">
<h3>演艺经历</h3>

<p>2015年，以选手的身份参加浙江卫视才艺养成选秀节目《燃烧吧少年》。</p>

<h3 id="live">个人生活</h3>

<p>热爱学习，热爱旅游，热爱生活，感情经历：以前都是过去试，现在我只有他，他老婆只有我，双向奔赴。</p>

<h3 id="zuopin">主要作品</h3>

<p>陈情令。余生请多指教，斗罗大陆，狼殿下，王牌部队，待播：梦中的那片海，玉骨遥，骄阳伴我等</p>

<h3>社会活动</h3>

<p>1月31日，由北京市人民政府新闻办公室主办，中国新闻网承办，北京市教育委员会支持，北京市第二外国语学院协办的“相约冬奥·i Beijing——爱上北京的100个理由短视频征集大赛”启动，肖战担任宣推官，邀请大家并分享与北京的故事。 </p>
<p>2月3日，腾讯奥运报道星运电台冬奥季宣布肖战担任2月17日腾讯冬奥报道雪舞官，为冬奥健儿加油，为冰雪运动喝彩。</p>
<p>9月7日，为驰援甘孜州泸定县地震灾区，肖战通过甘孜藏族自治州红十字会向四川泸定捐款100万元。</p>

<h3>获奖记录</h3>

<p>腾讯视频星光大赏年度人气电视剧演员；百度沸点年度演员；太多了</p>

<h3>人物评价</h3>

<p>肖战是一个特别纯净的人，所以他的眼睛看起来很干净；同时，他也是一个很有天赋的演员。从《最美表演》短片合作中能看出他在拍摄前做了很多的功课。拍摄时肖战特别松弛，并没有把任何的表演痕迹加在这个角色人物里面。比如拍《买耳朵》饰演外卖小哥前，肖战观察生活中的外卖小哥。拍摄时肖战没有所谓的包袱，不化妆、不刮胡子、不做头发，完全去服务人物（导演苏伦评）。</p>
</body>
</html>
```

#### 页面渲染

![image-20230320072000259](image/image-20230320072000259.png)

### 16-注释标签和特殊字符

#### 源码

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>注释标签和特殊字符</title>
</head>
<body>
<h4>注释</h4>
如果需要在html文档中添加一些便于阅读和理解。但又不需要显示在页面中的注释文字，就需要使用注释标签<br/>
总的来说方便自己和他人查阅更改,在程序中不会显示出来
    <!--一夜暴富-->
注释以“ <&it;!--”开头，以“--&gt;”结束
<h4>快捷键：Ctrl + /</h4>
空格& nbsp冒号：&nbsp;(几个空格就加几个）
</body>
</html>
```

#### 页面渲染

![image-20230320074134365](image/image-20230320074134365.png)
