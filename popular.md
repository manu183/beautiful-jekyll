---
layout: page
title: "Hi, I'm Manuel"
subtitle: Computer Science Student / Sports Fan / Machine Learning / Computer Vision
css: "/css/index.css"
meta-title: "Manuel Lang / Computer Science student at KIT"
meta-description: "Computer Science student focusing on Artificial Intelligence and Robotics interested in state-of-the-art technologies, sports, books and travelling."
use-site-title: true
bigimg:
  - "/img/hockenheimring-2016.jpg" : "Formula 1, Hockenheim, Germany (2016)"
  - "/img/lindau-2015.jpg" : "Lindau, Germany (2015)"
  - "/img/jamaica-2015.jpg" : "Treasure Beach, Jamaica (2015)"
  - "/img/nyc-2014.jpg" : "New York City, NY, USA (2014)"
  - "/img/daytona-beach-2014.jpg" : "Daytona Beach, FL, USA (2014)" 
---

<div class="list-filters">
  <a href="/" class="list-filter">All posts</a>
  <span class="list-filter filter-selected">Most Popular</span>
</div>

<div class="posts-list">
  {% for post in site.tags.popular %}
  <article>
    <a class="post-preview" href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>
	
	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>

      <div class="post-entry">
        {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
        <span href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</span>
      </div>
    </a>  
   </article>
  {% endfor %}
</div>