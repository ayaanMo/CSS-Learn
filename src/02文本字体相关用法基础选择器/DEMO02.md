1. 基础选择器:
   标签选择器(HTML 标签名作为选择器)
   类选择器(样式点定义, 结构类(class)调用, 一个或多个, 开发最常用)，多类名样式（可以将公共的样式提出一个类）
   id 选择器(HTML 元素以 id 属性来设置 id 选择器, 样式#定义, 结构 id 调用, 只能调用一次, 别人切勿使用)
   通配符选择器:* 会将页面所有标签的颜色都将改变，通配符选择器不需要调用，自动给所有的元素使用样式
2. 字体相关属性:
   font-size(字体大小)、font-weight(字体粗细)、font-family(字体格式)、font-style(字体斜体)、font(必须要用 font-size 和 font-family)
3. 文本相关属性:
   color: 文本颜色
   text-align: 水平居中 默认值 left right center
   text-decoration 属性规定添加文本修饰，可以添加下划线、删除线、上划线，默认是 none(取消装饰线)、underline(下划线)、overline(上划线)、line-through(删除线)
   text-indent 属性用来指定文本的第一行的缩进，通常是将段落的首行缩进 传的是 em 相当于当前元素(font-size 默认值是 16px)的 1 个文字的大小
   line-height 行间距 可以控制行行与行之间的间距 一个完整的行间距 是由三个部分组成(上间距、文本高度、下间距) 一般设置的是上间距和下间距高度
4. 内部样式表和外部样式表: 1.行内样式表:优点:书写方便，权重高 缺点:结构样式混写 较少 2.内部样式表:优点:部分结构和样式相分离 缺点:没有彻底分离 较多 3.外部样式表:优点:完全实现结构和样式相分离 缺点:需要引入 最多 <link rel="stylesheet" href="demo04.css">
