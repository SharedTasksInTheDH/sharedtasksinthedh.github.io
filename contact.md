---
layout: page
title: Contact
index: 100
add_to_menu: true
---



## Organizers

{% for b in site.data.people %}
{% assign a = b[1] %}

- {{ a.name }}, {{ a.affiliation }} &nbsp;<a href="javascript:toggle('#details-{{ forloop.index }}')">&#9432; info</a><br/>
  E-Mail: [`{{ a.email }}`](mailto:{{ a.email }})<br/>
  {% for c in a.links %}{{ c.desc }}: [`{{ c.name }}`]({{ c.url }})<br/>
  {% endfor %}
  <div id="details-{{ forloop.index }}" style="display:none;">
	{{ a.bio | markdownify }}
  </div>
{% endfor %}




## Advisory Board

- [Fotis Jannidis](http://www.jannidis.de), Würzburg University
- [Jonas Kuhn](http://www.ims.uni-stuttgart.de/~jonas/), Stuttgart University
- [Jan Christoph Meister](https://www.slm.uni-hamburg.de/germanistik/personen/meister.html), Hamburg University
