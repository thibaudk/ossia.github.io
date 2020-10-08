---
layout: libossia-page
title:  "Features"

permalink: /site-libossia/features.html
category: "site-libossia"
---



{% assign rawcats = "" %}
{% for post in site.libossia_features %}
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
    

<div>
    {% for ct in cats %}
         <h2 class="feature-title">{{ ct }}</h2>
         <div class="features-list">
        {% for post in site.libossia_features %}
                <a href="{{post.url}}" class="thumbnail" >
                    <img class="thumbnail-feature" src="/assets/blank.png" alt="" data-echo="{{post.image}}"  width="auto"/>
                    <h1 class="blog-title">{{post.title}} </h1>
                    <span class="feature-description">{{post.description}} </span>
                </a>
        {% endfor %}
        </div>
        
    {% endfor %}
</div>

{% include lazyload.html %}
