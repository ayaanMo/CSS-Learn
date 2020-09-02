Flex布局(flexible Box):
    用来为盒状迷行提供最大的灵活性，任何一个容器都可以指定flex布局
    * 当我们为父盒子设置flex布局以后，子元素的float、clear和vertical-align属性将失效
    * 采用了flex布局的元素，称之为Flex容器，简称容器，它所有子元素自动成为容器成员，称之为Flex项目(flex item)
    * 就是通过给父盒子添加flex属性，来控制子盒子的位置和排列方式
flex常见属性:
  父级属性:
    1.flex-direction:设置主轴的方向
        flex-direction 属性决定主轴的方向(即子元素的排列方向)，默认是row 从左至右
        row（从左至右）、row-reverse（从左至右）、column（从上至下）、column-reverse（从下至上）
      注意：主轴和侧轴是回变化的，就看flex-direction设置谁为主轴，剩下的就是侧轴，子元素都是跟着主轴来排列的
    2.justify-content:设置主轴上的子元素排列方式
        justify-content 默认值是从头部开始，如果主轴是x轴，则从左至右
        flex-start（默认值是从头部开始，如果主轴是x轴，则从左至右）、flex-end（从尾部开始排列）、center（在主轴居中对齐，如果主轴是x轴则水平居中）、space-around（平分剩余空间）、space-between（先两边贴边再平分剩余空间）
    3.flex-wrap:设置子元素是否自动换行
        flex-wrap:默认是不换行，项目都排在一条线（又称"轴线"）上
    4.align-content:设置侧轴上的子元素排列方式(多行)
        设置子项在侧轴上的排列方式并且只能用于子项出现换行的情况（多行），在单行下是没有效果的
        flex-start（默认值在侧轴的头部开始排列）、flex-end（在侧轴的尾部开始排列）、center（在侧轴的中间显示）、space-around（子项在侧轴平分空间）、space-between（子项在侧轴先分布在两头，在平分剩余空间）、stretch（设置子项元素高度平分父元素高度）
    5.align-items:设置侧轴上的子元素排列方式(单行)
        该属性是控制子项在侧轴（默认是y轴）上的排列方式，在子项为单项的时候使用
        flex-start（从上到下）、flex-end（从下到上）、center（挤在一起居中）、stretch（拉伸，默认值）
    6.flex-flow:复合属性，相当于同时设置了flex-direction和flex-wrap
        flex-direction:column; flex-wrap:wrap => flex-flow:column wrap;
  子项属性:
    1.flex子项目占的分数
        语法 子项目{flex:<number>}
    2.align-self控制子项自己在侧轴的排列方式
        属性是允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值是auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch
    3.order属性定义子项的排列顺序（前后顺序）
        数值越小，排列约靠前，默认是0