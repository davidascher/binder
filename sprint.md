---
title: Sprints
layout: page
---

<ul>
{% for sprint in site.data.allsprints.sprints %}
  <li> {{sprint.name}}
  <ul>
   {% for initiative in sprint.initiatives %}
   <li>
   	  P{{ initiative.priority }}: 
      {{ initiative.name }} (led by 
      {{ initiative.lead }})
  </li>
   {% endfor %}
  </ul>
  </li>
{% endfor %}
</ul>