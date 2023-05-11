---
layout: page
title: Home
id: home
permalink: /
---

<!-- Load an icon library -->
<link rel="stylesheet" href="https://movetoroll-materria.netlify.app/">

<div class="navbar">
  <a class="active" href="#"><i class="fa fa-fw fa-home"></i> Home</a>
  <a href="#"><i class="fa fa-fw fa-search"></i> Search</a>
  <a href="#"><i class="fa fa-fw fa-envelope"></i> Contact</a>
  <a href="#"><i class="fa fa-fw fa-user"></i> Login</a>
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
