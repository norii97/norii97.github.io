---
title: "Pick me"
layout: archive
permalink: /categories/Pick me
author_profile: true
sidebar_main: true
---


{% assign posts = site.categories['Pick me'] %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}