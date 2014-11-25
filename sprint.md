---
title: Sprints
layout: page
---

{% for sprint in site.sprints | sort: end_date %}
### {{sprint.title}} (ends on {{sprint.end_date}})
{% for initiative in sprint.initiatives %}
{% for blob in site.initiatives %}
{% if blob.slug == initiative && sprint.%}
* [{{ blob.title }}]({{site.baseurl}}/initiatives/{{ blob.slug }}.html) (led by {{ blob.lead }})
{% endif %}
{% endfor %}
{% endfor %}
{% endfor %}

