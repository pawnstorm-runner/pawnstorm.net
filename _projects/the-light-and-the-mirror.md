---
title: The Light and the Mirror
date: 2022-01-06
type: philosophy
status: In Progress
excerpt: My thoughts on how to live a good life.
---
<h1 id="top">The Light and the Mirror</h1>
<ul>
{% for section in site.philosophy %}
  <li><a href="#{{ section.slug }}">{{ section.name }}</a></li>
{% endfor %}
</ul>

---

### Huh?
This is a collection of my thoughts on how to live a good life. I'm borrowing from a lot of traditions here, principally the stoics, and the title comes from Don Quixote, and which I have always interpreted as meaning that our words and actions should be in agreement: we should both project virtue in our words and reflect it in our actions.

As of early 2022, there isn't much in the way of content here, and probably won't be for at least a couple of months. My goal is to have at least on piece of philosophy-ish writing up here by the end of the year (which is a deliberately low target, I'm going for realistic here). I still need to figure out a posting process, but it will probably consist of posting the writing as a regular blog post and copying it here at the same time. No matter what, anything that goes in here will be announced or posted as part of the main blog.

---

{% for section in site.philosophy %}
  <h2 id="{{ section.slug }}">{{ section.name }}</h2>
  <p>{{ section.content | markdownify }}</p>
  <p><a href="#top">back to table of contents</a></p>
  ---
{% endfor %}
