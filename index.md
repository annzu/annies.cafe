---
title: Annie's Cafe
layout: default
---
<div class="columns">
   <section class="column is-three-quarters">
      {% for post in site.posts limit:5 %}
         {% include post-item.html %}
      {% endfor %}
   </section>
   <aside class="column is-one-quarters is-hidden-mobile">
      {% include recent-posts.html %}
      {% include about.html %}
   </aside>
</div>
