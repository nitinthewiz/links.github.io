---
title: "ProtoFlow: Coverflow for Prototype"
slug: protoflow-coverflow-for-prototype
date: 2008-03-11 08:28:35 -0500
category: 
external-url: http://ajaxian.com/archives/protoflow-coverflow-for-prototype
hash: dd71d30103950bd35cd8d86f3beae283
year: 2008
month: 03
scheme: http
host: ajaxian.com
path: /archives/protoflow-coverflow-for-prototype

---

Obaid Ahmed has written a coverflow-like component on top of Prototype and Script.aculo.us called ProtoFlow.

It is simple to use:

PLAIN TEXT
HTML:







<div id="protoflow">


    &lt;img src="imgs/DSCN0940_91360.jpg"/&gt;


    &lt;img src="imgs/stimme_von_oben_187192.jpg"/&gt;


    &lt;img src="imgs/Tropfen_1_Kopie_201721.jpg"/&gt;


    &lt;img src="imgs/farbraum_012_147508.jpg"/&gt;


    &lt;img src="imgs/IMG_4906_199357.jpg"/&gt;


    &lt;img src="imgs/Tropfen_1_Kopie_201721.jpg"/&gt;


    &lt;img src="imgs/Fries_201253.jpg"/&gt;


    &lt;img src="imgs/Fries_201253.jpg"/&gt;


</div>





<ul id="protoCaptions" class="protoCaptions">


    <li>Caption 1</li>


    <li>Caption 2</li>


    <li>Caption 3</li>


    <li>Caption 4</li>


    <li>Caption 5</li>





    <li>Caption 6</li>


    <li>Caption 7</li>


    <li>Caption 8</li>


</ul>








PLAIN TEXT
JAVASCRIPT:







Event.observe(window, 'load', function() &#123; 


 cf = new ProtoFlow($("protoflow"), &#123;captions: 'protoCaptions'&#125;);


&#125;);
