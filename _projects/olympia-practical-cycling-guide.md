---
title: Olympia Practical Cycling Guide
date: 2020-08-18
type: community resource
status: In Progress
excerpt: Some good routes for getting around Olympia, Lacey, and Tumwater by bicycle.
---
<h1 id="top">Olympia Practical Cycling Guide</h1>
<ul>
{% for route in site.bike_routes %}
  <li><a href="#{{ route.slug }}">{{ route.name }}</a></li>
{% endfor %}
</ul>

---

### About this guide...
*This is an incomplete first draft. As of this writing (8/20/20) the routes are incomplete and inconsistent, and I'm still figuring out the format.* <br /><br />
**What is this?** This is a guide for how to get around the Olympia-Lacey-Tumwater area by bicycle.<br />
**Who is it for?** People who ride bicycles. In particular, I wanted to write a guide that would help people in the area who are new to cycling and for whom the official bicycle map might not be very helpful (because although it tells you where you *can* cycle, it doesn't tell you which routes are *good*). <br />
**How did I pick the routes?** Mostly, I went by routes that I have figured out on my own. I do have some preferences, though:
* I would rather ride on a quiet neighborhood street *without* a bike lane than on a busy street *with* a bike lane (and prefer a protected bike lane or trail over both), so a lot of routes will be going through neighborhoods.
* Decades of riding have instilled a dislike of hills, so I chose easier grades whenever possible. When there is a harder, but significantly more direct route, I have tried to list it in the Alternate Routes section of the given route.
* I like riding in the shade, so I'm willing to go a bit out of my way for tree cover.
* I tried to avoid busy streets as much as possible. Although when I'm on my own, I have a pretty high tolerance for risk, but when I ride with my kid, much less so. I tried to include routes that I would be comfortable towing a kid in a trailer on.

---

## To Do
This is an incomplete first draft, so there is a ton of stuff that I need to do:
* Finalize termini.
* Write up routes for the remainder of the connections.
    * Downtown to Eastside
    * Downtown to Tumwater
    * Eastside to Westside?
    * Eastside to Lacey?
    * Lacey to Tumwater
    * Lacey to Hawks Prairie
* Ride all of the routes to make sure that I got them right.
* Work on improved map images.
* Create and link to proper routes on a real mapping site.
* Add a big map to the beginning of the page once the basic routes are all done.

---

### Locations

* **Downtown Olympia** Olympia Timberland Library
* **Westside Olympia** mall?
* **Eastside Olympia** San Francisco Bakery/Roosevelt Elementary?
* **Lacey** Target
* **Tumwater** Department of Health / WA State Offices
* **Hawks Prairie** LA Fitness compound?

---

# The Routes

{% for route in site.bike_routes %}
  <h2 id="{{ route.slug }}">{{ route.name }}</h2>
  <picture>
    <img src="/assets/{{ route.slug }}.png" alt="route map" style="max-width: 100%;">
  </picture>
  **Start:** {{ route.start }}
  **End:** {{ route.end }} <br />
  **Distance:** {{ route.distance }}
  **Elevation Gain:** {{ route.elevation-gain }}
  <p>{{ route.content | markdownify }}</p>
  <p><i>Last updated: {{ route.last-updated }}</i></p>
  <p><a href="#top">back to route list</a></p>
  ---
{% endfor %}
