---
layout: page
title: Categories
permalink: /categor/
---
<!-- categories -->	
{% for category in site.categories %}
<div class="box">
	<h1>{{ category | first }}<a name="{{ category | first | cgi_escape }}"></a></h1>
	<ul class="postList">	
	{% for posts in category %}
      {% for post in posts %}
		<li><a href="{{ post.url }}" title="{{ post.excerpt }}">{{ post.title }} 
			<span>{{ post.date | date: '%d.%m.%y' }}</span></a></li>						
	{% endfor %}{% endfor %}
	</ul>
</div>				
{% endfor %}
	

