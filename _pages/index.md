---
layout: page
title: Home
id: home
permalink: /
---

<div class="topnav">
  <a class="active" href="#home">Home</a>
  <a href="#about">About</a>
  <a href="#contact">Contact</a>
  <input type="text" placeholder="Search..">
</div>

# Welcome! 🌱

This is a repository for all the open notes for the D&D world setting, Materria. This is meant to be used by players to learn more about the world that they play in and act as a wiki inspired database.

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
