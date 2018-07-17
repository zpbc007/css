# 第二章 需提前了解的术语和概念

## 专业术语

```css
.vovabulary {
    height: 99px;
    color: transparent;
}
```

1. 属性
2. 值
    - 整数值 如z-index: 1
    - 数值 如line-height: 1.5
    - 百分比值 如padding: 50%
    - 长度值 如 99px
    - 颜色值 如 #999
    - 位置值 如 float: left
3. 关键字
    solid、inherit
4. 变量
5. 长度单位
    - 相对长度单位
        (1)相对字体长度单位 em,ex,rem,ch
        (2)绝对长度单位 px
6. 功能符
    值以函数的形式指定 如rgba(0, 0, 0, 0.5)
7. 选择器
    - 类选择器
    - id选择器
    - 属性选择器 [title="css-word"]
    - 伪类选择器 :first-child
    - 伪元素选择器 ::first-line
8. 关系选择器
    - 后代选择器 空格连接
    - 相邻后代选择器，只要儿子元素。 > 连接
    - 兄弟选择器 ~ 连接
    - 相邻兄弟选择器 + 连接

## 未定义行为

标准中并未明确指出，各浏览器实现方式不同。
    