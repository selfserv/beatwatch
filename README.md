---
layout: default
title: Beat Watch - Proper Drum & Bass Ratings
description:  The Freshest Drum & Bass Ratings
permalink: /
datatable: true 
---
<div class="datatable-begin"></div>
<ul>
{% for date in site.data.choons %}
  <li>{{ date.Rating" }}-{{ date.Artist }}</li>
{% endfor %}
</ul>

second table 
<table id="sampleTable" class="display">
  {% for row in site.data.choons %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
<div class="datatable-end"></div>
