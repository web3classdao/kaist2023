---
layout: page
title: Staff
nav_order: 2
description: A listing of all the course staff members.
---

# Staff

## Instructors

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistants (Volunteer)

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign community_staff = site.staffers | where: 'role', 'Community Staff' %}
{% assign num_community_staff = community_staff | size %}
{% if num_community_staff != 0 %}
## Community Staff (Volunteer)

{% for staffer in community_staff %}
{{ staffer }}
{% endfor %}
{% endif %}
