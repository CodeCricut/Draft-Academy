---
layout: post
title: JavaScript Projects
categories: portfolio
permalink: javascript-projects
---

{% for post in site.categories.javascript-project %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="https://github.com/CodeCricut/{{ post.title }}">{{ post.title }}</a></li>
{% endfor %}