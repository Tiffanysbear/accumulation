## event.target 和 event.currentTarget 的区别
>  [event.target 和 event.currentTarget 的区别](http://www.calledt.com/target-and-currenttarget/)
> 
> 冒泡和捕获： 当addEventListener的第三个参数为true的时候，代表是在捕获阶段绑定；当第三个参数为false或者为空的时候，代表在冒泡阶段绑定
> 

结论：event.target指向引起触发事件的元素，而event.currentTarget则是事件绑定的元素，只有被点击的那个目标元素的event.target才会等于event.currentTarget。


## line-heiht


* 所有浏览器都支持line-height，但ie不支持 line-height 的 inherit 值
* line-height 不允许设置负值
* 未设高度的空div中的文字之所以有高度，是因为line-height。在inline box模型中，有个line boxes，line-boxes是根据文案、图片等这些资源生成的一个高度框，自身不产生高度。line-boxes的默认高度为字体高度的110%
* 使用height会使标签haslayout，而使用line-height则不会。



## IE8问题
* 在背景上放置链接，是不可点击的，通过设置层级z-index也不行。hack方法：为链接设置position: relative 或者 设置background: #fff，在将背景设置透明``` opacity: 0; filter: alpha(opacity=0); ```

## 移动端
* active伪类在PC端的作用为鼠标点击到放开时给元素添加样式用，呈现目标被点击的激活状态。需要在按钮元素或body/html上绑定一个touchstart事件才能激活:active状态。
<br>``` document.body.addEventListener('touchstart', function (){}); //...空函数即可 ```

## 居中问题

* 多行高度不定文字居中，padding-top和padding-bottom设置相同即可
* 单行文本的垂直居中，line-height = height
* 多行文本的高度固定居中, display:table和display:table-cell的使用方法，前者必须设置在父元素上，后者必须设置在子元素上。vertical-align 用来指定行内元素（inline）或表格单元格（table-cell）元素的垂直对齐方式。