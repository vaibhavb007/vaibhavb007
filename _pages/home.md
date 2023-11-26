---
title: "Home"
layout: homelay
sitemap: false
permalink: /
---

### About me

Vaibhav Bhosale is a third-year Ph.D. student at Georgia Tech advised by Prof. Ada Gavrilovska and Dr. Ketan Bhardwaj. His research is focused on building systems and networking solutions for LEO satellite networks. He has explored different aspects related to LEO satellite networks such as control plane management, edge application deployment, route variability, and cellular deployment.

{% for member in site.data.pi %}
<div class="jumbotron">
### Education
 <ul style="overflow: hidden">
  <li> {{ member.education1 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education2 | replace: "-","&#8211;"}} </li>
  <li> {{ member.education3 | replace: "-","&#8211;"}} </li>
  </ul>
</div>
{% endfor %}

{% if site.data.experience %}
<div class="jumbotron">
### Professional Experience
<ul>
{% for member in site.data.experience %}
<li><i>{{member.title}}</i> at <b>{{member.company}}</b> {{member.team}}  {{member.period}}
{% if member.mentor %}
Mentored by: {{member.mentor}}
{% endif %}
</li>
{% endfor %}
</ul>
</div>
{% endif %}