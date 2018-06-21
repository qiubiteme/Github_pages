**流式布局**：就是百分比布局，非固定像素，

内容向两侧填充，理解成流动的布局，称为流式布局



**视觉窗口**：viewport,是移动端特有。

这是一个虚拟的区域，承载网页的。

  **承载关系**：浏览器---->viewport---->网页/



## **适配要求：**

    1. **网页宽度必须和浏览器保持一致** 

    2. **默认显示的缩放比例和PC端保持（缩放比例1.0）** 

    3. **不允许用户自行缩放网页**  

        满足这些要求达到了适配，国际上通用的适配方案，

       标准的移动端适配方案。*/*

       ## **适配设置：**    

       如果任何设置都没有，默认走的就是viewport的默认设置    

       去设置新的viewport设置,达到适配要求。 

       ```
          <meta name="viewport"> 
       ```

       设置视口的标签  在head里面并且应该紧接着编码设置   

       ##  **viewport的功能：**

       width    可以设置宽度   (device-width 当前设备的宽度)   

       height   可以设置高度   

       initial-scale  可以设置默认的缩放比例  

       user-scalable  可以设置是否允许用户自行缩放   

       maximum-scale  可以设置最大缩放比例    

       minimum-scale  可以设置最小缩放比例  

       

       ###   **在viewport** 上 content使用参数   

       ```
       <meta name="viewport" content="width=device-width,initial-scale=1.0,user-scalable=0">
       ```

       width=device-width   宽度一致比例是1.0   

       initial-scale=1.0        宽度一致比例是1.0   

       user-scalable=no     不允许用户自行缩放  （yes，no  1,0）    

       标准适配方案：  

       ```
         <meta name="viewport" content="width=device-width,initial-scale=1.0,user-scalable=0">  
       ```

         meta:vp + tab  快捷方式

       # Viewport的设定

       ------

       ```
       <meta name="viewport" content="width=device-width, initial-scale=1"> 1
       ```

       作用是设置可视区域的**宽度**及**初始缩放比例**

       **1 `width`可视区域的宽度，值可为数字或关键词 `device-width`、`phys.width`**

       - `device-width`：又指 `css-width`，通过 `window.screen.width` 获取
       - `phys.width`：物理宽度，通过 `document.documentElement.clientWidth` 获取

       通常 `device-width` 和 `phys.width` 不相等，如 iPhone6 的 `phys.width` 为 750px，而 `css-width` 为 375px

       **2 `height`可视区域的高度**

       **3 `initial-scale`可视区域初始缩放比例**

       **4 maximum-scale允许用户缩放的最大比例，`1.0` 将禁止用户放大到实际尺寸以上**

       **5 minimum-scale允许用户缩放的最小比例，`1.0` 将禁止用户缩小到实际尺寸以下**

       **6 user-scalable是否允许用户手动缩放，`no` 禁止缩放**

       详细说明：

       浏览器如果把电脑端宽度为 980px 的网页展现在宽度为 750px 的 iPhone6 手机屏上，势必会放不下，手机端横向会出现滚动条，怎么阻止这种情况呢，很简单，浏览器默认一个虚拟窗口，不同浏览器有不同的虚拟窗口宽度的默认值，如：

       - Safari iPhone：980px
       - opera：850px
       - Andriod webkit：800px
       - IE：974px

       然后把这个 980px 虚拟窗口装进宽度为 750px 的 iPhone6 中，当然这样的话必须缩放，这就是为什么在手机中展现电脑端页面没有出现横向滚动条，而且字迹明显变小的原因。

       `meta` 标签中，`width` 有两个含义：

       I `width` 是`phys.width`

       II `width` 也是虚拟窗口的 `width`

       这样就会有两个结果：

       I iPhone6 的 `phys.width` 也变成了 `css-width` 即 375px，可以通过 `document.documentElement.clientWidth` 获取得到此时 `phys.width` 确实为 375px

       II 如果是 375px 的手机端页面，此时的虚拟窗口的宽度也为 375px，再装进 `phys.width` 为 375px 的手机时，当然如设计的效果一致，不会缩放，也不会出现横向滚动条

       此外还会影响响应式布局和媒体查询

       ```
       @media only screen and (min-width: 350px) and (max-width: 480px){.....................}1
       ```

       如没有meta标签，此时的 `width` 当然即为 `phys.width`，iPhone6 就不会执行上边的括号里边的代码，但是有了 `meta` 标签以后呢，`width` 变成了 `css-width`，即为 375px,，所以是会执行代码的。

       从以上可以看出，有了 `meta` 标签以后，原本的 iPhone6，即像素比为2的手机，可以按照 `css-width`相同的像素比为1的手机一样正常显示，像素比更高的手机也能正常显示。当然现在 andriod 的 2K 屏在 `meta` 标签的帮助下也能正常显示。即对于开发者来说，已经可以不管手机的像素比，只需按照 css 像素编写代码即可。



## 非主流的适配方案：

1.页面的真实尺寸会比在设备的上尺寸要大几倍
2.假设设备是iphone4 -> 320px -> 网页尺寸 640px
3.缩放操作，有2倍的  有3倍  和屏幕像素比有关系
4.什么是屏幕像素（物理像素，像素点） px(页面的尺寸单位)
5.物理像素 是设备显示屏的最小可视颗粒的大小   以前的手机（直板手机）
6.现在有 高清显示屏  视网膜屏  retina屏
7.显示的效果就提高了更细腻，但是在显示同等质量的图片的时候（模糊效果）

8.在屏幕像素比（一个px宽的屏幕能放几个物理像素）高的设备  图片（非矢量）显示会模糊
9.提高网页的清晰度  根据屏幕的像素比 来缩放网页
10.但是这样的适配方案成本非常高
11.一般的企业开发当中使用的还是标准化设置

在高清显示屏当中：图片可能会失真（模糊）