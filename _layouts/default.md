---
layout: none
---

<head>
  <link rel="stylesheet" href="{{ "../styles/styles.css" | relative_url }}">
</head>

# {{ page.title }}

{% include toc.md %}

{{ content }}

<footer>
Copyright © {{ site.time | date: "%Y" }}
</footer>

