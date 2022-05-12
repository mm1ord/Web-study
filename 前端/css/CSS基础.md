## CSS基础

### css初识


css决定了页面的美观程度
css写在head标签里的title下,在style标签中
例子:
```
 p {
            color: blueviolet;
            font-size: 30px;
            background-color: green;
            width: 400px;
            height: 400px;
        } 
```
p:选择器 color:属性名 blueviolet:属性值
color-->字体颜色
font-size-->字体大小
background-color-->背景颜色
width-->背景宽度
height-->背景高度

### CSS引入方式
__内嵌式-->小案例__
CSS写在style文件中
__外联式-->项目中__
CSS单独写在单独的css文件中,通过link标签引入
__行内式-->配合js使用__
CSS写在标签的style属性中
### 选择器

#### 标签选择器
标签选择器就是以标签命名的选择器
选中所有的这个标签都生效css
eg 标签名{css属性名:属性值;}

#### 类选择器
class=" "
.类名{css属性名:属性值;}
所有标签上都有类属性
通过类名,找到页面中所有带这个类名的标签,设置样式
类名不能以数字或者中划线开头
一个标签可以同时拥有多个类名,类名之间以空格隔开
类名可以重复,一个类选择器可以同时选中多个标签

#### id选择器
id属性值{css属性名:属性值;}
所有标签上都有id属性
id属性值类似于身份证号码,在一个页面中是唯一的
一个标签上只有一个id值

#### 通配符选择器
*{css属性名:属性值;}
作用:找到页面中的所有标签,设置样式
开发中使用极少,只会在极特殊的情况下才会用到
在基础班小页面中可能会用于去除标签默认的margin和padding

### 字体和文本样式

#### 1.字体样式

字体大小:font-size-->数字+px

字体粗细 : font-weight
- 关键字:normal:正常 bold:加粗
- 纯数字:100-900的整百数 --> 400 加粗700
  
字体样式 : font-style
- 正常:normal
- 倾斜:italic

字体类型 : font-family
- 默认为微软雅黑
- 无衬线字体
- 衬线字体
- 等宽字体
```
    font-family: 微软雅黑,黑体,sans-serif
    /*如果电脑没有安装微软雅黑,就按照黑体显示*/
    /*如果电脑没有安装黑体,就按照任意一种无衬线字体显示*/
```

字体类型 : font 属性连写
```
/*font: style weight size 字体*/
  font: italic 700 66px 宋体;
```
注意点:如果需要同时设置单独和连写形式
- 要么把单独的样式写在连写的下面
- 要么把单独的样式写在连写的里面

__层叠性:如果共同体忒同一个标签设置了相同的属性,此时样式会层叠(覆盖),写在最下面的会生效__

#### 2.文本样式

文本缩进: tex-indent
取值:
- 数字+px 或 数字+em 
- (1em = 当前标签的font-size大小)

文本水平对齐方式: text-align
取值:
- left --> 左对齐
- right -->右对齐
- center -->居中对齐

text-align:center 能让哪些元素居中?
1. 文本
2. span标签\a标签
3. input标签\img标签
如果要让以上元素水平居中,text-align:center 需要给其 __父元素__ 设置

文本修饰属性 text-decoration
取值:
- underline --> 下划线(常用)
- line-through --> 删除线(不常用)
- overline --> 上划线(几乎不用)
- none --> 无修饰线(常用)
开发中会使用 text-decoration:none; 清除a标签默认的下划线(a超链接)

#### 3.行高
作用:控制一行的上下行间距

属性名:line-height

取值:
- 数字+px
- 倍数(当前标签font-size的倍数)

应用:
1. 让 __单行文本__ 垂直居中可以设置 __line-height:文字父元素高度__
2. 网页精准布局时,会设置line-height:1 可以取消上下间距

行高与font连写的注意点
- 如果同时设置了行高和font连写,注意覆盖问题
- font: style weight size/line-height family;

行高 = 上间距+文本高度+下间距

#### Chrome调试工具

#### 颜色常见取值
文字颜色 color

背景颜色 background-color

属性值:

|  颜色表示方式   | 表示含义 | 属性值 |
|  ----  | ----  | ---- |
| 关键词  |预定义的颜色名 |red green blue yellow
| rgb表示法  | 红绿蓝三原色每项取值范围 0-255 | rgb(0,0,0) rgb(255,255,255)
| rgba表示法  | 红绿蓝三原色+a表示透明度 前三项取值范围0-255 最后一项0-1 | rgba(255,255,255,0.3)
| 十六进制表示法  | #开头,将数字转换成十六进制表示 |  #000000 #ff0000










