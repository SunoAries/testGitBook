# 前公司移动开发平台文档
Ares是前公司移动开发框架，在此基础上，只需调用相关api，即可构建面向不同业务的移动应用

## 技术栈

前端技术栈为React、React-Redux、React--Native-Router-Flux、Native-Base

## 功能

* 安全登录登出
* 请求加密
* 版本检测
* 应用安装与卸载
* 聊天功能
* 下载模块
* 用户管理
* 数据持久化

##  项目搭建

1.  Java环境+安卓环境
2.  npm install
3.  react-native run-android/run-ios


##  使用

* [UI组件](chapter1.md)
     引入 `import { Button } from "native-base";` 在页面中即可使用`<Button>button</Button>`
     
* [工具函数](di-er-zhang.md)
      引入 `import {versionCheck} from "../../util/AppUtil";` 
      
      调用工具函数`versionCheck(this.props.setting.version)`
      
* [路由](di-san-zhang.md)
      引入 `import {Router, Scene, ActionConst} from 'react-native-router-flux'`
          

##  性能对比

### 性能 
*   内存：Native最少；因为React Native含有框架，所以相对较高，但是后期平稳后会优于Native。
*   CPU：React Native居中。
*   动画：React Native动画需求基本满足。
*   Big ListView
*   真机体验：Native >= React Native > H5/Hybrid

### 更新与维护
*   更新能力: H5/Hybird > React Native > Native
*   维护成本: H5/Hybird <= React Native < Native


## 项目目录

```
├─api
├─components    #自定义组件
│  ├─app
│  ├─checkbox
│  ├─expand
│  ├─friend
│  ├─group
│  ├─image
│  ├─infoItem
│  ├─input
│  ├─logo
│  ├─menu
│  ├─message
│  ├─modalBox
│  ├─org
│  ├─portalModal
│  ├─tab
│  ├─titleBar
│  └─toast
│      └─image
├─frame         #redux全局状态管理
│  ├─actions
│  ├─reducers
│  ├─state
│  ├─store
│  └─style
├─native        #原生模块
│  ├─aresNative
│  └─ui
├─resources
│  └─img
├─util         #rn工具函数
└─views        #rn业务代码
    ├─appDetail
    ├─appStore
    ├─assets
    │  └─contacts
    ├─contacts
    ├─contactsDetail
    ├─createGroupOne
    ├─createGroupTwo
    ├─groupDetail
    ├─login       #登录页面
    ├─main
    ├─note
    ├─platform    #native-base UI组件使用示例
    │  ├─boot
    │  ├─screens
    │  │  ├─actionsheet
    │  │  ├─anatomy
    │  │  ├─badge
    │  │  ├─button
    │  │  ├─card
    │  │  ├─checkbox
     ..................
     ..................
    ├─push
    ├─splash        
    ├─user
    ├─userSetting   #用户管理页面
    └─webview       #调用webview页面
```

