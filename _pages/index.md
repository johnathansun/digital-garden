---
layout: page
title: Home
id: home
permalink: /
---

# Hello!

These are a collection of notes and thoughts on a small corner of the web.

Please feel free to take a look around. Some notes are more polished than others, but hopefully they're useful or interesting in some capacity. You can find an interactive graph of notes <a class="internal-link" href="{{ site.baseurl }}/graph">here</a>.

Do let me know if you have any thoughts at [me@johnathan.cc](mailto:me@johnathan.cc).

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  I'm a student at Harvard studying applied mathematics. I'm interested in macroeconomic policy, quantitative techniques in the social sciences, and advances in AI/ML.
</p>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
