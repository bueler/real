{% assign data = include.data %}
<table class="asst-table">
{% for hw in data.homework %}
<tr>
	<td>
		<table class="inner">
		  <tr>
            <td>Homework {{ hw.name }}</td>
		  </tr>
		  <tr>
            <td>due {{ hw.due }}</td>
		  </tr>
		  <tr>
            <td><a href="{{ data.home }}/{{ hw.source }}">{{ hw.source }}</a> -> <a href="{{ data.home }}/{{ hw.blank }}">PDF</a></td>
		  </tr>
		  {% if hw.seealsopdf %}
			  <tr>
                <td>see also: <a href="{{ hw.seealsopdf }}">{{ hw.seealsoname }} (PDF)</a></td>
			  </tr>
		  {% endif %}
		</table>
	</td>
</tr>
{% endfor %}
</table>
