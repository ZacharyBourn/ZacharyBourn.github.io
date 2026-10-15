---
layout: default
title: Recommended Reading
permalink: /reading/
---
<div class="page-head"><div class="eyebrow">The reading room</div><h1>Recommended Reading</h1><p>Books that inform historical understanding, from major works of scholarship to firsthand accounts.</p></div>
<p class="reading-note">This is a starter list and can be edited at any time. The notes describe each book; add your personal assessments as you develop the collection.</p>
<div class="book-list">
{% for book in site.data.books %}
<article class="book-entry"><div class="book-symbol" aria-hidden="true">{{ forloop.index | prepend: '0' | slice: -2, 2 }}</div><div><span class="eyebrow">{{ book.subject }}</span><h2>{{ book.title }}</h2><p class="book-author">{{ book.author }}</p><p>{{ book.note }}</p></div></article>
{% endfor %}
</div>
