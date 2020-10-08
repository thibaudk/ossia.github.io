---
layout: score-page
title:  "Features"

permalink: /score/features.html
category: "site-score"
---

{% assign rawcats = "" %}
{% for post in site.score_features %}
{% assign tcats = post.tag | join:'|' | append:'|' %}
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

<h1> Important: the documentation below is a work-in-progress. </h1>
            {% if post.visible %}
            {% endif %}
<div>
    {% for ct in cats %}
         <h2 class="feature-title">{{ ct }}</h2>
         <div class="features-list">
        {% for post in site.score_features %}
            {% if post.tag contains ct %}
                <a href="{{post.url}}" class="thumbnail" >
                    <img class="thumbnail-feature" src="{{post.image}}" width="auto"/>
                    <h1 class="blog-title">{{post.title}} </h1>
                    <span class="feature-description">{{post.description}} </span>
                </a>
            {% endif %}
        {% endfor %}
        </div>
        
    {% endfor %}
</div>
