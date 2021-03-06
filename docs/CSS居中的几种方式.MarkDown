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

[Demo](../examples/CSS居中的几种方式/demo1.html)

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

[Demo](../examples/CSS居中的几种方式/demo2.html)

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
[Demo](../examples/CSS居中的几种方式/demo3.html)

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

[Demo](../examples/CSS居中的几种方式/demo4.html)

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

[Demo](../examples/CSS居中的几种方式/demo5.html)

## 垂直居中

### 使用vertical-align

```css
.container{
    display: table-cell;
    vertical-align: middle;
}
```

注意要设置height或者line-height。

[Demo](../examples/CSS居中的几种方式/demo6.html)

或者

```css
.container{
    display:inline-block;
    vertical-align: middle;
}
```

[Demo](../examples/CSS居中的几种方式/demo7.html)

### 绝对定位

```css
.container{
    height: 500px;
    position:relative;
}
.ele{
    position: absolute;
    top: 50%;
    height: 50px;
    margin-top: -25px;
}
```

当然height的一半也可以用

```css
transform:translate(0,-50%);
```

来替代。

[Demo](../examples/CSS居中的几种方式/demo8.html)

### 使用flex布局实现

```css
.container{
    display: flex;
    align-items: center;
}
```

[Demo](../examples/CSS居中的几种方式/demo9.html)

## 水平垂直居中

### 使用flex布局

利用flex布局的justify-content以及align-items修改弹性盒子纵向以及横向的对其位置，使子元素在纵向以及横向位置都以正中位置对其。

```css
.container{
    display: flex;
    justify-content: center;
    align-items: center;
}
```

[Demo](../examples/CSS居中的几种方式/demo10.html)

### 使用绝对定位

使用绝对定位设置top以及left为50%，然后将宽度以及高度的一半“拉”回来。

```css
.container{
    position: relative;
}
.ele{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}
```

[Demo](../examples/CSS居中的几种方式/demo11.html)

如果宽度高度指定的时候也可以通过设置负的margin来实现。

```css
.container{
    position: relative;
}
.ele{
    position: absolute;
    top: 50%;
    left: 50%;
    height: 100px;
    width: 100px;
    margin-left: -50px;
    margin-top: -50px;
}
```

## 利用vertical-align,text-align,inline-block实现

```css
.container{
    display:table-cell;
    vertical-align: middle;
    text-align: center;
}
.ele{
    display: inline-block;
}
```

[Demo](../examples/CSS居中的几种方式/demo12.html)