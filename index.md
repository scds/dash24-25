---
layout: home
title: Home
description: DASH Webinars
nav_order: 1
---

{%- assign workshops = site.pages 
    | where_exp: "item", "item.grand_parent == null"
    | where_exp: "item", "item.parent == null"
    | sort: "title" 
-%}

<img src="assets/img/titleSlide.png" alt="Workshop Title Slide" width="100%">

# Welcome to DASH: The Data Analysis Support Hub Webinars

DASH workshops help registrants with data analysis and visualization by providing training for software programs and coding languages including Excel, LaTeX, Python, R, and SPSS.

DASH workshops welcome students, staff, and faculty from any discipline, as well as the public at large. A number of DASH workshops are also geared towards beginners, so even if you’re new to data analysis, we encourage you to sign up and learn!

## 2023-2024 DASH Workshop Topics

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Workshops
</summary>
<ul>
{% for workshop in workshops %}
{% if workshop.title != null and workshop.title != "Home" %}
<li><a href="{{workshop.url | absolute_url}}">{{workshop.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
</div>

## Land Acknowledgment

{% include def/land_ack.md %}
