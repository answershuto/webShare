## 左列固定宽度，右列自适应

### 使用flex布局实现

```css
.container{
    display: flex;
}
.l{
    width: 100px;
}
.r{
    flex: 1;
}
```

[Demo](../examples/CSS常见布局/demo1.html)

### 使用float以及margin实现

```css
.l{
    width: 100px;
    float: left;
}
.r{
    margin-left: 100px;
}
```

[Demo](../examples/CSS常见布局/demo2.html)

### 使用float以及overflow实现

```css
.l{
    width: 100px;
    float: left;
}
.r{
    overflow: hidden;
}
```

通过设置overflow创建了一个(BFC)[http://www.cnblogs.com/cjlalala/p/5556855.html]，可以形成一个独立的容器，浮动盒区域不叠加在BFC上，容器内子元素不会影响到外面的元素，反之亦然。设置overflow:auto;等都能达到同样效果，只需要形成一个BFC。

[Demo](../examples/CSS常见布局/demo3.html)

### 使用table实现

```css
.container{
    display: table;
    table-layout: fixed;
    width: 100%;
}
.l{
    width: 100px;
}
.r, .l{
    display: table-cell;
}
```

[Demo](../examples/CSS常见布局/demo4.html)

## 右列固定宽度，左列自适应

### 使用flex布局实现

```css
.container{
    display: flex;
}
.l{
    flex: 1;
}
.r{
    width: 100px;
}
```

[Demo](../examples/CSS常见布局/demo5.html)

### 使用float以及margin实现

```css
.l{
    float: left;
    margin-right: -100px;
    width: 100%;
}
.r{
    float: right;
    width: 100px;
}
```

[Demo](../examples/CSS常见布局/demo6.html)

### 使用table实现

```css
.container{
    display: table;
    table-layout: fixed;
    width: 100%;
}
.r{
    width: 100px;
}
.l, .r{
    display: table-cell;
}
```