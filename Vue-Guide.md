## Vue代码规范

### 命名 

#### 1、components下的命名

1-1、文件夹首字母必须大写并驼峰命名，如GlobalHeader、Exception  

1-2、文件夹下所有文件首字母大写并驼峰命名  

#### 2、views下的命名

2-1、文件夹以模块命名

2-2、文件夹首字母必须小写并驼峰命名，如globalHeader、exception   

2-3、文件夹下所有文件首字母小写并驼峰命名  

#### 3、methods下的命名

3-1、事件方法以 on 开头（onTypeChange、onUsernameInput）  

3-2、尽量使用常用单词开头（set、get、open、close、jump）  

3-3、驼峰命名（good: getListData）（bad: get_list_data、getlistData）  

3-4、私有方法以“_”开头 (_getTableList)

### 结构化规范

```
.
├── src
│   ├── App.vue
│   ├── api                         # 接口管理模块
│   ├── assets                      # 静态资源模块
│   ├── components                  # 公共组件模块
│   ├── ├── GlobalHeader            # components下文件夹命名
│   ├── ├── ├── GlobalHeader.vue    # components下文件命名
│   ├── layouts                     # 公共自定义布局
│   ├── main.js                     # 入口文件
│   ├── public                      # 公共资源模块
│   ├── router                      # 路由
│   ├── store                       # vuex状态库
│   ├── utils                       # 公共方法模块
│   ├── views                       # 视图模块
│   ├── ├── control                 # views下文件夹命名
│   ├── ├── ├── model               # control模块下的model框
│   ├── ├── ├── piece               # control模块下的拆分组件
│   ├── ├── ├── index.vue       # control模块下入口文件
```
###  注释

1、单行注释 '//'

2、多行注释  '/** **/'

3、方法注释

```
/**
* 方法名称
* @desc 方法描述
* @author 作者
* @date 2017年12月05日17:22:43
* @param {Object} [title]    - 参数说明
* @param {String} [columns] - 参数说明
**/
```

### 其他

1、尽力避免使用watch监听  

2、子组件Prop接收定义，小驼峰命名
```
//bad
props: ['title']

//good
props: {
    title: {
        type: String,
        required: true,
        default:()=>{}
    }
}
```
3、components 导入，引用顺序规范

```
<template>
  <global-header></global-header>
</template>
<script>
import GlobalHeader from "./GlobalHeader"

...
components:{
  GlobalHeader,
  GlobalTable,
  "update-table-data": UpdateTableData
}
...
</script>
```
4、VUEX采用命名空间的写法，原因是避免命名重复













