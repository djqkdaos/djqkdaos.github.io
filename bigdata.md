---
title: bigdata
permalink: /bigdata/
categories: bigdata
---
<div class="container">
  <div id="article">
  <h1>BigData</h1>
  <ul class="posts">
{% assign hasSimilar = '' %}
{% for post in site.posts  %}
    {% assign postHasSimilar = false %}
    {% for tag in post.categories %}
        {% for thisTag in page.categories %}
            {% if postHasSimilar == false and hasSimilar.size < 6 and post != page and tag == thisTag %}
               <li><span><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><time class="pull-right post-list">{{ post.date | date_to_string | date: "%b %-d, %Y"  }}</time></span></li>
                {% capture hasSimilar %}{{ hasSimilar }}*{% endcapture %}
                {% assign postHasSimilar = true %}
            {% endif %}
        {% endfor %}
    {% endfor %}
{% endfor %}
 </ul>
</div>

