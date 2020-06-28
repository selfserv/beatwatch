We help you find the best drum & bass music. We keep digging through the crates so you don't have to!
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
{% include advertisements.html %}
