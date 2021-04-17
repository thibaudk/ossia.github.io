---
layout: score-page
title:  "Features"

permalink: /score/features.html
category: "site-score"
---
{% assign cats = "Structure|Audio|Controls|Graphics|Interoperability|Presentation|Scripting|Software model" | split: '|' %}

<h1> Important: the documentation below is a work-in-progress. </h1>
<div>
    {% for ct in cats %}
         <h2 class="feature-title">{{ ct }}</h2>
         <div class="features-list">
        {% for post in site.score_features %}
            {% if post.tag contains ct %}
            {% if post.visible %}
                <a href="https://ossia.io/score-docs/{{post.doclink}}" class="thumbnail" >
                    <img class="thumbnail-feature" src="/assets/blank.png" alt="" data-echo="{{post.image}}"  width="auto"/>
                    <h1 class="blog-title">{{post.title}} </h1>
                    <span class="feature-description">{{post.description}} </span>
                </a>
            {% endif %}
            {% endif %}
        {% endfor %}
        </div>
    {% endfor %}
</div>

{% include lazyload.html %}