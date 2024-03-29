定位：
  1. 能够说出为什么要定位；
     可以让盒子自由的再某个盒子内移动位置或者固定屏幕中某个位置，平切可以压住其他盒子；
     将盒子定在某一个位置，所以定位也是在摆盒子，按照定位的方式移动盒子

   定位 = 定位模式 + 边偏移
   定位模式用于指定一个元素在文档中的定位方式。边偏移则决定了该元素的最终位置
  2. 能够说出四种分类; 
    position定位模式：
      1.static：静态定位
      2.relative：相对定位
      3.absolute：绝对定位
      4.fixed：固定定位
    边偏移就是定位盒子移动的最终位置，有top、bottom、left和right4个属性
    top：顶端偏移量 定义元素相对于其父元素上边线的距离
    bottom：底部偏移，定义元素相对于父元素下边线的距离
    left：左侧偏移 定义元素相对于其父元素左边线的距离
    right：右侧偏移，定义元素相对于其父元素右边线的距离

  3. 能够说出4种定位的各自特点；
   static（了解）：静态定位 默认定位方式，无定位的意思 语法 选择器{position:static} 静态定位按照标准流特性摆放位置，它没有边偏移 静态定位在布局时很少用
   relative：

       相对定位 是元素在移动位置时候，是相对于它原来的位置来说的(是按照自已原本的位置来移动的) 自恋型定位;虽然它移动了 但是它原本的位置是不会被占有的,它原来标准流的位置还是保留的
       因此相对定位并没有脱标。它最典型的应用就是给绝对定位当爹的

   absolute：

      绝对定位 是元素在移动位置的时候，是相对于它的组件元素来说的；绝对定位的特点如下：
      选择器:{position:absolute;}
      1.如果没有祖先元素或者祖先元素没有定位，则以浏览器为准定位（Document）
      2.如果祖先元素有定位（相对、绝对、固定定位），则以最近一级的有定位组件元素为参考点移动位置
      3.绝对定位不再占有原先位置的(脱标)

  fixed:

      固定定位：是元素固定于浏览器可视区的位置，主要使用场景：可以再浏览器页面滚动时元素的位置不会改变。
      选择器{position:fixed}
      固定定位特点：
        1.以浏览器的可视窗口为参照点移动元素
          跟父元素没有任何关系
          不随滚动条滚动
        2.固定定位不占有原先的位置
          固定定位也是脱标的，其实固定定位也可以看做是一种特殊的绝对定位

  sticky:

      粘性定位sticky：粘性定位可以被认为是相对定位和固定定位的混合。Sticky粘性的
      选择器{position:sticky;top:10px}
       粘性定位的特点：
         1.以浏览器的可视窗口为参照点移动元素（固定定位特点）
         2.粘性定位占有原先的位置（相对定位的特点）
         3.必须添加top、left、right、bottom其中一个才有效
       总结：跟页面滚动搭配使用，兼容性差，ie不支持

  4. 能够说出为什么常用子绝父相布局；
    子绝父相：子级使用绝对定位，父级则需要使用相对定位   
      1.子级绝对定位，不会占有位置，可以放到父盒子里面的任何一个地方，不会影响其他的兄弟盒子。
      2.父盒子需要加定位限制盒子在父盒子内显示。
      3.父盒子布局时，需要占有位置，因此父亲只能相对定位。
     总结：因为父级需要占有位置，因此是相对定位，子盒子不需要占有位置，则是绝对定位

定位总结; 

    |     定位模式     |    是否脱标    |      移动位置      |   是否常用   |
    | :--------------: | :------------: | :----------------: | :----------: |
    |  static静态定位  |       否       |   不能使用边偏移   |     很少     |
    | relative相对定位 |  否(占有位置)  | 相对于自身位置移动 |     常用     |
    | absolute绝对定位 | 是(不占有位置) |   带有定位的父级   |     常用     |
    |  fixed固定定位   | 是(不占有位置) |    浏览器可视区    |     常用     |
    |  sticky粘性定位  |  否(占有位置)  |    浏览器可视区    | 当前阶段很少 |

定位叠放次序z-index:
   在使用定位布局时，可能会出现盒子重叠的情况。此时，可以使用z-index来控制盒子的前后次序(Z轴)
   选择器{z-index:1}; 
   1. 数值可以是正整数、负数或0，默认是auto，数值越大，盒子越上
   2. 如果属性值相同，则按照书写顺序，后来居上
   3. 数值后面不能加单位
   4. 只有定位的盒子才有z-index属性
定位拓展：

    1.加了绝对定位的盒子不能通过margin：0 auto 水平居中，但是可以通过计算方法实现水平和垂直居中
    2.浮动元素和绝对定位虽然都是浮起但是还是有一定区别的：浮动元素只会压出下面标准流的盒子但是不会压住标准流盒子里面的文字（图片），但是绝对定位（固定定位）是会压住盒子和内容的
     浮动之所以不会压住文字，因为浮动产生的最初目的是为了做文字环绕效果的。文字会围绕浮动元素）
    3.如果一个盒子既有left又有right，则默认先会执行left属性 同理既有top又有bottom则会先执行top属性

定位的特殊性：

    1.行内元素添加绝对或者固定定位，可以直接设置高度和宽度；
    2.块级元素添加绝对或者固定定位，如果不给宽度或者高度，默认大小是内容的大小;
    3.浮动元素、绝对定位（固定定位）元素都不会触发外边距合并的问题;

  5. 能够写出淘宝轮播图；
    display:
        none (隐藏元素),block(显示元素)；隐藏元素后，不再占有位置,但是审查元素的时候会发现它还是存在的只是隐藏了;
    visibility:
        hidden(隐藏元素)，visible(显示元素)；visibility隐藏元素后，继续占有原来的位置并且记得是在dom结构中还是存在的只是隐藏了；
    overflow:
        指的是内容溢出；visible(不剪切内容也不添加滚动条)、hidden(不显示超过对象尺寸的内容，超出部分隐藏掉)、scroll(不管超过内容否，总显示滚动条)、auto(超出自动显示滚动条，不超出不显示滚动条)
        一般情况下，我们都不想让溢出的内容显示出来，因为溢出部分会影响布局
        但是如果有定位的盒子，请慎用overflow:hidden，因为它会隐藏多余部分

  6. 能够说出显示隐藏的2种方式以及区别; 

  网页布局总结：

     通过盒子模型，清楚知道大部分html标签是一个盒子
     通过CSS浮动、定位可以让每个盒子排列成为网页
     一个完整的网页，是标准流、浮动、定位一起完成布局的，每个都有自己的专门用法。
     1.标准流
       可以让盒子上下排列或者左右排列，垂直的块级盒子显示就用标准流布局
     2.浮动
       可以让多个块级元素一行显示或者左右对齐盒子，多个块级盒子水平显示就用浮动布局
    3.定位
       定位最大的特点是层叠的概念，就是可以让多个盒子前后叠压来显示。如果元素自由在某个盒子内移动就用定位布局
