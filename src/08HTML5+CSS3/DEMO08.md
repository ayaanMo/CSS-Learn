HTML5语义性标签
    * <header> 头部标签
    * <nav> 导航标签
    * <article> 内容标签
    * <section> 定义文档某个区域
    * <aside> 侧边栏标签
    * <footer> 尾部标签
  注意：
    * 这种语义化标准主要是针对搜索引擎的
    * 这些标签页面中可以使用多次
    * 在IE9中，需要把这些元素转换成块级元素
    * 移动端更喜欢这些标签
    * HTML5还增加了很多其他标签
HTML5新增标签
    * 视频<video>  支持三种格式 MP4、WebM（IE不支持，Safari不支持）、Ogg（IE不支持，Safari不支持）
        <video src="文件地址" controls="controls">
        常用属性：
            autoplay:自动播放(chrome一般是禁用这个功能的);
            muted:静音播放(配合自动播放使用可以解决chrome不自动播放);
            controls:视频播放控件；
            loop：播放完是继续播放视频，循环播放;
            preload:auto(预先加载视频) none(不应加载视频) 规定是否预加载视频，如果有了autoplay，就忽略该属性
            poster:加载等待的图画图片
    * 音频<audio> 支持三种格式 MP3、WavOgg（IE不支持）、Ogg（IE不支持，Safari不支持）
        <audio src="文档地址" controls="controls"></audio>
        常用属性:
            autoplay:音频就绪后会自动播放
            controls:向用户显示控件，比如播放键
            loop:当音频结束时重新开始播放
    总结：
        音频标签和视频标签使用方式基本一致
        浏览器支持情况不同
        谷歌浏览器把音频和视频自动插放禁止了
        我们可以给视频标签添加muted属性来静音播放视频,音频不可以(可以通过Javascript解决)视频标签是重点,我们经常设置自动播放,不使用controls控件,循环和设置大小属性 
CSS3新增属性:
    * 属性选择器:可以根据元素特定属性来选择元素
     注意：类选择器、属性选择器、伪类选择器权重都是10
    * 结构伪类选择器:根据文档结构来选择其元素，常用于根据父级选择器里面的子元素
        E:first-child --匹配父元素中的第一个子元素E
        E:last-child --匹配父元素中的最后一个元素E
        E:nth-child(n) --匹配父元素中的第n个子元素E 可以是数字也可以是公式 
            * n可以是数字，关键字和公式
            * n如果是数字，就是选择器第n个子元素，里面数字从1开始
            * n可以是关键字：even偶数，odd基数
            * n可以是公式  比如n+5（从第五个开始包含第五个到最后，-n+5前五个（包含第五个））
        E:first-of-type --指定类型E的第一个
        E:last-of-type --指定类型E的最后一个
        E:nth-of-type(n) --指定类型E的第n个
    注意：
        1.nth-child对父元素里面所有孩子排序选择（序号是固定的）先找到第n个孩子，看看和E是否匹配
        2.nth-of-type 对父元素里面指定子元素进行排序选择,然后再根据E找第n个孩子
    * 伪元素选择器
        伪元素选择器可以帮助我们利用CSS创建新标签元素，而不需要HTML标签，从而简化HTML结构
        ::before 在元素内部的前面插入内容
        ::after 在元素内部的后面插入内容
        注意：
          1. before和after会创建一个元素，属于行内元素
          2. 新创建的这个元素在文档树中是找不到的，所以我们称之为伪元素
          3. 语法：element::before{}
          4. before和after必须有content属性
          5. before在父元素内容的前面创建元素，after在父元素内容的后面插入元素
          6. 伪元素选择器和标签选择器权重一样，都为1
    * 盒子模型 border-box
        CSS3中可以通过box-sizing来制定盒模型。有两个值：即可指定为content-box，border-box
        可以分成两种情况：
            1.box-sizeing-conten 盒子大小为width+padding+border（以前默认的）
            2.box-sizing-border-box 盒子大小为width 那padding和border就不会成大盒子了（前提padding和border不会超过width的宽度）
    * CSS3滤镜filter
        filter CSS属性将模糊或颜色偏移等图形效果应用于元素
        语法：filter：函数(); 例如：filter:blur(5px);blur模糊处理 数值越大越模糊
    * CSS3 calc函数：
        calc()此CSS函数让你再声明CSS属性值时执行一些计算
        例如：width:calc(100% - 80px) 括号里面可以使用 + - * / 运算符前后需要加空格
    * CSS3过渡
        过渡transition 不适用Flash东华或js的情况下就可以跟元素添加效果，主要效果是当元素从一种样式变换为另一种样式时添加效果；
        过渡动画:是从一个状态渐渐的过渡到另外一个状态 我们经常跟:hover一起搭配使用
        语法：transition：过渡的属性 花费时间 运动曲线 何时开始
            1.属性：想要变化的css属性，宽度高度 背景颜色 内外边距都可以。如果想要所有属性都变化过渡写一个all就可以
            2.花费时间：单位是秒（必须写单位）
            3.运动曲线：默认是ease（可以省略）
            4.何时开始：单位是秒（必须写单位） 可以设置延迟触发时间 默认是0s（可以省略）
        口诀：谁要过渡给谁加






