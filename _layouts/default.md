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
            <li><a href="{{ "/" | relative_url }}"><i class="fas fa-home"></i></a></li>
            <li>
                <!-- {% assign current_url = page.url %}
                {% assign parts = current_url | split: '/' %}
                {% assign chapter_part = parts.last | split: '_' %}
                {% assign book_chapter = chapter_part[0] | split: 'c' %}
                {% assign book = book_chapter[0] | replace: 'b', '' %}
                {% assign chapter = book_chapter[1] | plus: 0 %}
                {% assign prev_chapter = chapter | minus: 1 %}
                {% if prev_chapter >= 0 %}
                    {% assign prev_url = "/chapters/b" | append: book | append: "c" | append: prev_chapter | append: "_ARRAYS_INTRO" %}
                    <a href="{{ prev_url | relative_url }}"><i class="fas fa-arrow-circle-left"></i></a>
                {% endif %} -->

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
                            <a href="{{ prev_url | relative_url }}"><i class="fas fa-arrow-circle-left"></i></a>
                        {% else %}
                            <a href="{{ "/books/client_book" | append: book | relative_url }}"><i class="fas fa-book"></i></a>
                        {% endif %}
                    {% elsif chapter == 0 %}
                        <a href="{{ "/books/client_book#" | relative_url }}"><i class="fas fa-book"></i></a>
                    {% endif %}


            </li>
            <li><a href="{{ "/books/client_book" | append: book | relative_url }}"><i class="fas fa-book"></i></a></li>
        </ul>
    </nav>
</div>

<!-- # {{ page.title | markdownify }} -->

{{ content }}

<footer>
Copyright © {{ site.time | date: "%Y" }}
</footer>

