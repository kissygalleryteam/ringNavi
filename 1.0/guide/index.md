## ringNavi

* 版本：1.0
* 教程：[http://gallery.kissyui.com/ringNavi/1.0/guide/index.html](http://gallery.kissyui.com/ringNavi/1.0/guide/index.html)
* demo：[http://gallery.kissyui.com/ringNavi/1.0/demo/index.html](http://gallery.kissyui.com/ringNavi/1.0/demo/index.html)

## 组件概览
![RingNavi](http://www.seejs.com/wp-content/uploads/2013/08/ringnavi.png)

## 参数说明

* param trigger{String|HtmlNode} 导航显示/隐藏控制器
* param items{String} 导航元素class，用于选择导航元素
* param displayArea{Object} 设置导航展开区域，由于是环状展开，因此单位为【度】
  
  from {Number} 起始度数
  
  to {Number} 结束度数
* param expandWay{String} 设置导航展开方式，目前支持默认和 `stepByStep` 两种方式
* param expanded{Boolean} 设置导航默认是否展开
* param easing{String} 导航展开过程动画名称，使用KISSY提供的 `easeIn`、`bounceOut` 等，默认 `easeIn`
* param toggle{Boolean} 是否开启，展开状态点击trigger关闭导航，关闭状态点击trigger展开导航功能
* param radius{Number} 设置环状导航的展开半径，默认为200
* param speed{Float} 导航展开时间，用于控制速度，单位s，默认0.2
* param delay{Number} 设置 `expandWay` 为 `stepByStep` 时有效，用于控制单个导航出现的时间间隔

## 使用说明
本地使用，请添加以下代码：

```
var S = KISSY;
S.Config.debug = true;
if (S.Config.debug) {
    var srcPath = "../../../";
    S.config({
        packages:[
            {
                name:"gallery",
                path:srcPath,
                charset:"utf-8",
                ignorePackageNameInUri:true
            }
        ]
    });
}
```

组件初始化方法：

```
S.use('gallery/ringNavi/1.0/index', function (S, RingNavi) {
	var ringNavi = new RingNavi({
		trigger: ".J_RingNavi",
		displayArea: {
			from: 180,
			to: 270
		},
		expanded: true,
		expandWay: "stepByStep",
		delay: 200,
		toggle: true,
		radius: 150
	});
});
```
详细演示请自行查看demo。

## changelog

### V1.0


