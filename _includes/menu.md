{% for p in site.pages %}
    {% if p.category %}
        {% capture cur_cat %}{{p.category}}{% endcapture %}
        {% if cur_cat != cat %}
            {% unless forloop.first %}</ul>{% endunless %}
            <h3>{{cur_cat}}</h3>
            {% capture cat %}{{cur_cat}}{% endcapture %}
        {% endif %}
        <li><a href="{{p.url}}"><img src="{{p.image}}"> {{p.title}}</a></li>
    {% endif %}
{% endfor %}
