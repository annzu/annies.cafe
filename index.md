---
title: Annie's Cafe
layout: default
---
<div class="columns">
   <section class="column is-three-quarters">
      {% for post in site.posts limit:3 %}
         <div class="content">
            <h2 class="title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
            <p class="subtitle">
               {{ post.date | date_to_string }}
               {% for category in post.categories %}
                  <span class="tag">{{category}}</span>
               {% endfor %}
            </p>
            {{ post.excerpt }}
            <p>
               <a href="{{ post.url }}">Read more.</a>
            </p>
         </div>
      {% endfor %}
   </section>
   <aside class="column is-one-quarters is-hidden-mobile">
      {% include recent-posts.html %}
      {% include about.html %}
   </aside>
</div>
