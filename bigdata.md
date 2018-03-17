---
title: bigdata
permalink: /bigdata/
categories: bigdata
---
<div class="container">
  <div id="article">
{% assign hasSimilar = '' %}
{% for post in site.posts  %}
    {% assign postHasSimilar = false %}
    {% for tag in post.categories %}
        {% for thisTag in page.categories %}
               <li><span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><time class="pull-right post-list">{{ post.date | date_to_string | date: "%b %-d, %Y"  }}</h4></time></span></span></li>
        {% endfor %}
    {% endfor %}
{% endfor %}
</div>

