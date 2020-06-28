<head><script data-ad-client="ca-pub-4712055147463047" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script></head>
<p style="text-align: center;"><b>We help you find the best drum & bass music. We keep digging through the crates so you don't have to!</b></p>
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
<center><footer>&copy; 2020 <a href='https://www.linkedin.com/in/csluken/'>Chris Luken</a>. All Rights Reserved.</footer></center>
