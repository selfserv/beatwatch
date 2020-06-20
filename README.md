---
layout: default
title: Beat Watch - Proper Drum & Bass Ratings
description:  The Freshest Drum & Bass Ratings
permalink: /
datatable: true 
---
<ul>

<div class="datatable-begin"></div>
<table id="sampleTable" class="display">
  {% for row in site.data.choons | sort: 'Rating' | reverse  %}
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
</ul>
<div class="datatable-end"></div>
