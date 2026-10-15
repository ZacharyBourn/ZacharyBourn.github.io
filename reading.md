---
layout: default
title: Recommended Reading
permalink: /reading/
---
<div class="page-head"><div class="eyebrow">The reading room</div><h1>Recommended Reading</h1><p>An independently curated shelf of American history, biography, firsthand accounts, and historical interpretation.</p></div>
<p class="reading-note">Titles below are initial examples. Individual notes can be revised into personal recommendations as the collection develops.</p>
<div class="book-list">
{% assign ordered_books = site.data.books | sort: 'order' %}
{% for book in ordered_books %}
<article class="book-entry">
  <div class="book-cover">
    {% if book.cover and book.cover != '' %}
      {% assign cover_prefix = book.cover | slice: 0, 4 %}
      {% if cover_prefix == 'http' %}
      <img src="{{ book.cover }}" alt="Cover of {{ book.title | escape }}" loading="lazy">
      {% else %}
      <img src="{{ book.cover | relative_url }}" alt="Cover of {{ book.title | escape }}" loading="lazy">
      {% endif %}
    {% elsif book.isbn and book.isbn != '' %}
      <img src="https://covers.openlibrary.org/b/isbn/{{ book.isbn }}-L.jpg?default=false" alt="Cover of {{ book.title | escape }}" loading="lazy" onerror="this.style.display='none';this.nextElementSibling.style.display='flex';">
      <span class="book-cover-fallback" style="display:none;">Cover unavailable</span>
    {% else %}
      <span class="book-cover-fallback">Cover forthcoming</span>
    {% endif %}
  </div>
  <div class="book-details">
    <span class="eyebrow">{{ book.subject | escape }}</span>
    <h2>{{ book.title | escape }}</h2>
    <p class="book-author">By {{ book.author | escape }}</p>
    {% if book.note and book.note != '' %}<p class="book-description">{{ book.note | escape }}</p>{% endif %}
  </div>
</article>
{% endfor %}
{% if ordered_books.size == 0 %}<div class="empty-state">The reading list is being prepared.</div>{% endif %}
</div>