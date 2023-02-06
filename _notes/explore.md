---
title: Explore Notes
---

This website is organized as a [[Digital Garden]] -- an organic collection of notes that link to each other.

## Recently updated notes

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 10 %}
    <li>
      {{ note.last_modified_at | date: "%b %e, %Y" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

## Notes Graph

This is a graph of all of the notes on the site, and how they connect to each other. You can highlight notes to see what they are connected to.

{% include notes_graph.html %}