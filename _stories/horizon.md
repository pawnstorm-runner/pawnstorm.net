---
title: Horizon Station
author: Tom Dillon
genre: Science Fiction
wordcount: Series
rank: 1
excerpt: For Ava, Remi, and Vance, life on Habitat Station sucks. But when they discover an abandoned space station drifting in space, their luck just might change. A series of short stories.
---
# {{ page.title }}

In the distant future, humanity has spread across the stars, and now the majority of people live in space stations.  Almost all habitable planets have been converted to agricultural purposes and the promise of liberation through space colonization has been forgotten. But even in a universe where people live like insects in hive-like space stations and trade conglomerates have replaced governments, there is hope.

{% for story in site.horizon %}
  <div class="listTitle singleLine storyTitle"><a href="{{ story.url }}" class="list">{{ story.title }}</a></div>
  <div class="storyGrid">
    <div>{{ story.wordcount | divided_by: 200 }} minute read</div>
    <div class="storyExcerpt">{{ story.excerpt }}</div>
  </div>
{% endfor %}
