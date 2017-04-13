## 水平居中

### 使用inline-block以及text-align实现。

```css
.container{
    text-align: center;
}
.ele{
    display: inline-block;
}
```

[Demo](../examples/CSS常见布局/demo1.html)

### 使用table实现

这种方法可以不定宽居中。

```css
.container{
        
}
.ele{
    display: table;
    margin: 0px auto;
}
```

[Demo](../examples/CSS常见布局/demo2.html)

### 使用margin: 0 auto实现

这种定位方法需要指定witdh。

```css
.container{

}
.ele{
    width: 100px;
    margin: 0 auto;
}
```
[Demo](../examples/CSS常见布局/demo3.html)

### 使用flex布局实现

```css
.container{
    display: flex;
    justify-content: center;
}
```

或者

```css
.container{
    display: flex;
}
.ele{
    margin: 0px auto;
}
```

[Demo](../examples/CSS常见布局/demo4.html)

### 绝对定位

```css
.container{
    position: relative;
}
.ele{
    position: absolute;
    left: 50%;
    margin-left: -50px;
    width: 100px;
    height: 100px;
    background-color: red;
}
```

或者将元素宽度的一般改成transform: translate(-50%)，这样不定宽的时候也可以实现居中，但是兼容性不是足够好。

```css
.container{
    position: relative;
}
.ele{
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    width: 100px;
    height: 100px;
    background-color: red;
}
```