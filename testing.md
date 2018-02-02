---
layout: page
title: "Hey, It's Marty."
subtitle: "He Writes, He Codes, He Draws"
bigimg: "img/softserveTwilightDim.jpg"
share-img: "martyav.github.io/img/softserveTwilight.jpg"
use-site-title: true
---


  {% for post in paginator.posts %}
 
    {{ post.url | prepend: site.baseurl }}
	  {{ post.title }}

	  {% if post.subtitle %}
	 
	    {{ post.subtitle }}

	  {% endif %}
    
      Posted on {{ post.date | date: "%B %-d, %Y" }}

      {% if post.image %}
        {{ post.url | prepend: site.baseurl }}
      {% endif %}
        {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }}
        {% assign excerpt_word_count = post.excerpt | number_of_words %}
        {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
          {{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]
        {% endif %}

    {% if post.tags.size > 0 %}
      Tags:
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ site.baseurl }}/tags#{{- tag -}}">{{- tag -}}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    {% endif %}

  {% endfor %}

{% if paginator.total_pages > 1 %}
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  {% endif %}
{% endif %}
