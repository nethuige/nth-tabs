# nth-tabs是什么？
基于bootstrap的多功能选项卡插件
# 其他依赖
> 滚动条 jquery.scrollbar
> 图标 font-awesome

# 背景
开发项目时需要一款多选项卡的插件，网上搜寻了一番，基本都是太丑陋、太古老、功能太少、BUG多、集成在框架中的混淆版。均无法满足本人需求，所以，只能自己动手造一个。根据自己的需求写了这款插件，插件功能定位主要是满足我个人需求，有更多需求的可以自己添加修改，如果有写的不好的地方或者存在BUG欢迎提issues，如果你觉得对你有用，请来个start。
# 使用说明
## CSS
```
<link href="https://cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet">
<link href="https://cdn.bootcss.com/font-awesome/4.4.0/css/font-awesome.min.css" rel="stylesheet">
<link href="https://cdn.bootcss.com/jquery.scrollbar/0.2.11/jquery.scrollbar.min.css" rel="stylesheet">
<link href="css/nth-tabs.css" rel="stylesheet">
<link href="css/nth-icons.css" rel="stylesheet">
```
## JS
```
<script src="https://cdn.bootcss.com/jquery/2.1.4/jquery.min.js"></script>
<script src="https://cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
<script src="https://cdn.bootcss.com/jquery.scrollbar/0.2.11/jquery.scrollbar.min.js"></script>
<script src="js/nth-tabs.js"></script>
```
## HTML
```
<div class="nth-tabs" id="custom-id"></div>
```
## 初始化
```
nthTabs = $("#custom-id").nthTabs();
```
## 新建选项卡
```
nthTabs.addTab({
    id: 'menu-manage',
    title: '菜单管理',
    content: '这是菜单管理页面~',
    //url: "http://www.nethuige.com",
    active: true, // 是否激活状态，默认是
    allowClose: true, //是否可关闭，默认是
    location: false, //是否自动定位，默认是
    fadeIn: true //是否开启淡入淡出效果，默认是
});
```
## 快速新建一个自定义内容选项卡
```
nthTabs.addTab({
    id: "web-site",
    title: 'URL选项卡',
    url: "http://www.nethuige.com"
});
```
## 快速新建一个自定义URL选项卡
```
nthTabs.addTab({
    id: "web-site",
    title: 'URL选项卡-' + id,
    url: "http://www.nethuige.com"
});
```
## 新建一个不可关闭的选项卡
```
nthTabs.addTab({
    id: 'home',
    title: '首页',
    content: '这里是首页',
    allowClose: false
});
```
## 新建一个非活动状态的选项卡
```
nthTabs.addTab({
    id: 'role-manage',
    title: '角色管理',
    active: false,
    content: '这是角色管理页面~'
});
```
## 新建多个选项卡-连贯操作
```
nthTabs.addTab({
    id: 'menu-manage',
    title: '菜单管理',
    active: false,
    content: '这是菜单管理页面~'
}).addTab({
    id: 'role-manage',
    title: '角色管理',
    active: false,
    content: '这是角色管理页面~'
});
```
## 新建多个选项卡-批量操作
```
nthTabs.addTabs([{
    id: 'user-manage',
    title: '用户管理',
    content: '这是用户管理页面~'
}, {
    id: 'auth-manage',
    title: '权限管理',
    content: '这是权限管理页面~'
}]);
```
## 删除一个选项卡
```
nthTabs.delTab('id');
```
## 删除当前选项卡
```
nthTabs.delTab();
```
## 删除其他选项卡
```
nthTabs.delOtherTab();
```
## 删除所有选项卡
```
nthTabs.delAllTab();
```
## 激活指定选项卡
```
nthTabs.setActTab(id);
```
## 切换到指定选项卡
```
nthTabs.toggleTab(id);
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
nthTabs.getTabList();
```
## 获取指定选项卡是否存在
```
nthTabs.isExistsTab();
```
## 选项卡切换事件处理器
```
nthTabs.tabToggleHandler(func);
```

## 打赏
<img src="https://s1.ax1x.com/2018/09/14/iEM5Y8.jpg" height="370" width="300">
