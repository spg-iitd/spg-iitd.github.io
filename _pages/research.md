---
title: "SPRING Lab - Research"
layout: textlay
excerpt: "SPRING Lab -- Research"
sitemap: false
permalink: /research/
---

# Research

<div class="row">
{% for data in site.data.research %}
<div class="col-sm-12 clearfix">
<div class="well">
<div class="row">
<div class="col-sm-4">
<img src="{{ site.url }}{{ site.baseurl }}/images/respic/{{ data.image }}" class="img-responsive res-photo" alt="{{ data.title }}" />
</div>
<div class="col-sm-8">
<pubtit>{{ data.title }} </pubtit>
<div style="clear: both;">
  <p>{{ data.description }}</p>
  <p>Members: <em>{{ data.students }}</em></p>
</div>
</div>
</div>
</div>
</div>
{% endfor %}

<!-- {% assign number_printed = 0 %}
{% for data in site.data.research %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if data.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<div class="well">
  <pubtit>{{ data.title }} </pubtit>
  <div style="clear: both;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ data.image }}" class="img-responsive res-photo" />
  <p>{{ data.description }}</p>
  <p>Members: <em>{{ data.students }}</em></p>
  </div>
</div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %} -->