---
layout: page
title: Projects
permalink: /projects/
nav: true
nav_order: 3
---

## Work-related (sanitized)

{% assign work = site.projects | where: "group", "work" | sort: "importance" %}
{% include projects.liquid projects=work %}

## Personal

{% assign personal = site.projects | where: "group", "personal" | sort: "importance" %}
{% include projects.liquid projects=personal %}

## Academic / Coursework

{% assign acad = site.projects | where: "group", "academic" | sort: "importance" %}
{% include projects.liquid projects=acad %}
