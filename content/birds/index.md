---
title: "See Birds"
# 注意：这里删掉了 type: landing，回归普通页面模式
---

<style>
  .bird-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 15px;
    padding: 20px 0;
  }
  .bird-item {
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    background: #f8f8f8;
  }
  .bird-item img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    display: block;
    transition: transform 0.3s ease;
  }
  .bird-item img:hover {
    transform: scale(1.05);
  }
</style>

<div class="bird-gallery">
  {{ range .Resources.Match "*.jpg" }}
    <div class="bird-item">
      <a href="{{ .RelPermalink }}" target="_blank">
        <img src="{{ .RelPermalink }}" alt="Bird photo">
      </a>
    </div>
  {{ end }}
</div>
