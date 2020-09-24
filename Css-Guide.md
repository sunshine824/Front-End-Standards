## Css代码规范
1、每个样式属性后（必须）加 ";" 方便压缩工具"断句"；  

2、Class命名中（禁止）出现大写字母，（必须）采用” - “对class中的字母分隔，如：  

```
/* good */
.hotel-title {
    font-weight: bold;
}

/* bad */
.hotelTitle {
    font-weight: bold;
}
```
3、空格的使用，以下规则（必须）执行：  

> 选择器与 { 之前（必须）要有空格  

> 属性名的 : 后（必须）要有空格  

> 属性名的 : 前（禁止）加空格  

```
/* good */
.hotel-content {
    font-weight: bold;
 }
```
4、多选择器规则之间（必须）换行   

> 当样式针对多个选择器时每个选择器占一行  

```
/* good */
 a.btn,
 input.btn,
 input[type="button"] {
     ......
 }
```
5、禁止为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;  

6、尽量使用简写形式的十六进制值，例如，用 #fff代替 #ffffff  

7、>、+、~ 选择器的两边各保留一个空格  

```
/* good */
main > nav {
  padding: 10px;
}
label + input {
  margin-left: 5px;
}
input:checked ~ button {
  background-color: #69C;
}

/* bad */
main>nav {
  padding: 10px;
}
label+input {
  margin-left: 5px;
}
input:checked~button {
  background-color: #69C;
}
```
8、属性选择器中的值必须用双引号包围   

```
/* good */
article[character="juliet"] {
  voice-family: "Vivien Leigh", victoria, female;
}

/* bad */
article[character='juliet'] {
  voice-family: "Vivien Leigh", victoria, female;
}
```
9、当数值为 0 - 1 之间的小数时，省略整数部分的 0    

```
/* good */
panel {
  opacity: .8;
}

/* bad */
panel {
  opacity: 0.8;
}
```
10、RGB颜色值必须使用十六进制记号形式 #rrggbb。不允许使用 rgb()   

```
/* good */
.success {
  box-shadow: 0 0 2px rgba(0, 128, 0, .3);
  border-color: #008000;
}

/* bad */
.success {
  box-shadow: 0 0 2px rgba(0,128,0,.3);
  border-color: rgb(0, 128, 0);
}
```
11、颜色值不允许使用命名色值。    

```
/* good */
.success {
  color: #90ee90;
}

/* bad */
.success {
  color: lightgreen;
}
```
12、关于css背景图片(关键字：合并，缩写，去引号), 引号不是必须的，而且在某些浏览器上加引号反而出错   
```
// good(合并、去除引号)
.canbox {
    background: #f60 url(/img/xxx.png); 
}

// bad
.canbox{
    background-color: #ff6600;
    background-image: url("/img/xxx.png");
}
```
13、所有CSS的命名应语义化，如：回复框，.replyBox{…}，禁止用拼音缩写命名，如.hfk{…}  

14、上下相邻的两模块尽量避免混用margin-bottom，margin-top，否则会产生重叠现象  

