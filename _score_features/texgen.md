---
layout: score-feature
title:  "Bytebeat"

permalink: /score/features/texgen.html
category: "site-score"

image: /assets/features/texgen.png
description: "Generative textures"

tag: "Graphics"
visible: true
---

# Example
{% highlight cpp %}
extern "C"
void score_rgba(unsigned char* rgba, int width, int height, int t)
{
  int k = 0;
  for(int j = 0; j < height; j++)
  {
    for(int i = 0; i < width; i++)
    {
      rgba[k++] = 255 * t * k / (width * height);
      rgba[k++] = 255 * t * k / (width * height);
      rgba[k++] = 255 * t * k / (width * height);
      rgba[k++] = 255 * t * k / (width * height);
    }
  }
}
{% endhighlight %}