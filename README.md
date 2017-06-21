# nth-tabs是什么？
基于bootstrap的多功能选项卡插件
# 其他依赖
>滚动条 jquery.scrollbar
> 图标 font-awesome

# 为何会有此插件？
在开发项目的时候刚好需要一款多选项卡的插件，因为找了网上的各种插件基本上总结如下：太丑陋、太古老、功能太少、有bug、XX框架内集成、压缩版。均无法满足本人需求，无奈之下，时间紧张的情况下也只能加班加点自己撸一个。根据自己的需求写了这款插件，插件功能定位主要是满足我个人需求，如果你需要更多的功能需求可以自己更改源码扩展，如果有写的不好的地方或者存在bug欢迎submit issues，如果你觉得对你有用，不妨来个start。
# 使用说明
## CSS
```
<link href="https://cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet">
<link href="https://cdn.bootcss.com/font-awesome/4.4.0/css/font-awesome.min.css" rel="stylesheet">
<link href="https://cdn.bootcss.com/jquery.scrollbar/0.2.11/jquery.scrollbar.min.css" rel="stylesheet">
<link href="css/nth.tabs.min.css" rel="stylesheet">
```
## JS
```
<script src="https://cdn.bootcss.com/jquery/2.1.4/jquery.min.js"></script>
<script src="https://cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
<script src="https://cdn.bootcss.com/jquery.scrollbar/0.2.11/jquery.scrollbar.min.js"></script>
<script src="js/nth.tabs.min.js"></script>
```
## HTML
```
<div class="nth-tabs" id="custom-id"></div>
```
## 初始化
```
nthTabs = $("#custom-id").nthTabs();
```
## 添加一个选项卡
```
nthTabs.addTab({
        id:'a',
        title:'孙悟空',
        content:'看我七十二变',
});
```
## 添加一个不可关闭的选项卡
```
nthTabs.addTab({
        id:'a',
        title:'孙悟空',
        content:'看我七十二变',
        allowClose:false,
});
```
## 添加一个活动状态的选项卡
```
nthTabs.addTab({
        id:'a',
        title:'孙悟空',
        content:'看我七十二变',
        active:true,
});
```
## 添加多个选项卡
```
nthTabs.addTab({
        id:'a',
        title:'孙悟空',
        content:'看我七十二变',
}).addTab({
        id:'b',
        title:'孙悟空二号',
        content:'看我七十三变',
});
```
## 删除一个选项卡
```
nthTabs.delTab('id');
```
## 删除其他选项卡
```
nthTabs.delOtherTab();
```
## 删除所有选项卡
```
nthTabs.delAllTab();
```
## 切换到指定选项卡
```
nthTabs.setActTab(id);
```
## 定位到当前选项卡
```
nthTabs.locationTab();
```
## 左滑动
```
$('.roll-nav-left').click();
```
## 右滑动
```
$('.roll-nav-right').click();
```
## 获取左右滑动步值
```
nthTabs.getMarginStep();
```
## 获取当前选项卡ID
```
nthTabs.getActiveId();
```
## 获取所有选项卡宽度
```
nthTabs.getAllTabWidth();
```
## 获取所有选项卡
```
nthTabs.nthTabs.getTabList();
```