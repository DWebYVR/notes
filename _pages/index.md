---
layout: page
title: Home
id: home
permalink: /
---

# DWeb Vancouver 🌱

## Next Event

[[Feb 2023 Flash Talks & Tea]] <a
  href="https://lu.ma/event/evt-BwFDxi3MEnabDpE"
  class="luma-checkout--button"
  data-luma-action="checkout"
  data-luma-event-id="evt-BwFDxi3MEnabDpE">Register for Event</a>

<script id="luma-checkout" src="https://embed.lu.ma/checkout-button.js"></script>

Visit the [Calendar](../notes/calendar/){:.internal-link} to browse all upcoming events, and submit your own to share!

## Recently updated notes

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
