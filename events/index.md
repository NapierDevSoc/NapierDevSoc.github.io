---
layout: page
title:  Events
navTab: Events
weight: 30
---

## Activities
The society organises many events for its members - both on a regular, scheduled basis and ad-hoc, as other possibilities present themselves.

Key activities that we are involved in include:

- Weekly co-working spaces and social nights out
- Monthly tech-related talks and workshops
- Attendance to local meetups, sessions and hackathons 

Please check our calendar below for information on relevant, upcoming events that may be of interest to NDS members.

## Calendar
<iframe src="https://www.google.com/calendar/embed?src=j0js43u21s8tu9j2s1q9bhhrtk%40group.calendar.google.com&ctz=Europe/London" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>

## Upcoming Events
<div class="posts">
  {% if site.categories.events %}
  {% for post in site.categories.events reversed limit:5 %}
    <div class="post">  
      <h2>
        <a href="{{ post.url | prepend: site.baseurl }}">
          {{ post.title }}
          {% if post.category != 'minutes' %}
            <small>{{ post.date | date: "%B %-d, %Y" }}</small>
          {% endif %}
        </a>
      </h3>
      <p class="post-meta">
        Published by <a href="https://github.com/{{ post.author }}">{{ post.author }}</a>
      </p>


      <div class="content">
        {{ post.excerpt | remove: '<h2>' | remove: '</h2>' }}
      </div>
    </div>
  {% endfor %}
  {% else %}
  <p> No upcoming events at this time, please check back soon. </p>
  {% endif %}
</div>
