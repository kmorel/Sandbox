---
layout: page
title: Dr. Moron
tagline: "&ldquo;What kind of doctor are you?&rdquo; &ldquo;The pretentious kind.&rdquo;"
---
{% include JB/setup %}

This site contains rambling articles on personal projects.  The activity on this site is somewhere in between [my professional webpage](http://www.sandia.gov/~kmorel) and [my facebook posts](https://www.facebook.com/kenneth.moreland.7).
    
## Posts

{% for post in site.posts %} 
<ul class="posts">
  <li>
    <article itemscope="itemscope"
             itemtype="http://schema.org/BlogPosting"
    	     itemprop="blogPost">
      <a href="{{ BASE_PATH }}{{ post.url }}">
        {{ post.title }} &nbsp;&nbsp;&nbsp;&nbsp;
	<span class="entry-date">
	  <time datetime="{{ post.date | date_to_xmlschema }}"
	        itemprop="datePublished">
	    {{ post.date | date: "%B %d, %Y" }}
	  </time>
	</span>
      </a>
    </article>
  </li>
</ul>
{% endfor %}
