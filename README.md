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
        <em class="title">『 希望 』</em>
        <div class="tab-content">
            <section style="writing-mode: tb-rl;letter-spacing:3px;float:right;margin-top:10px;">
                <p style="font-size:16px;">「微微的希望」</p>
                <p style="text-align:right;color:#636363;">--孤城</p>
                <p>我和无数 </p>
                <p>不能孵化的卵石</p>
                <p>垒在一起</p>
                <p>蓝色的河溪慢慢爬来 </p>
                <p>把我们吞没</p>
                <p>又悄悄吐出</p>
                <p>没有别的</p>
                <p>只希望草能够延长</p>
                <p>它的影子</p>
            </section>
        </div>
    </label>
    <label  >
        <input type="radio" name="tabs" />
        <em class="title">
            <svg version="1.1" width="34px" height="50px" fill="#ffffff" x="0px" y="0px" viewBox="0 0 64 64" style="enable-background:new 0 0 64 64;" xml:space="preserve">
                <g>
                    <path d="M38.786,16h-0.063c0,0-8.713-9.172-16.316-2.202c-4.444,4.074-4.011,11.316,0.559,18.023c1.739-1.373,4.439-3.002,7.491-3.002c2.214,0,4.241,0.829,6.024,2.464c2.535,2.324,3.551,5.704,2.86,9.517c-0.186,1.028-0.501,2.049-0.908,3.059c0.098,0.04,0.192,0.084,0.29,0.124l0.063,0.246c17.267-6.97,23.92-23.461,16.316-30.431C47.499,6.828,38.786,16,38.786,16z"/>
                    <path d="M22.397,55.957l0.049-0.074c7.354-2.969,12.224-7.999,14.159-12.833c1.596-3.988,1.196-7.842-1.476-10.292c-1.544-1.415-3.147-1.938-4.673-1.938c-2.52,0-4.823,1.424-6.307,2.611C23.091,34.275,22.446,35,22.446,35h-0.049c0,0-3.696-4.18-8.01-4.181c-1.526,0-3.129,0.523-4.673,1.938C3.803,38.176,8.974,50.538,22.397,55.957z"/>
                </g>
            </svg>
        </em>
        <div class="tab-content">
            <img style="width:100%;" src="http://d3.freep.cn/3tb_16051014451625ue564436.jpg" alt="">
            <p style="text-align:right;margin: 4px 0 0 0;color:#4e4e4e;">2013 蒙自·南湖</p>
        </div>
    </label>
    <label >
        <input type="radio" name="tabs" />
        <em class="title">二维码</em>
        <div class="tab-content">
            <p style="text-align:center;">
                <img style="-webkit-filter:grayscale(1);filter:grayscale(1);" src="http://d3.freep.cn/3tb_160512092739u7ec564436.png" alt="微信二维码" />
            </p>
            <p style="text-align:center;">加微信  来撩骚</p>
        </div>
    </label>
</div>
```
