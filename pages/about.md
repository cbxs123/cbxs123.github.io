---
layout: page
title: About
description: Less is More
keywords: Ysai
comments: true
menu: 关于
permalink: /about/
---

<select class="sel-lang" onchange= "onLanChange(this.options[this.options.selectedIndex].value)">
    <option value="0" selected> 简  介 </option>
</select>
<div class="zh post-container">
    {% capture about_zh %}{% include about/zh.md %}{% endcapture %}
    {{ about_zh | markdownify }}
</div>
<script type="text/javascript">
    // get nodes
    var $zh = document.querySelector(".zh");
    var $select = document.querySelector("select");

    // bind hashchange event
    window.addEventListener('hashchange', _render);
    
    // handle render
    function _render(){
        var _hash = window.location.hash;
        // en
        if(_hash == "#en"){
            $select.selectedIndex = 1;
            $en.style.display = "block";
            $zh.style.display = "none";
        // zh by default
        }else{
            // not trigger onChange, otherwise cause a loop call.
            $select.selectedIndex = 0;
            $zh.style.display = "block";
            $en.style.display = "none";
        }
    }
    
    // handle select change
    function onLanChange(index){
        if(index == 0){
            window.location.hash = "#zh"
        }else{
            window.location.hash = "#en"
        }
    }
    
    // init
    _render();
</script>





