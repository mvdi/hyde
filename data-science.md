---
title: Data Science
layout: page
---

<div class="message">
A place to link useful resources.
</div>

## Courses
Courses I'm taking.

## Reading List
Useful resources.

# Recent Posts
<div class="message">
A place to document my machine learning self study.
</div>
{% assign blog_sorted = site.datascience | reverse %}
<div class="posts">
  {% for post in blog_sorted %}
  <div class="post">
    <h2 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>

    <span class="post-date">{{ post.date | date_to_string }}</span>
    {% assign first_par = post.content | split: "<p>" | shift | first %}
    {{ first_par }}
    <p style="text-align:right"><a href="{{ post.url }}">See More</a></p>
  </div>
  {% endfor %}
</div>
