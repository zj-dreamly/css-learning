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

#### 背景

- 背景颜色
- 渐变色背景
- 多背景叠加
- 背景图片和属性（雪碧图）
- base64和性能优化
- 多分辨率适配

#### 边框

- 边框的属性：线性 大小 颜色
- 边框背景图，边框衔接（三角形）

#### 滚动

- visible 滚动条隐藏，超出显示
- hidden 滚动条隐藏，超出隐藏
- scroll 滚动条显示
- auto 滚动条自动隐藏

#### 文字折行

- overflow-wrap(word-wrap) 通用换行控制
  - 是否保留单词
- word-break 针对多字节文字
  - 中文句子也是单词
- white-space 空白处是否断行

#### 装饰性属性以及其他

- 自重（粗体） font-weight
- 斜体 font-style: itatic
- 下划线 text-decoration
- 指针 cursor

#### CSS Hack

- Hack即不合法但生效的写法
- 主要用于区别不同浏览器
- 缺点：难理解，难维护，易失效
- 替代方案：特性检测
- 替代方案：针对性加class

### CSS面试真题

#### css样式（选择器）的优先级

- 计算权重确定
- !important
- 内联样式
- 后写的优先级高

#### 雪碧图的作用

- 减少HTTP请求，提高加载性能
- 在某些情况下减少图片的大小

#### 自定义字体的使用场景

- 宣传/品牌页/banner等固定文案
- 字体图标

#### base64的使用

- 减少HTTP请求
- 适用于小图片
- base64的体积大概约为原来的三分之四

#### 伪类和伪元素的区别

- 伪类表示状态
- 伪元素是真的有元素
- 前者单冒号，后者双冒号

#### 如何美化checkbox

- label[for] 和id
- 隐藏原生input
- :checked + label

### CSS布局

- css知识体系的重中之重
- 早期以table为主（简单）
- 后来以技巧性布局为主（难）
- 现在有flexbox/grid（偏简单）
- 响应式布局是必备知识

#### 常用布局方式

- table表格布局
- float + margin
- inline-block布局
- flexbox布局

#### display

- block
- inline
- inline-block

#### position

- static
- relative
- absolute
- fixed

#### flexbox

- 弹性盒子盒子本身就是并列的
- 指定宽度即可

#### float

- 元素“浮动”

- 脱离文档流

- 但不脱离文本流

- 对自身的影响

  - 会形成“块”（BFC）

  - 位置尽量靠上

  - 位置尽量靠左/右

- 对兄弟的影响

  - 上面贴非float元素

  - 旁边贴float元素

  - 不影响其他块级元素的位置

  - 影响其他块级元素内部文本

- 对父级元素的影响

  - 从布局上消失

  - 高度塌陷

#### inline-block

- 像文本一样排列block元素
- 没有清除浮动等问题
- 需要处理间隙

#### 响应式设计与布局

- 在不同设备上正常使用
- 一般处理屏幕大小问题
- 主要方法：
  - 隐藏
  - 折行
  - 自适应空间
  - rem
  - viewport
  - media query

### CSS面试真题

#### 实现两栏（三栏）布局的方法

- 表格布局
- float + margin布局
- inline-block布局
- flexbox布局

#### position:absolute/fixed区别

- 前者相对最近的absolute或者relative
- 后者相对屏幕

#### display:inline-block的间隙

- 原因：字符间距
- 消灭字符或者间距

#### 如何清除浮动

- 让盒子负责自己的布局
  - overflow:hidden(auto)
  - ::after{clear:both}

#### 如何适配移动端页面

- viewport
- rem/viewport/media query
- 设计上：隐藏，折行，自适应

### CSS效果

