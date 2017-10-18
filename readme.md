### 表单
1. 提交表单时，需要阻止默认事件
   - 当先校验客户提交的数据,格式是否正确
   - 当需要对这些数据进行一个处理再提交
   就需要先阻止下默认提交表单的行为
```
submit = (e) => {
    e.preventDefault();
    ...
}
```

2. 使用`form`标签时，需要对设置按钮的类型`type = "button"`，否则点击按钮页面会来回跳。

```
<form>
	<input type="text" name="username" placeholder="请输入您的账号" />
	<input type="password" name="password" placeholder="请输入您的密码" />       
	<button type="button" class="submitBtn">登 录</button>
</form>
```

3.删除 浏览器自带`input`输入框会有黄色背景，以及删除处于焦点的输入框`border`
```
.input-value {
      border: 0;
      height: 60px;
      width: 150px;
      -webkit-box-shadow: 0 0 0 1000px white inset;

      &:focus {
        outline: none !important;
        border: none;
        box-shadow: white;
      }
    }
```

5. 垂直居中
 - 块状元素，利用盒子模型的`padding`属性，套一个父`div`，然 后通过计算父盒子高度和子盒子高度差，分配`padding`上下值

```
  // 根据可视区域高度，自适应居中
  const visibleHeight = $(window).height();
  $('.parent').height(visibleHeight);
  
  const $child = $('.child');
  let paddingVal = Math.floor((visibleHeight - $child.height()) / 2 / 2);
  $mainBox.css({ 'padding-top': `${paddingVal}px` });
  $mainBox.css({ 'padding-bottom': `${paddingVal}px` });
```


- 行内元素，设置`line-height`值与高度值一致，实现垂直居中，仅适用于**单行文本**
```
.text {
    display: inline-block;
	height: 20;
    line-height: 20px
}
```

6. 水平居中
 - 行内元素 ，`text-align: center`
 - 固定宽度的块状元素
```
 width: 200px;
 margin: 0 auto;
```
