# JsonFormater

### 基于jQuery的json格式化、高亮库

> 核心代码参考[天马行空工作室](http://tmxk.org/c/json/)，本人只做了模块化和一些代码优化。

## demo

[http://leo108.github.io/jsonFormater/](http://leo108.github.io/jsonFormater/)

## 使用方式

### 引入jQuery

`<script type="text/javascript" src="jquery-1.7.2.min.js"></script>`

注意：*jQuery版本要求>=1.7.2*

### 引入jsonFormater.js和jsonFormater.css

`<script type="text/javascript" src="jsonFormater.js"></script>`

`<link href="jsonFormater.css" type="text/css" rel="stylesheet"/>`

### 在html中新增一个空的元素作为显示的容器

例如`<div id='container'></div>`

### 调用JsonFormater

    $(document).ready(function(){
        var options = {
            dom : '#container' //对应容器的css选择器
        };
        var jf = new JsonFormater(options); //创建对象
        jf.doFormat('{"string":"leo108"}'); //格式化json
    });

## 效果图

![效果图](http://leo108.github.io/jsonFormater/images/demo.png)

## 详细使用方式

### 配置

支持的配置以及默认配置如下:

    {
        dom: '',          //用于放置的dom的选择器
        singleTab: "  ",  //单个tab
        tabSize: 2,       //缩进数量
        quoteKeys: true,  //key是否用双引号包含
        imgCollapsed: "images/Collapsed.gif", //收起的图片路径
        imgExpanded: "images/Expanded.gif",  //展开的图片路径
        isCollapsible: true //是否支持展开收起
    }

### 方法

`obj.doFormat(json)`格式化一个json字符串或者js对象

`obj.expandAll()`全部展开

`obj.collapseAll()`全部收起

`obj.collapseLevel(level)`展开到level层
