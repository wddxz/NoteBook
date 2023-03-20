## day02

### 1-1 表格的基本语法

#### 1-1 源码

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>表格基本语法</title>
</head>
<body>
<h4>表格的作用</h4>
 <p>因为它可以让数据显示的非常的规整。主要用于显示，展示数据</p>
<p><b>table</b>:用于定义表格的标签，<br/>
    <b>tr</b>:定义表格中的行,必须嵌套在table标签中使用<br/>
    <b>td</b>:定义表格中的单元格，就是单元格内的文字，必须嵌套在tr中使用</p>
    <table>
        <tr> <td> 姓名 </td>  <td> 性别 </td>  <td> 年龄 </td></tr>
        <tr> <td> 肖战 </td>  <td> 男 </td>  <td> 32 </td></tr>
        <tr> <td> 刘德华 </td>  <td> 男 </td>  <td> 56 </td></tr>
        <tr> <td> 张学友 </td>  <td> 男 </td>  <td> 58 </td></tr>
        <tr> <td> 肖战老婆 </td>  <td> 女 </td>  <td> 28 </td></tr>
    </table>


</body>
</html>
```

#### 页面渲染

![image-20230320164641331](image/image-20230320164641331.png)

### 1-2 表头单元格标签

#### 1-2 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表头单元格标签</title>
</head>
<body>
<h4>表头单元格的使用</h4>
<p><b>th：位于表格的第一行或者第一列，在表头单元格里面文本内容加粗居中显示,也是嵌套在tr中使用</b></p>
<table>
    <tr> <th> 姓名 </th>  <th> 性别 </th>  <th> 年龄 </th></tr>
    <tr> <td> 肖战 </td>  <td> 男 </td>  <td> 32 </td></tr>
    <tr> <td> 刘德华 </td>  <td> 男 </td>  <td> 56 </td></tr>
    <tr> <td> 张学友 </td>  <td> 男 </td>  <td> 58 </td></tr>
    <tr> <td> 肖战老婆 </td>  <td> 女 </td>  <td> 28 </td></tr>
</table>

</body>
</html>
```

#### 页面渲染

![image-20230320165412538](image/image-20230320165412538.png)

### 1-3 表格属性

#### 1-3 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表格属性</title>
</head>
<body>
<!--表格属性要写到表格标签table里面去-->
<!--实际开发不用，目的是记住后，后面css会使用-->
<table align="center" border="1" cellpadding="0" cellspacing="0" width="520" height="251" >
    <tr> <th> 姓名 </th>  <th> 性别 </th>  <th> 年龄 </th></tr>
    <tr> <td> 肖战 </td>  <td> 男 </td>  <td> 32 </td></tr>
    <tr> <td> 刘德华 </td>  <td> 男 </td>  <td> 56 </td></tr>
    <tr> <td> 张学友 </td>  <td> 男 </td>  <td> 58 </td></tr>
    <tr> <td> 肖战老婆 </td>  <td> 女 </td>  <td> 28 </td></tr>
</table>
</body>
</html>
```

#### 页面渲染

![image-20230320170650871](image/image-20230320170650871.png)

### 1-4 今日小说排行榜

#### 1-4 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>今日小说排行榜</title>
</head>
<body>
<!--这里的table不能有闭合标签-->
  <table align="center" width="500" height="249" border="1" cellspacing="0">
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
        <td>1</td>
        <td>剑来</td>
        <td><img src="down.jpg" ></td>
        <td>456</td>
        <td>123</td>
        <td><a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a></td>
    </tr>

    <tr>
        <td>2</td>
        <td>遮天</td>
        <td><img src="up.jpg" ></td>
        <td>234</td>
        <td>123</td>
        <td><a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a></td>
    </tr>

    <tr>
        <td>3</td>
        <td>斗罗</td>
        <td><img src="up.jpg" ></td>
        <td>456</td>
        <td>123</td>
        <td><a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a></td>
    </tr>
</tbody>
</body>
</html>
```

#### 页面渲染

![image-20230321051104380](image/image-20230321051104380.png)

### 1-5 合并单元格

#### 1-5 源码

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>合并单元格</title>
</head>
<body>
<table width="500" height="249" border="1" cellspacing="0">
<tr>
    <td></td>
    <td colspan="2"></td>

</tr>
<tr>
    <td rowspan="2"></td>
    <td></td>
    <td></td>
</tr>
<tr>

    <td></td>
    <td></td>
</tr>
</body>
</html>
```

#### 页面渲染

![image-20230321051819938](image/image-20230321051819938.png)

### 1-6 无序列表

#### 1-6 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无序列表</title>
</head>
<body>
    <h4>我最喜欢的食物？</h4>
<ul>
    <li>榴莲</li>
    <li>芝士</li>
    <li>奶油</li>
    <li>
        <p>123</p>
    </li>
</ul>

</body>
</html>
```

#### 页面渲染

![image-20230321052733052](image/image-20230321052733052.png)

### 1-7 有序列表

#### 1-7 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>有序列表(理解)</title>
</head>
<body>
<h4>粉丝排行榜</h4>
<ol>
    <li>肖战 3052万</li>
    <li>孙燕姿 2001万</li>
    <li>张国荣 3520万</li>
</ol>

</body>
</html>
```

#### 页面渲染

![image-20230321053006532](image/image-20230321053006532.png)

### 1-8 自定义列表(重点)

#### 1-8 源码

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>自定义列表(重点)</title>
</head>
<body>
    <dl>
        <dt>关注我们</dt>
        <dd>新浪微博</dd>
        <dd>官方微信</dd>
        <dd>联系我们</dd>
        <dt>关注我们</dt>
        <dd>新浪微博</dd>
        <dd>官方微信</dd>
        <dd>联系我们</dd>
    </dl>

</body>
</html>
```

#### 页面渲染

![image-20230321053437275](image/image-20230321053437275.png)

### 1-9 表单域

#### 1-9 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单域(了解)</title>
</head>
<body>
    <form action="demo.php" method="post" name="name1">
<table width="500" hright="249" border="1" cellspacing="0">
    <tr>
    <th>属性</th>
        <th>属性值</th>
        <th>作用</th>
    </tr>
   from标签：用于定义表单域，以实现用户信息的收集和传递</br>
    会把它范围内的表单元素信息交给服务器。
    <td>action</td>
    <td>url地址</td>
    <td>用于指定接收并处理表单数据的服务器程序的url地址</td>
    </tr>

    <tr>
        <td>method</td>
        <td>get/post</td>
        <td>用于设置表单数据的提交方式，其取值为get或post</td>
    </tr>

    <tr>
        <td>name</td>
        <td>名称</td>
        <td>用于指定表单的名称，以区分同一个页面中的多个表单域</td>
    </tr>

</body>
</html>
```

#### 页面渲染

![image-20230321060940244](image/image-20230321060940244.png)

### 1-10 input 表单元素

#### 1-10 源码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>input 表单元素</title>
</head>
<body>
    <form action="xxx.php" method="get">
<!--        text 文本框 用户可以里面输入任何文字-->
    用户名：<input type="text" name="username" value="请输入用户名" maxlength="6">
<!--password 密码框 用户看不见密码-->
        密码：<input type="password" name="pwd" ></br>
<!-- radio 单选按钮 可以实现多选-->
<!-- name 是表单元素名字 这里性别按钮单选按钮必须有相同的名字name 才可以实现多选1  -->
<!--单选按钮和复选框可以设置checked 属性，当页面打开的时候就可以默认这个按钮-->
        性别：男<input type="radio" name="sex" value="男"> 女 <input type="radio" name="sex" value="女" checked="checked">人妖<input type="radio" name="sex" value="人妖">
<!--     checkbox 复选框 可以实现多选   -->
        爱好：吃饭<input type="checkbox" name="hobby" value="吃饭">睡觉<input type="checkbox" name="hobby">打豆豆<input type="checkbox" name="hobby" checked="checked">
        <br>
<!--点击了提交按钮，可以把表单域form里面的表单元素 里面的值 提交给后台服务器-->
  <input type="submit" value="免费注册">
<!--    重置按钮可以还原表单元素初始的默认状态-->
    <input type="reset" value="重新填写">
<!--普通按钮 button 后期结合JS搭配使用-->
<input type="button" value="获取短信验证码"><br>
<!--文件域 使用场景 上传文件使用的-->
上传头像：<input type="file">
    </form>
</body>
</html>
```

#### 页面渲染

![image-20230321065724581](image/image-20230321065724581.png)

### 1-11 label标签

#### 1-11 源码

#### 页面渲染

### 1-12 select下拉表单

#### 1-12 源码

#### 页面渲染

### 1-13 textarea 文本域

#### 1-13 源码

#### 页面渲染

### 1-14 综合案例-注册页面

#### 1-14 源码

#### 页面渲染





