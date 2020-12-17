---
layout: blog_home
---

[Subscribe to the newsletter](http://subscribe.ladsantos.org) to get an email notification whenever there is a new post.

Recent posts
============

<div class="posts">
  {% for post in site.posts limit:5 %}
    <article class="post">

      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>

Archive
=======

**Disclaimer**: *The contents of this blog do not represent the views of any organization or institution, and reflect only the opinions of the author.*

{% for tag in site.tags reversed %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li>{{ post.date | date: "%B %e"}}: <i><a href="{{ post.url }}">{{ post.title }}</a></i></li>
    {% endfor %}
  </ul>
{% endfor %}