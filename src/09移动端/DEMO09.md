移动端：
    1. 视口（viewport）就是浏览器显示页面内容的屏幕区域。视口可以分为布局视口、视觉视口和理想视口
        * 布局视口（layout viewport）
            1. 一般移动设备的浏览器都默认设置了一个布局视口，用于解决早期的PC端页面在手机上显示的问题
            2. ios Android 基本都是将这个视口的分别率设置为980px，所以PC上的网页大多都能在手机上呈现，只不过元素看上去看小，一般都默认可以通过手动缩放网页
        * 视觉视口（visual viewport）
            1. 字面意思，它是用户正在看到的网站的区域。注意是网站的区域
            2. 我们可以通过缩放去操作视觉视口，但不会影响布局视口，布局视口仍然保持原来的宽度
        * 理想视口（ideal viewport）
            1. 为了使网站在移动端有最理想的浏览和阅读宽度而设定
            2. 理想视口，对设备来讲，是最理想的视口尺寸
            3. 需要手动填写meta视口标签通知浏览器操作
            4. meta视口标签的主要目的：布局视口的宽度应该与理想视口的宽度一致，简单理解就是设备有多宽，我们布局的视口就多宽。
            meta视口标签：
                <meta name="viewport" content="width-device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minmum-scale=1.0">
                    width 宽度设置的是viewport宽度，可以设置device-width特殊值
                    initial-scale 初始缩放比，大于0的数字
                    maximum-scale 最大缩放比，大于0的数字
                    minimum-scale 最小缩放比，大于0的数字
                    user-scalable 用户是否可以缩放，yes或no（1或0）
                注意：标准的viewport设置
                    1. 视口宽度和设备保持一致
                    2. 视口的默认缩放比1.0
                    3. 不允许用户自行缩放
                    4. 最大的允许缩放比例1.0
                    5. 最小允许的缩放比上1.0
    2. 物理像素&物理像素比
        * 物理像素点指的是屏幕显示的最小颗粒,是物理真实存在的。这是厂商在出厂时就设置好了比如苹果6\78是750*1334
        * 我们开发时候的1px不是一定等于1个物理像素的
        * PC端页面. 1个px等于1个物理像素的,但是移动端就不尽相同
        * 一个px的能显示的物理像素点的个数,称为物理像素比或屏幕像素比

    3. 背景缩放background-size
        background-size属性规定背景图像的尺寸
        background-size:背景图片宽度 背景图片高度（长度|宽度|cover|contain）
        cover把背景图像扩展至足够大，以使背景图像完全覆盖背景区域;
        contain把图像扩展至最大尺寸，以使其宽度和高度完全适应内容区域
    4.移动端开发选择
        * 单独开发的移动端
        * 响应式开发
    5.移动端技术解决方案
        * CSS初始化 normalize.css （推荐使用normalize.css:地址http://necolas.github.io/normalize.css)
            1. Normalize.css 保护了有价值的默认值
            2. Normalize.css 修复了浏览器的bug
            3. Normalize.css 拥有详细的文档
        * 盒子模型 box-sizing:border-box CSS3盒子模型
    6.移动端技术选型:
        * 单独开发移动端页面
          1. 流式布局
          2. flex弹性布局
          3. less+rem+媒体查询布局
          4. 混合布局
        * 响应式页面兼容移动端
          1. 媒体查询
          2. bootstrap










