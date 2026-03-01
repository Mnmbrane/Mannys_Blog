---
layout: page
title: Manny's Blog
---

This blog documents my hands-on project work from start to finish, including planning, implementation, issues, fixes, and lessons learned.

The goal is to make each post practical and useful so others can follow the process, reuse what works, and avoid common mistakes.

## What You'll Find Here

- Project updates and build logs
- Technical decisions and tradeoffs
- Problems encountered and how they were solved
- Real results and next steps

## Latest Posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}
