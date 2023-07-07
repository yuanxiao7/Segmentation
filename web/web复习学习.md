## web复习学习

[教程-前后端基础知识](https://space.keter.top/docs/others/%E5%89%8D%E5%90%8E%E7%AB%AF/%E6%89%93%E6%AF%94%E8%B5%9B%E5%BF%85%E5%A4%87%E7%9A%84%E5%89%8D%E5%90%8E%E7%AB%AF%E7%9F%A5%E8%AF%86)

[视频链接](https://www.bilibili.com/video/BV1mM4y1N779/?spm_id_from=333.337.search-card.all.click&vd_source=a9c7c4d1d0286db11338144169a58869)



## 实战操作

1. 用html语言写标题，传图片，写静态按键
2. 使用CSS来辅助HTML的位置

### web小demo1

<img src="C:\Users\Happy\AppData\Roaming\Typora\typora-user-images\image-20230706215154987.png" alt="image-20230706215154987" style="zoom:50%;" />



代码实现如下

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mnist手写数字识别</title>
    <style>
        .b{
            text-align: center;
        }
    </style>
    <style>
        #a{
            text-align: center;
            /*display: table-cell;*/
            /*vertical-align: middle;*/
            /*width: 2000px;*/
            /*height: 400px;*/
            background: aquamarine;
        }
        #img{
            width: 300px;
            height: 300px;
        }
    </style>
</head>
<body>

    <h1 align="center">Mnist手写数字识别</h1>
<!--    <img src="https://blog.keter.top/img/touxiang.png" alt="一张神奇的图">-->
    <p id="a">
        <img src="https://blog.keter.top/img/touxiang.png" alt="一张神奇的图" id="img">
    </p>

    <p class="b">
        <input type="file" name="file">
        <input type="button" value="上传">
        <br />
        <br />
        识别结果
    </p>
</body>
</html>
```

1. 通过在body写 <p id="a">  html语言  </p>

   在head 写<style>绑定id或class 设置信息 <style> 来实现指定图片，按键居中

2. 文本居中 直接在<h1 设置align >  <h1> 即可

3. 换行 <br />或者是直接把要换行的内容写在<div>里面

4. 其实<p></p>和<div></div>用法相似，可以把html语言包在里面

5. 然后在<img 这里可以添加图片地址src 释义alt 绑定的id 然后在head就可以用style来设置相应的信息

   



教程答案如下

<img src="C:\Users\Happy\AppData\Roaming\Typora\typora-user-images\image-20230706220334865.png" alt="image-20230706220334865"  />



### web小demo2

下面是JavaScript语言运用

- 同样的，JavaScript也是插入到HTML语言里面用的，它用于逻辑实现
- 他必须包在<script>里面<script>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mnist手写数字识别</title>
    <style>
        .b{
            text-align: center;
        }
    </style>
    <style>
        #a{
            text-align: center;
            /*display: table-cell;*/
            /*vertical-align: middle;*/
            /*width: 2000px;*/
            /*height: 400px;*/
            background: aquamarine;
        }
        #img{
            width: 300px;
            height: 300px;
        }
    </style>
</head>
<body>

    <h1 align="center">Mnist手写数字识别</h1>
<!--    <img src="https://blog.keter.top/img/touxiang.png" alt="一张神奇的图">-->
    <p id="a">
        <img src="https://blog.keter.top/img/touxiang.png" alt="一张神奇的图" id="img">
    </p>

    <p class="b">
        <input type="file" name="file">
        <input type="button" value="上传">
        <br />
        <br />
        识别结果
    </p>
<script>
    // alert("⚠未知操作");  //弹窗
    var len = 16;
    var x = 1;
    var sun = len + x;
    var person = {firstName: "John", lastName: "Doe"};
    console.log(person.firstName)
    console.log(sun)     

    function myFunction(a, b){
        return a*b;
    }

    console.log("3, 4相乘的结果为：", myFunction(3, 4))  // 可以将结果输出在web控制台显示
</script>
</body>
</html>
```



web展示如下

<img src="C:\Users\Happy\AppData\Roaming\Typora\typora-user-images\image-20230706222740092.png" alt="image-20230706222740092" style="zoom: 67%;" />





下面是jQuery触发按键绑定

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Mnist手写数字识别</title>
    <style>
        .b{
            text-align: center;
        }
    </style>
    <style>
        #a{
            text-align: center;
            /*display: table-cell;*/
            /*vertical-align: middle;*/
            /*width: 2000px;*/
            /*height: 400px;*/
            background: aquamarine;
        }
        #img{
            width: 300px;
            height: 300px;
        }
    </style>
<!--    下面这个src是引入jQuery这个包-->
    <script src="https://cdn.staticfile.org/jquery/1.8.3/jquery.js"></script>
</head>
<body>

    <h1 align="center">Mnist手写数字识别</h1>
<!--    <img src="https://blog.keter.top/img/touxiang.png" alt="一张神奇的图">-->
    <p id="a">
        <img src="https://blog.keter.top/img/touxiang.png" alt="一张神奇的图" id="img">
    </p>

    <p class="b">
        <input type="file" name="file">
        <input type="button" value="上传">
        <br />
        <br />
        识别结果
        <br />
        <br />
         <button onclick="fun()">fun1</button>
        <button id="b1">fun2</button>
    </p>

<script>
    // alert("⚠未知操作");
    var len = 16;
    var x = 1;
    var sun = len + x;
    var person = {firstName: "John", lastName: "Doe"};
    console.log(person.firstName)
    console.log(sun)

    function myFunction(a, b){
        return a*b;
    }
    console.log("3, 4相乘的结果为：", myFunction(3, 4))

    // 按键绑定1
    function fun()
    {
        alert("按钮设置成功！")
    }

    // 这种设置比较常见 触发后将按键原本的字改成现在html中的字
    $('#b1').click(function (){
        $('#b1').html('啊哈哈哈哈，搞定！')
    })
</script>
</body>
</html>
```

第一种是click绑定function

第二种是id绑定click调用function

具体实现如上述代码

明天接着学习Ajax   然后算法与前后端对接  后面接着写 面积 体积 直径获取  以及病灶检测，并打印最后的见过报告单，加油！