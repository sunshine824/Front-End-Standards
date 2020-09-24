## Css代码规范
1、每个样式属性后（必须）加 ";" 方便压缩工具"断句"；</br>
2、Class命名中（禁止）出现大写字母，（必须）采用” - “对class中的字母分隔，如：</br>
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
3、空格的使用，以下规则（必须）执行：</br>
> 选择器与 { 之前（必须）要有空格</br>
> 属性名的 : 后（必须）要有空格</br>
> 属性名的 : 前（禁止）加空格</br>
```
/* good */
.hotel-content {
    font-weight: bold;
 }
```
4、多选择器规则之间（必须）换行 </br>
> 当样式针对多个选择器时每个选择器占一行</br>
```
/* good */
 a.btn,
 input.btn,
 input[type="button"] {
     ......
 }
```
5、禁止为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;</br>
6、尽量使用简写形式的十六进制值，例如，用 #fff代替 #ffffff</br>
7、>、+、~ 选择器的两边各保留一个空格</br>
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
8、属性选择器中的值必须用双引号包围 </br>
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
9、当数值为 0 - 1 之间的小数时，省略整数部分的 0 </br>
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
10、RGB颜色值必须使用十六进制记号形式 #rrggbb。不允许使用 rgb() </br>
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
11、颜色值不允许使用命名色值。</br>
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
