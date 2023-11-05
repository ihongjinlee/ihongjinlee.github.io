---
title: GitHub Blog 한 번에 끝내기 (6) 홈에 게시물 모두 보이게 하기
date: 2023-11-05 15:00:00 +09:00
categories: [github]
tags: [github, blog]
---

## \_layouts/home.html 수정

`for post in posts` ➡️ `for post in site.posts`

{% raw %}

```html
<div id="post-list" class="flex-grow-1 px-xl-1">
  {% for post in site.posts %}
  <article class="card-wrapper card">...</article>
  {% endfor %}
</div>
```

{% endraw %}
