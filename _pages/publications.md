---
title: "SPRING Lab - Publications"
layout: gridlay
excerpt: "SPRING Lab -- Publications."
sitemap: false
permalink: /publications/
---

# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications and patents](#full-list-of-publications).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
<div class="well">
  <pubtit>{{ publi.title }} </pubtit>

  <!-- <span style="background-color: green; color: white; padding: 1px 4px; border-radius: 2px; font-size: 12px;">{{ publi.tag }}</span> -->

<div style="clear: both;">
  <!-- <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" style="width: 50%; float: left; margin-right: 15px;" /> -->
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive pub-photo" />
{% if publi.description.size > 500 %}
  <p>{{ publi.description | slice: 0, 500 }}...</p>
{% else %}
  <p>{{ publi.description }}</p>
{% endif %}
<p><em>{{ publi.authors }}</em></p>
</div>

<div style="display: flex; gap: 10px;">
<strong>{{ publi.venue }}</strong>
{% if publi.award %}
<span style="background-color: maroon; color: white; padding: 1px 4px; border-radius: 2px; font-size: 12px;"><i class="fas fa-award" style="font-size: 12px;"></i> {{ publi.award }}</span>
{% endif %}
<span style="background-color: green; color: white; padding: 1px 4px; border-radius: 2px; font-size: 12px;">{{ publi.tag }}</span>
</div>


<div style="display: flex; gap: 10px;">
{% if publi.pdf %}
  <a href="{{ publi.pdf }}" target="_blank">
    <button class="btn btn-primary btn-lg" style="padding: 5px 10px; border-radius: 10px; background-color: black;">
      <i class="fas fa-file-pdf" style="font-size: 15px;"></i> PDF
    </button>
  </a>
{% endif %}

{% if publi.website %}
  <a href="{{ publi.website }}" target="_blank">
    <button class="btn btn-primary btn-lg" style="padding: 5px 10px; border-radius: 10px; background-color: black;">
      <i class="fas fa-globe" style="font-size: 15px;"></i> Website
    </button>
  </a>
{% endif %}

{% if publi.code %}
  <a href="{{ publi.code }}" target="_blank">
    <button class="btn btn-primary btn-lg" style="padding: 5px 10px; border-radius: 10px; background-color: black;">
      <i class="fab fa-github" style="font-size: 15px;"></i> Code
    </button>
  </a>
{% endif %}

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
{% endif %}

<p> &nbsp; </p>


<!-- ## Patents
<em>Milan P Allan, S Gröblacher, RA Norte, M Leeuwenhoek</em><br />Novel atomic force microscopy probes with phononic crystals<br /> PCT/NL20-20/050797 (2020)

<em>Milan P Allan</em><br /> Methods of manufacturing superconductor and phononic elements <br /> <a href="https://patents.google.com/patent/US10439125B2/en?inventor=Milan+ALLAN&oq=inventor:(Milan+ALLAN)">US10439125B2 (2016)</a> -->

## Full List of Publications

### Conference Publications
{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br />
  <strong>{{ publi.venue }}</strong> {% if publi.award %}
<span style="background-color: maroon; color: white; padding: 1px 4px; border-radius: 2px; font-size: 12px;"><i class="fas fa-award" style="font-size: 12px;"></i> {{ publi.award }}</span>
{% endif %} <span style="background-color: green; color: white; padding: 1px 4px; border-radius: 2px; font-size: 12px;">{{ publi.tag }}</span>
<div style="display: flex; gap: 10px; margin-top: -5px;">
{% if publi.pdf %}
  <a href="{{ publi.pdf }}" target="_blank">
    <button class="btn btn-primary btn-lg" style="padding: 2px 6px; border-radius: 6px; background-color: black;">
      <i class="fas fa-file-pdf" style="font-size: 12px;"></i> PDF
    </button>
  </a>
{% endif %}

{% if publi.website %}
  <a href="{{ publi.website }}" target="_blank">
    <button class="btn btn-primary btn-lg" style="padding: 2px 6px; border-radius: 6px; background-color: black;">
      <i class="fas fa-globe" style="font-size: 12px;"></i> Website
    </button>
  </a>
{% endif %}

{% if publi.code %}
  <a href="{{ publi.code }}" target="_blank">
    <button class="btn btn-primary btn-lg" style="padding: 2px 6px; border-radius: 6px; background-color: black;">
      <i class="fab fa-github" style="font-size: 12px;"></i> Code
    </button>
  </a>
{% endif %}

</div>

{% endfor %}
