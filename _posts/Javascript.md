###`Javascript`


1. `string`去除空格
	- 去除所有空格
	
```
	str = str.replace(/\s+/g,"");    
```
   
   - 去除两头空格

```
str = str.replace(/^\s+|\s+$/g,"");
```
  
   - 去除左空格
```
str=str.replace( /^\s*/, '');
```

   - 去除右空格


```
str=str.replace(/(\s*$)/g, "");
```

2.  判断是否为数组
```
function isArray(o){
  return Object.prototype.toString.call(o)=='[object Array]';
}
```

3. 获取页面高度

- 使用`jquery`获取浏览器可视区域

```
 const visibleHeight = $(window).height();
 const visibleWidth = $(window).width();

```

-  `js`获取移动端屏幕高度和宽度等设备尺寸，兼容性比较好的方法：

```
document.documentElement.clientWidth;
document.documentElement.clientHeight;
```

