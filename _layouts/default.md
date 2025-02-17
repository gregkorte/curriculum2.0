---
layout: none
---

<head>
  <link rel="stylesheet" href="{{ "/styles/styles.css" | relative_url }}">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>

<div class="header">
    <img src="{{ "/assets/nss.png" | relative_url }}" alt="Nashville Software School Logo">
    <nav class="nav-right">
        <ul>
            {% if page.url != "/" %}
                <li><a href="{{ "/" | relative_url }}"><i class="fas fa-home"></i></a></li>
            {% endif %}

            {% assign prev_chapter = chapter | minus: 1 %}
            {% if prev_chapter >= 0 %}
                {% assign prev_url = "" %}
                {% for page in site.pages %}
                    {% assign page_parts = page.url | split: '/' %}
                    {% assign page_chapter_part = page_parts.last | split: '_' %}
                    {% assign page_book_chapter = page_chapter_part[0] | split: 'c' %}
                    {% assign page_book = page_book_chapter[0] | replace: 'b', '' %}
                    {% assign page_chapter = page_book_chapter[1] | plus: 0 %}

                    {% if page_book == book and page_chapter == prev_chapter %}
                        {% assign prev_url = page.url %}
                        {% break %}
                    {% endif %}
                {% endfor %}

                {% if prev_url != "" %}
                    <li><a href="{{ prev_url | relative_url }}"><i class="fas fa-arrow-circle-left"></i></a></li>
                {% endif %}
            {% endif %}

            {% if book and page.url != "/" %}
                <li><a href="{{ "/books/client_book" | append: book | relative_url }}"><i class="fas fa-book"></i></a></li>
            {% endif %}
        </ul>
    </nav>

</div>

<!-- # {{ page.title | markdownify }} -->

{{ content }}

<footer>
Copyright © {{ site.time | date: "%Y" }}
</footer>

