{% assign data = include.data %}

<ul>
{% for material in data.daily %}
<li style="margin-bottom: 10px;"><b>{{ material.day }}</b>
    {% if material.cover %}
        <br>covering: {{ material.cover }}
    {% endif %}
    {% if material.due %}
        <br><span style="color: #8B0000;">due: {{ material.due }}</span>
    {% endif %}
    {% if material.more %}
        <br>{{ material.more }}
    {% endif %}
    {% if material.chapter %}
        <br>(start <b>Chapter {{ material.chapter }}</b>)
    {% endif %}
    {% if material.worksheet %}
        <br>worksheet: <a href="{{ data.home }}/{{ material.worksheet }}">{{ material.worksheetname }} (PDF)</a>
    {% endif %}
    {% if material.doc %}
        <br><a href="{{ data.home }}/{{ material.doc }}">{{ material.docname }}</a>
    {% endif %}
    {% if material.otherurl %}
        <br><a href="{{ material.otherurl }}">{{ material.otherurlname }}</a>
    {% endif %}
</li>
{% endfor %}
</ul>
