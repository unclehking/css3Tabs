# css3Tabs
纯css3实现的tab选项卡

[Demo -- 演示页面](http://unclehking.github.io/css3Tabs/)

截图： <br />
![github](http://unclehking.github.io/css3Tabs/screenshot.jpg "github")  

css：

```java  
    *{-webkit-tap-highlight-color:rgba(255,0,0,0);}
    .tabs {width: 100%;max-width:520px; height: 410px; list-style: none;position: relative;padding: 0px;margin: 0px;color:#fff; }
    .tabs:after{display: block;content: " ";width: 0px;height: 0px;clear: both;float: none;}
    .tabs label{float: left;display: block;width: calc(100% / 3);height: 50px;}
    .tabs input[type="radio"]{display: none;}
    .tabs label{display: block;height: 50px; font-size: 18px;text-align: center;background: #0276BC;cursor: pointer;}
    .tabs .tab-content{z-index: 2;display: none;overflow: hidden; width: calc(100% - 13px * 2);min-height: 260px;line-height: 14px;padding: 12px;position: absolute;top: 50px;left: 0;border: solid #ffffff 1px;border-top: none;color: #000000;text-align: left;cursor: default;font-weight: normal; font-size: 14px;background: #ffffff;box-shadow: 3px 3px 8px rgba(0,0,0,.04),-3px 0 8px rgba(0,0,0,.04);}
    .tabs input[type=radio]:checked ~ .tab-content{display: block;}
    .tabs label em{display: block;width: 100%;height: 100%;line-height: 2.6em; font-style: normal;position: relative; }
    .tabs label em:after{display: block;content: " ";width: 0%;height: 3px;background-color: #ff4081;-webkit-transition: all 0.3s ease-in-out;-moz-transition: all 0.3s ease-in-out;transition: all 0.3s ease-in-out;position: absolute;left: 50%;bottom: 0px;}
    .tabs input[type=radio]:checked + em:after{width: 100%;left: 0px;}
    .tabs label em:before{display: none;z-index: 1;content: " ";position: absolute;top: 50%;left: 50%;width: 0;height: 0; border-radius: 50%; background-color: #f8f8f8;opacity: 0.6;-webkit-transition: all 0.5s ease-in-out;-moz-transition: all 0.5s ease-in-out;transition: all 0.5s ease-in-out;}
    .tabs label em:hover:before{display: block;}
    .tabs input[type=radio]:checked + em:before{width:240px;height:240px;left:calc(-120px + 50%);top:calc(-120px + 50%);opacity: 0;}
```

html:
```java  
<div class="tabs">
    <label >
        <input type="radio" name="tabs" checked />
        <em class="title"><!--title--></em>
        <div class="tab-content">
            <!--content-->
        </div>
    </label>
    ，，，
</div>
```
