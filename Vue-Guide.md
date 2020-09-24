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
  ```bash
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
  、、、
