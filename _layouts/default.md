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

            {% assign current_url = page.url %}
            {% assign parts = current_url | split: '/' %}
            {% assign chapter_part = parts.last | split: '_' %}
            {% assign book_chapter_section = chapter_part[0] | split: 'c' %}
            {% assign book = book_chapter_section[0] | replace: 'b', '' %}
            {% assign chapter_section = book_chapter_section[1] | split: 's' %}
            {% assign chapter = chapter_section[0] | plus: 0 %}
            {% assign section = chapter_section[1] | plus: 0 %}

            {% assign prev_section = section | minus: 1 %}
            {% assign prev_chapter = chapter | minus: 1 %}
            {% assign prev_url = "" %}

            {% for page in site.pages %}
                {% assign page_parts = page.url | split: '/' %}
                {% assign page_chapter_part = page_parts.last | split: '_' %}
                {% assign page_book_chapter_section = page_chapter_part[0] | split: 'c' %}
                {% assign page_book = page_book_chapter_section[0] | replace: 'b', '' %}
                {% assign page_chapter_section = page_book_chapter_section[1] | split: 's' %}
                {% assign page_chapter = page_chapter_section[0] | plus: 0 %}
                {% assign page_section = page_chapter_section[1] | plus: 0 %}

                {% if page_book == book %}
                    {% if page_chapter == chapter and page_section == prev_section %}
                        {% assign prev_url = page.url %}
                        {% break %}
                    {% elsif prev_section < 1 and page_chapter == prev_chapter %}
                        {% assign prev_url = page.url %}
                    {% endif %}
                {% endif %}
            {% endfor %}

            {% if prev_url != "" %}
                <li><a href="{{ prev_url | relative_url }}"><i class="fas fa-arrow-circle-left"></i></a></li>
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

