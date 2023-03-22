# 设置授权免翻应用列表
## 说明
MIUI12-安卓11，设置申请个“显示在其他应用上层”权限居然让我去翻整个应用列表！还要在一堆应用里里面去翻你要开的那个应用，这种时候还没有个搜索！每次申请这个权限都不免血压升高一次。话说MIUI开发部，你是故意这么做的，还是不小心留的bug？  

通过Xposed，hook了那个列表activity的onCreate()方法，在方法执行结束后，直接startActivitiy到目标软件的“允许显示在其他应用上层”的开关，极大简化了授予权限的步骤。  
  
听说MIUI13申请安装未知应用也要翻列表，不过我没有设备，没法测试，下个版可以开发。
## 使用
安装本模块，在Xposed（LSP）中启用，并勾选设置。
