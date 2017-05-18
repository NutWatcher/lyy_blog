---
title: 表单设计器(React+Redux for Form Designer)
date: 2017-5-18 17:07:04
tags: [作品集,Redux,React]
categories: [作品集,代码作品集,React+Redux]
---
通过 React+Redux 构建的一个表单设计器
页面底部有demo
![](http://of6m03mmi.bkt.clouddn.com/post_17_5_18_templateForm1.png)

<!--more-->
<link href="http://77flf3.com1.z0.glb.clouddn.com/Component_slider_css_unslider.css" rel="stylesheet" type="text/css">
<link href="http://77flf3.com1.z0.glb.clouddn.com/Component_slider_css_unslider-dots.css" rel="stylesheet" type="text/css">
<script src="http://77flf3.com1.z0.glb.clouddn.com/Component_slider_js_unslider-min.js"></script>
<style>
.unslider-nav ol li.unslider-active {
    background: #999999;
}
.unslider-nav ol li {
    border: 2px solid #999999;
}
.unslider-arrow.prev {
    left: 20px;
    right: auto;
    -ms-transform: rotate(-180deg);
    transform: rotate(-180deg);
}
.unslider-arrow {
    display: block;
    width: 32px;
    height: 32px;
    top: 45%;
    right: -20px;
    left: auto;
    margin-top: 16px;
    overflow: hidden;
    background: rgba(0,0,0,.2) no-repeat 50% 50%;
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAkAAAAQCAQAAABuQZ3IAAAAi0lEQVR4AU3OISBEQQBAwS0AACS9NxqQgCZpkiYBVddFvWhAAUABAPQCAGC4g/0vTnrBqCfDIZl70J+kMUBPpEwT4FNXxBxz4F1HxHyr4EVTxBLb4EFNxEon4CJSlVNw9AcV9sC16h8osgke1P1ArgXwouVvdQq86ww/GQefusNf7kBviBlxpT8k+gL/Wox4r1d4MwAAAABJRU5ErkJggg==');
    background-size: 7px 11px;
    border-radius: 32px;
    text-indent: -999em;
    opacity: .6;
    transition: opacity .2s;
}
.unslider-arrow:hover {
    opacity: 1;
}
.unslider{
              position: relative;
              padding: 5px;
              margin-bottom: 50px;
              background: #ccc;
              color: #666;
              text-align: center;
              text-shadow: none;
              border-radius: 6px;
              box-shadow: 0 4px 6px rgba(0,0,0,.1);
          }
</style>
<div class="my-slider">
	<ul>
	    <li ><a href="/demo/templateForm" target="_blank"><img style="top:20px;max-height:400px;width:auto;" src="http://of6m03mmi.bkt.clouddn.com/post_17_5_18_templateForm1.png"><p>表单设计界面</p></a></li>
		<li><a href="/demo/templateForm/preview.html" target="_blank"><img style="top:20px;max-height:400px;width:auto;" src="http://of6m03mmi.bkt.clouddn.com/post_17_5_18_preiviewForm.png"><p>表单展示界面</p></a></li>
		<li><a href="/demo/templateForm/preview.html" target="_blank"><img style="top:20px;max-height:400px;width:auto;" src="http://of6m03mmi.bkt.clouddn.com/post_17_5_18_preiviewFormForIphone.png"><p>表单展示界面(响应式)</p></a></li>
		<li><a href="/demo/templateForm/showData.html" target="_blank"><img style="top:20px;max-height:400px;width:auto;" src="http://of6m03mmi.bkt.clouddn.com/post_17_5_18_dataForm.png"><p>表单结果展示界面</p></a></li>
	</ul>
</div>
<script>
	jQuery(document).ready(function($) {
			$('.my-slider').unslider({autoplay: false});
		});
</script>













<a href="/demo/templateForm" title="设计页面" target="_blank">设计页面</a>     <a href="/demo/templateForm" title="designer page" target="_blank">Designer Page</a>
<a href="/demo/templateForm/preview.html" title="form page" target="_blank">表单页面</a>     <a href="/demo/templateForm/preview.html" title="form page" target="_blank">Form Page</a>
<a href="/demo/templateForm/showData.html" title="data page" target="_blank">结果页面</a>     <a href="/demo/templateForm/showData.html" title="data page" target="_blank">Data Page</a>