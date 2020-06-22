---
layout: score-page
title:  "Features"

permalink: /score/features.html
category: "site-score"
---


<div class="recent-post-view">
    {% for post in site.score_features %}
        <a href="{{post.url}}" class="thumbnail" >
            <img class="thumbnail-feature" src="{{post.image}}" width="auto"/>
            <h1 class="blog-title">{{post.title}} </h1>
            <span class="feature-description">{{post.description}} </span>
        </a>
    {% endfor %}
</div>
