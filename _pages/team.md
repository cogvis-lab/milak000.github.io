---
layout: page
permalink: /team/
title: Team
description: Members and close collaborators of the group.
nav: true
nav_rank: 2
---

{% assign groups = site.members | sort: "group_rank" | map: "group" | uniq %}
{% for group in groups %}
## {{ group }}

    {% assign members = site.members | sort: "lastname" | where: "group", group %}
    {% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                
            </div>
            
        </div>
    </div>
</p>
    {% endfor %}
{% endfor %}
