# css3Tabs
纯css3实现的tab选项卡

[Demo -- 演示页面](http://unclehking.github.io/css3Tabs/)

截图： <br />
![github](http://unclehking.github.io/css3Tabs/screenshot.png "github")  

css：

```java  
  .tabs {width: 520px;height: 410px; list-style: none;position: relative;padding: 0px;margin: 0px;color:#fff;}
  .tabs:after{display: block;content: " ";width: 0px;height: 0px;clear: both;float: none;}
  .tabs label{float: left;display: block;width: 33.3333333333333333333333%;height: 50px;}
  .tabs input[type="radio"]{display: none;}
  .tabs label{display: block;height: 50px; font-size: 18px;text-align: center;background: #0276BC;cursor: pointer;}
  .tabs .tab-content{z-index: 2;display: none;overflow: hidden;width: -webkit-calc(100% - 13px * 2);height: 332px;line-height: 24px;padding: 12px;position: absolute;top: 50px;left: 0;border: solid #0276BC 1px;border-top: none;color: #000000;text-align: left;cursor: default;font-weight: normal;}
  .tabs input[type=radio]:checked ~ .tab-content{display: block;}
  .tabs label em{display: block;overflow: hidden; width: 100%;height: 100%;line-height: 2.6em; font-style: normal;position: relative; }
  .tabs label em:after{display: block;content: " ";width: 0%;height: 4px;background-color: #FF4081;-webkit-transition: all 0.3s ease-in-out;-moz-transition: all 0.3s ease-in-out;transition: all 0.3s ease-in-out;margin: 0px auto 0 auto;}
  .tabs input[type=radio]:checked + em:after{width: 100%;}
  .tabs label em:before{display: none;z-index: 1;content: " ";position: absolute;top: 0px;left: 0px;width: 100%;height: 3px;background-color: #FF4081;-webkit-transition: all 0.3s ease-in-out;-moz-transition: all 0.3s ease-in-out;transition: all 0.3s ease-in-out;}
  .tabs label em:hover:before{display: block;}
  .tabs input[type=radio]:checked + em:before{height: 200px;opacity: 0;}
```

html:
```java  
<div class="tabs">
    <label >
        <input type="radio" name="tabs" checked />
        <em class="title">希望</em>
        <div class="tab-content">
            <div>我和无数 </div>
            <div>不能孵化的卵石 </div>
            <div>垒在一起 </div>
            <div>蓝色的河溪慢慢爬来 </div>
            <div>把我们吞没 </div>
            <div>又悄悄吐出 </div>
            <div>没有别的</div>
            <div>只希望草能够延长</div>
            <div>它的影子</div>
        </div>
    </label>
    <label  >  
        <input type="radio" name="tabs" />
        <em class="title">标题二</em>
        <div class="tab-content">
            <img style="width:100%;-webkit-filter: grayscale(1); " src="http://d3.freep.cn/3tb_160510144216ds77564436.jpg" alt="">
        </div>
    </label>
    <label >
        <input type="radio" name="tabs" />
        <em class="title">标题三</em>
        <div class="tab-content">
            <img style="width:100%;" src="http://d3.freep.cn/3tb_16051014451625ue564436.jpg" alt="">
        </div>
    </label>
</div>
```
