---
feature_text: |
  ## Korea News
  가장 빠른 실시간 뉴스를 전달하는 korea news 입니다.
feature_image: "https://picsum.photos/1300/400?image=989"
excerpt: "가장 빠른 실시간 뉴스를 전달하는 korea news 입니다."
paginate: true
---

<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <a href="{{ post.url }}">
        <div class="post-box">
          <div class="thumbnail" style="background-image: url('{{ post.feature_image }}');"></div>
          <div class="post-content">
            <h3>{{ post.title }}</h3>
            <p>{{ post.feature_text }}</p>
          </div>
        </div>
      </a>
    </li>
  {% endfor %}
</ul>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="prev">Previous</a>
  {% endif %}
  {% for page in (1..paginator.total_pages) %}
    <a href="{{ paginator.page_path | replace: ':num', page }}" class="page-num {{ page == paginator.page ? 'active' : '' }}">{{ page }}</a>
  {% endfor %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next</a>
  {% endif %}
</div>
