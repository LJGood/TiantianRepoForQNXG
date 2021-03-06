# HTML入门笔记

## 1. 初识网页的结构

### W3C标准

- 结构：HTML
  - HTML用于描述页面的结构
- 表现：CSS
  - CSS用于控制页面中元素的样式
- 行为：JavaScript
  - JavaScript用于响应用户操作

## 2. html简介

- HTML是超文本标记语言
- <标签名>内容</标签名>
  - `<h1>` `</h1>`
  - `<h2>` `</h2>`
  - `<p>` `</p>`

```html
<h1>
    回乡偶书（二首）
</h1>
<h2>
    其一
</h2>
<p>
    少小离家老大回
</p>
<p>
   	乡音无改鬓毛衰
</p>
<p>
    儿童相见不相识
</p>
<p>
    笑问客从何处来
</p>
```

- 根标签
  - `<html>` `</html>`
- 子标签
  - `<head>` `</head>`
    - `<title>` `</title>` （是html的后代）（html是它的祖先）
  - `<body>` `</body>`
- 自结束标签
  - `<img>`
  - `<input>`
  - 也可以写成对的
    - `<img>` `<img />`
    - 但推荐只写一个

## 3. 标签的属性

- 属性，在开始标签或者自结束标签中可以设置属性
- 属性是一个名值对
- 属性用来设置标签中的内容如何显示
- 属性和标签名或其他属性应该使用空格隔开
- 属性不能瞎写，应该根据WC3文档中的规定来写
  - 有些属性有属性值
  - 有些没有
  - 如果有属性
  - 属性应该用引号引起来
  - 单引号和双引号都行

```html
<h1>这是我的<font color="red" siez="3">第三个</font>网页</h1>
```



## 4. 文档声明（doctype)

- 文档声明来告诉浏览器当前网页的版本
- html5的文档声明
- `<!doctype html>`
- 大写小写都无所谓
- `<!DOCTYPE html>`
- 文档声明写在网页最上面
- 浏览器看到后就知道用html5的标准来渲染



## 5. 字符编码

### 5.1. 简介

- 编码，将字符转换成二进制码的过程称为编码
- 解码，将二进制码转换为字符的过程成为解码
- 字符集，编码解码采用的规范叫做字符集
- 如果编码解码分别采用不同就会出现乱码问题
- 常见字符集（ASCII，GBK，UTF-8）
- 万国码——UTF-8 全世界通用

### 5.2. 避免网页乱码

- `<meta charset = "utf-8">`
- 网页保存时编码规则要和上面设置内容一致



## 6. 网页基本结构

### 6.1 样例

```html
<!-- 文档声明，声明当前网页的版本是html5 -->
<!DOCTYPE html>
<!-- 表明网页语言，如果是en，chrome会提示是否翻译，改成ch意思是中文就不会烦人了 -->
<html lang="en"> 
<!-- html根标签，网页所有内容都要写在根元素里面 -->
<html>
    <!-- head是网页的头部，head中的内容不会在网页中直接出现，主要用来帮助浏览器或搜索引擎来解析网页 -->
    <head>
        <!-- meta标签用来设置网页的元元素,这里设置网页字符集，避免乱码 -->
        <meta charset="utf-8">
        <!-- 这个是设置网页缩放等级，暂时用不到，不进行过多解释 -->
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <!-- title中的内容会显示在浏览器的标题栏，搜索引擎会主要根据title中的内容来判断网页的主要内容 -->
        <title>这是我的第四个网页</title>
    </head>

    <!-- body是html的子元素，表示网页的主题，网页中所有的可见内容都应该写在body里 -->
    <body>
        <!-- h1是网页一级标题 -->
        <h1>这是我的第四个网页</h1>
    </body>
</html>
```

### 6.2 实体

<<<<<<< HEAD
[实体.html](../Codes/05_实体.html)    (网页超链接记得右键看源码，或F12调试工具，后续不说明)

=======
>>>>>>> 13245c33ddf9e12b576448741e05a0f5394262f9
- 在html中有些时候，我们不能直接书写一些特殊符号

- 比如，多个连续的空格，比如字母两侧的大于和小于号
- 如果我们需要在网页中书写这些特殊的符号，则需要使用html中的实体（转义字符）
- 实体的名字
  - 空格`$nbsp;`
  - 大于号`$gt;`
  - 小于号`$lt;`
  - 版权符号`$copy;`
- 实体有很多，常用的记住，不常用的看文档



## 7. meta标签

<<<<<<< HEAD
[meta标签.html](../Codes/06_meta.html)

=======
>>>>>>> 13245c33ddf9e12b576448741e05a0f5394262f9
### 7.1. 样例

```html
    <meta charset="UTF-8">
    <!--
        meta主要用于设置网页中的一些元数据，元数据不是给用户看
            charset 指定网页的字符集
            name 指定的数据的名称
            content 指定的数据的内容

                keywords 表示网页的关键字，可以同时指定多个关键字，关键字用,(半角逗号)隔开
                description 用于指定网站的描述，内容会显示在搜索引擎的结果中
                title 表示网页的标题，会显示在标题栏，以及搜索结果的超链接上
                http-equiv="refresh" content="3;url=https://www.baidu.com"
                将页面重定向到另一个网站
    -->
    <meta name="keywords" content="HTML5,前端,CSS3">
    <meta name="description" content="这是一个非常不错的网站">
    <meta http-equiv="refresh" content="3;url=https://www.baidu.com">
```

### 7.2. 描述

- meta主要用于设置网页的元数据，元数据不是给用户看的
- 常见
  - charset 指定网页的字符集
  - name 指定的数据名称
    - 通常为 name=""
    - "keywords" 表示网页的关键字，可以同时指定多个关键字，关键字用,(半角逗号)隔开
    - "description" 用于指定网页的描述，内容会显示在搜索引擎的结果中
    - "title" 表示网页的标题，会显示在标题栏，以及搜索引擎的超链接上
  - content 指定的内容
    - 通常为 content=""
  - http-equiv
    - 完整结构`<meta http-equiv="refresh" content="3;url=">`
    - 可以实现网页多少秒后跳转到另一个网页
- 更多请看HTML文档



<<<<<<< HEAD
## 8.  语义化标签(一)

[语义化标签1.html](../Codes/07_语义化标签.html)

### 8.1. 概述

- 在网页中，HTML专门用来负责网页的结构
- 所以在使用html标签时
  - 应该关注标签的语义
  - 而不是它的样式

### 8.2. 标题标签

- h1~h6 一共有六级标题
- 从h1到h6重要性依次递减，h1最重要，h6最不重要
- h1在网页中的重要性仅次于title标签
- 一般情况下一个页面只会有一个h1
- 同时标题标签只会使用h1到h3，h4到h6很少用

### 8.3. 块元素

- 在页面中独占一行的元素为块元素
  - 标题标签都是块元素

### 8.4. 标题组

- hgroup标签用来为标题分组，可以将一组相关的标题同时放入到hgroup
- 但记住放在一起的标题一定要相关

```html
    <hgroup>
        <h1>回乡偶书二首</h1>
        <h2>其一</h2>
    </hgroup>
```

### 8.5. p标签

- p标签表示页面中的一个段落
- p也是一个块元素

### 8.6. em标签

- em标签表示语音语气强调
- em标签不会独占一行
  - 不会独占一行的元素称为行内元素
  - 也叫内联元素

### 8.7. strong标签

- strong标签强调重要内容
- 行内元素

### 8.8. blockquote标签

- blockquote表示一个长引用
- 块元素

### 8.9. q标签

- q表示一个短引用
- 行内元素

### 8.10. br标签

- br标签用来换行
- 自结束标签



## 9. 语义化标签(二)

- 块元素(block element)
  - 在网页中一般通过块元素来对页面进行布局

  - 有点像一个房子的布局，如三室两厅的布局
    行内元素(inline element)

  - 行内元素主要用来包裹文字
- 一般情况下会在块元素中放行内元素，而不会在行内元素中方块元素
  - 块元素中基本什么都能放
  - p元素中不能放块元素
- 浏览器在解析网页时，会自动对网页中不符合规范的内容进行修正，比如：
    - 标签写在根元素的外部
    - p元素中嵌套了块元素
    - 根元素中出现了除了head和body以外的子元素

## 10. 语义化标签(三)

[语义化标签3.html](../Codes/09_语义化标签3.html)

###  布局标签(结构化语义标签)

- header表示网页的头部
- main表示网页的主体(只有一个)
- footer表示网页的底部
- nav表示网页中的导航
- aside表示网页中的侧边栏(和主体相关的其他内容)
- article表示一个独立的文章
- section表示一个独立的区块(万能，如果上面表示不了用它，但不要滥用)
  - 但这些标签是html5新增的
  - 有的常用，有的不常用
  - 常不常用主要看在SEO(搜搜引擎)的作用
    

- div同样是万能区块，目前最主要的布局元素
- span行内元素，没有任何语义，一般用于在网页中选中文字
  - 这两个最常用



## 11. 列表
其中无序列表ul 用的最多，都可以通过ccs来修饰表现
### 11.1.无序列表ul

```html
    <ul>
        <li>结构</li>
        <li>表现</li>
        <li>行为</li>
    </ul>
```

### 11.2.有序列表ol
```html
    <ol>
        <li>结构</li>
        <li>表现</li>
        <li>行为</li>
    </ol>
```

### 11.3.定义列表dl
```html
    <dl>
        <dt>结构</dt>
        <dd>结构表示网页的结构</dd>
        <dd>规定哪里是标题</dd>
        <dd>等等</dd>
    </dl>
```



## 12. 超链接(一)

[超链接1.html](../Codes/11_超链接.html)

- 超链接可以让我们从一个页面跳转到其他页面
  或者是当前页面的其他位置

- 使用a标签来定义超链接
  - a标签是行内元素
  - 在a标签中可以嵌套除了a以外的任何元素

- 属性
  - href指定跳转的目标路径
  - 值可以是一个外部网站的地址
  - 也可以是内部页面的地址

```html
    <a href="https://www.baidu.com/">超链接1</a>
    <br>
    <a href="09_语义化标签3.html">超链接2</a> <!--这个在这个笔记里肯定不行 -->
```

## 13. 相对路径

- 当我们需要跳转一个服务器内部页面时，一般我们会用相对路径

- ./表示当前文件所在目录，可以省略不写
- ../表示当前文件所在目录的上级目录
- 比较简单，不详细说了



## 14. 超链接(二)

[超链接2.html](../Codes/13_超链接2.html)

- target属性，用来指定超链接打开的位置
- 可选项：
  - _self默认值，当前页面打开
  - _blank在一个新的页面中打开超链接
  - 后者国内常用，但经常会打开一堆页面忘关了
  - 前者国外常用，打开页面较少

## 15. 插入图片

[插入图片.html](../Codes/14_图片.html)

### 15.1. 概述

- 图片标签用于向当前页面中引入一个外部图片
- 使用img标签引入图片
- img是一个自结束标签
  - scr属性指定的是外部图片的路径，同超链接类似
  - alt图片的描述，一般不会显示，但如果无法加载，有些浏览器会显示描述
  - width宽度，单位是像素
  - height高度
    - 如果只改其中一个，等比例修改
    - 不建议同时修改
    - 不建议修改图片大小
    - 最好要多大的图，就制作多大的图
    - pc修改的少
    - 移动端大图变小挺常见

```html
    <img src="../images/dog.jpg" alt="狗子">
    <br>
    <img src="http://img2.imgtn.bdimg.com/it/u=1830066384,425676338&fm=26&gp=0.jpg" alt="猪猪侠">
```

- img这种元素属于替换元素
- 基于块和行内元素之间
- 最后在浏览器中显示的内容替代了代码写的内容

- alt搜索引擎也会根据这个来搜索图片
- 甚至屏幕阅读器帮助盲人看屏的时候会读出描述

### 15.2. 图片的格式

- jpeg(jpg)

  - 支持的颜色丰富，不支持透明，不支持动图(照片较多)
- gif
    - 支持颜色少，支持简单透明，支持动图
    - 颜色单一动图
- png
    - 支持颜色丰富，复杂透明，不支持动图
    - 颜色丰富nb专为网页而生
- 图片选择
- 效果一样选最小gif
- 效果不一样选最好
- 透明复杂png
- 要求小的jpg

- webp
  - 效果好(有上面的所有优点)
  - 占用小
  - 完美的图片
  - 最大最致命的缺点
    - 兼容性不好
    - 不要轻易使用

- base64
- 将图片编码
- 可以把图片转换为字符
- 通过字符引入图片
- 图片需要和网页一起加载才这样用
- 加载速度快
- 但它快了，别人就慢了



## 16. 内联框架

- iframe
- 内联框架，用于向当前页面中引入一个其他页面
- 属性：
- src路径
  - frameborder有无边界

    - 0无
  - 1有
  - width(貌似这个不会等比例修改）
  - height

- 现在用的很少了，以前用的多
- SEO不会爬取内联框架

```html
<iframe src="https://www.baidu.com" frameborder="0" width="1000" height="1000"></iframe>
```



## 17. 音频视频

[音频视频.html](../Codes/16_音频视频.html)

- 详细看上面网页源码中的注释
- 简述
  - audio标签
  - video标签
  - 可以简单写
  - 也可以为了兼容性稍微复杂写
  - 内联框架也可以插入视频网站的视频

```html
    <!-- <audio src="../source/起飞.mp3" controls autoplay></audio> 
        这种写法兼容性不好，可以用下面的方法兼容老的浏览器
    -->
    <audio controls>
        <source src="../source/起飞.mp3">
        <embed src="../source/起飞.mp3" type="audio/mp3" width="300" height="100">
        <!-- 兼容IE 8 -->
    </audio>

    <video controls>
        <source src="../source/老奶奶敢怒不敢言.mp4">
        <embed src="../source/老奶奶敢怒不敢言.mp4" type="video/mp4" width="500" height="300">
    </video>
    <!--
        但我们一般不把视频音频放到服务器里用相对路径
        因为这会占用很大的储存空间和网络带宽
        可以放到其他第三方远程托管降低成本
    -->
    <iframe src="//player.bilibili.com/player.html?aid=926289497&bvid=BV1FT4y1E7ZQ&cid=211202768&page=1" scrolling="no"
        border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="1300" height="800"> </iframe>
    <!--
        最后一种插入方式是内联框架的方法
    -->
```



## 18. 总结

- HTML称为超文本标记语言，是一种标识性的语言。
- 现在再读这句话，一定能明白其深刻含义了吧o(*￣▽￣*)ブ
- 在网页中，HTML专门用来负责网页的结构
  - 所以在使用html标签时
    - 应该关注标签的语义
    - 而不是它的样式
- HTML入门暂时到这里，今后边用边学
- 下载Zeal离线HTML文档，不懂或需要时直接查

