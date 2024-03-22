---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 3em 1em; background: #3B4252; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Atlas]]</span> to get started on your exploration.
</p>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "modified" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.modified | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
