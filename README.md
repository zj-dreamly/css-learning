## HTML

### HTML5文档工具

http://h5o.github.io

###  HTML5新增内容

- section
- article
- nav
- aside

- header
- footer
- em
- strong
- i

### HTML元素分类

#### 按默认样式分

- 块级block
- 行内inline
- inline-block

### HTML元素嵌套关系

- 块级元素可以包含行内元素
- 块级元素不一定能包含行内元素
- 行内元素一般不能包含块级元素(a除外)

### HTML元素默认样式

#### HTML默认样式的意义

#### 默认样式带来的问题

#### CSS Reset

### HTML真题

#### doctype的意义

- 让浏览器以标准模式渲染
- 让浏览器知道元素的合法性

#### HTML XHTML HTML5的关系

- HTML属于SGML
- XHTML属于XML，是HTML进行XML严格化的结果
- HTML5不属于SGML或XML，比XHTML宽松

#### HTML5有什么变化

- 新的语义化元素
- 表单增强
- 新的API，（离线，音视频，图形，实时通信，本地存储，设备能力）
- 分类和嵌套变更

#### em和I的区别

- em是语义化的标签，表示强调
- i是纯样式的标签，表示斜体
- HTML5中i不推荐使用，一般用作图标

#### 语义化的意义

- 开发者容易理解
- 机器容易理解结构（搜索，读屏软件）

- 有助于SEO
- semantic microdata

#### 哪些元素可以自闭合

- input
- img
- br
- hr
- meta
- link

#### HTML和DOM的关系

- HTML是“死”的
- DOM由HTML解析而来，是“活”的
- JS可以维护DOM

#### property和attribute区别

- attribute是“死”的
- property是“活”的

#### form的作用有哪些

- 直接提交表单
- 使用submit/reset按钮
- 便于浏览器保存表单
- 第三方库可以整体提取值
- 第三方库可以进行表单验证

------



## CSS

### CSS选择器

- 用来匹配HTML元素，有不同的匹配规则
- 多个选择器可以叠加

#### 选择器的分类

- 元素选择器 a{}
- 伪元素选择器 ::before{}
- 类选择器 .link{}
- 属性选择器 [type=radio]{}
- 伪类选择器 :hover{}
- ID选择器 #id{}
- 组合选择器 [type=checkbox] + label{}
- 否定选择器 :not(.link){}
- 通用选择器 *{}

#### 选择器权重

| 选择器         | 权重 |
| -------------- | ---- |
| ID选择器       | 100  |
| 类、属性、伪类 | 10   |
| 元素、伪元素   | 1    |
| 其他选择器     | 0    |

> 此计算方式不会产生进位，10个类选择器的权重并不等同于一个ID选择器的权重

- !important 优先级最高
- 元素属性 优先级高（直接写style）
- 相同权重，后写的生效

### 非布局样式

- 字体，字重，颜色，大小，行高
- 背景，边框
- 滚动，换行
- 粗体，斜体，下划线
- 其他

#### 字体族

- serif 
- sans-serif 
- monospace
- cursive 
- fantasy

- 多字体fallback
- 网络字体，自定义字体
- iconfont

```css
 font-family: "PingFang SC", "Microsoft Yahei", monospace;
```

>字体名称书写要加引号，字体族不需要

#### 行高

- 行高的构成
- 行高相关的现象和方案
- 行高的调整