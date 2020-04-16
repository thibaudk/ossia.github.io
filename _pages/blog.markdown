---
layout: community-page
title:  "Blog"

permalink: /blog.html
category: site-blog
---
{% comment%}
Here we generate all the categories.
{% endcomment%}

{% assign rawcats = "" %}
{% for post in site.posts %}
{% assign tcats = post.category | join:'|' | append:'|' %}
{% assign rawcats = rawcats | append:tcats %}
{% endfor %}

{% assign rawcats = rawcats | split:'|' | sort %}

{% assign cats = "" %}

{% for cat in rawcats %}
{% if cat != "" %}

{% if cats == "" %}
{% assign cats = cat | split:'|' %}
{% endif %}

{% unless cats contains cat %}
{% assign cats = cats | join:'|' | append:'|' | append:cat | split:'|' %}
{% endunless %}
{% endif %}
{% endfor %}

<div class="row oneandhalf" style="width: 80%; margin: auto;">
    <div class="9u skel-cell-important" style="padding: 0;">
        <ul class="posts">
            {% for post in site.posts %}
                <li class="wrapper blog" >
                    <h2 class="blog title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
                    <h1 class="blog">{{ post.categories }} - {{ page.date | date: "%b %-d, %Y" }} by {{post.author}}</h1>
                        {% if post.image %}
                            <p align="center" style="padding: 0;">
                            <img src="{{post.image}}">
                            </p>
                        {% endif %}
                        {{ post.excerpt }}
                </li>
            {% endfor %}
        </ul>
    </div>
    <div class="3u">
    <!-- Sidebar -->
        <section class="categories">
                <h1 class="blog category-title">Post by category</h1>
                {% for ct in cats %}
                    <h1 class="blog category" style="margin:0;"> {{ ct }} </h1>
                        {% for post in site.posts %}
                            {% if post.category contains ct %}
                            <a class="link-cat" href="{{ post.url }}">{{ post.title }} </a>
                        {% endif %}
                    {% endfor %}
            {% endfor %}
        </section>
    </div>
</div>
