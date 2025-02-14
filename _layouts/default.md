---
layout: none
---

<head>
  <link rel="stylesheet" href="{{ "/styles/style" | relative_url }}">
</head>

<div class="header">
    <img src="{{ "/assets/nss.png" | relative_url }}" alt="Nashville Software School Logo">
</div>

<!-- # {{ page.title | markdownify }} -->

{{ content }}

<footer>
Copyright © {{ site.time | date: "%Y" }}
</footer>

