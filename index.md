---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

## <center>Welcome to Draft Academy</center>

Draft academy believes in teaching important programming skills in a simple and easy to follow
manor. Many tutorials teach you how to solve specific real world problems, but sometimes that 
can leave you wondering how to expand your skills to projects that you haven't explicity been 
taught. By teaching you the basic syntax and ideas that every program uses, we belive that you
will be better equiped to expand your skills into more real world applications.

# Tutorials and Informative Articles:

{% for post in site.categories.informative %}
<h1><a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></h1>
{% endfor %}