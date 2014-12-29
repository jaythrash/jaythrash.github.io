---
layout: page
title: "Talks"
description: "Presentations I've given."
sharing: true
footer: true
category: talks
permalink: talks/
---

I'm always looking for opportunities and events where I can share what I've learned with fellow app designers and developers. The venues were I've been honored to present include: [360iDev](http://360idev.com), [CocoaConf](http://cocoaconf.com), and my [local CocoaHeads chapter](http://www.meetup.com/nscoderrtp/).

If you would like me to speak at your event, please contact via email – you can reach me at *jay at jaythrash.com*, or [@jaythrash on twitter](http://twitter.com/jaythrash).

<div id="blog-archives" class="category">
{% for post in site.talks reversed %}
    {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% unless year == this_year %}
        {% assign year = this_year %}
        <h2>{{ year }}</h2>
    {% endunless %}
    <article>
      <h3><a href="{{ root_url }}{{ post.url }}">{{ post.title }}</a></h3>
      <h5 class="meta-post"><time datetime="{{date format='YYYY-MM-DD'}}">{{ post.date | date: "%b %-d %Y" }}</time></h5>
    </article>
{% endfor %}
</div>
