# 第三章 流、元素与基本尺寸

html标签分为两类：块级元素和内联元素

## 3.1块级元素

块级元素的基本特征：水平流上只能单独显示一个元素，多个块级元素则换行显示。
由于块级元素具有换行特性，因此理论上都可以配合clear属性来清除浮动带来的影响。

```html
<div>
    <img src="http://demo.cssworld.cn/images/common/l/1.jpg" />
</div>
```

```css
.box {
    padding: 10px;
    background-color: #cd0000;
}
.box > img {
    float: left;
}
.clear:after {
    content: "";
    display: 'block' || 'table' || 'list-item';
    clear: both;
}
```

实际开发中只会使用block或者table并不会使用list-item，原因如下:
- 字符比较多
- 会出现不需要的项目符号，还需要加list-style: none
- ie不支持伪元素的display为list-item。

### 3.1.1 为什么list-item元素会出现项目符号

- 块级盒子负责结构，内联盒子负责内容。
    所有块级元素只有一个块级盒子，但无法显示list-item中的项目符号
- 所有块级元素都有一个主块级盒子，list-item除此之外还有一个附加盒子(marker box)
    但无法解释display: inline-block 既能在一行中显示又可以设置宽高。
- 每个元素都有两个盒子，外在和盒子和容器盒子。外在盒子负责元素是可以一行显示还是只能换行显示。容器盒子负责宽高、内容呈现等。