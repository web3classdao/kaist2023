---
layout: page
title: Speaker
nav_order: 4
description: A listing of guest speakers.
---

# Guest Speakers
The list will be updated. 

{% assign speakers = site.staffers | where: 'role', 'Speaker' %}
{% for staffer in speakers %}
{{ staffer }}
{% endfor %}
