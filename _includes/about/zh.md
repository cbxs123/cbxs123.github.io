> 写写代码，做做设计  
> 大道至简，唯有坚持

Hey，我是**厂白小赛(Ysai)**，一只在深圳工作的程序猿，主营大数据挖掘与分布式计算。

工作之余，爱好健身（跑步、羽毛球），喜欢看书，以及来一场说走就走的旅行。

博客采用<a href="https://pages.github.com/" target="_blank">GitHub Pages</a>与<a href="http://jekyll.com.cn/" target="_blank">Jekyll</a>搭建，感谢👉<a href="https://github.com/mzlogin/mzlogin.github.io" target="_blank">码志</a>和<a href="https://github.com/Huxpro/huxpro.github.io" target="_blank">黄玄</a>的开源主题，欢迎提出探讨~

## 联系

{% for website in site.data.social %}

- {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
  {% endfor %} 

## 技能

{% for category in site.data.skills %}

### {{ category.name }}

<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>

{% endfor %}