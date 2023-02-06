---
title: Explore Notes
---

This website is organized as a [[Digital Garden]] -- an organic collection of notes that link to each other.

## Recently updated notes

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

## Notes Graph

{% include notes_graph.html %}