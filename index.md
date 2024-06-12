---
layout: default
title: Korea News
feature_text: |
  ## Korea News
feature_image: "https://picsum.photos/1300/400?image=989"
excerpt: "가장 빠른 실시간 뉴스를 전달하는 korea news 입니다."
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span>{{ post.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>