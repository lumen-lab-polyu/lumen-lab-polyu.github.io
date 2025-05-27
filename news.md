---
layout: page
title: News
subtitle: Latest updates from our lab

news_items:
  - date: "2025-01-15"
    type: "achievement"
    title: "Our paper accepted to ICLR 2025"
    content: "Excited to announce that our work on 'Advanced Neural Network Architectures' has been accepted to ICLR 2025!"
    highlight: true
  - date: "2025-01-10"
    type: "event"
    title: "Lab retreat at Hong Kong"
    content: "Our annual lab retreat was a great success with team building activities and research discussions."
  - date: "2024-12-20"
    type: "award"
    title: "Best Paper Award at NeurIPS 2024"
    content: "Congratulations to our team for winning the Best Paper Award at NeurIPS 2024 for our groundbreaking research."
    highlight: true
  - date: "2024-12-15"
    type: "announcement"
    title: "New PhD students joining"
    content: "We are excited to welcome three new PhD students to our research group. Welcome aboard!"
  - date: "2024-12-01"
    type: "publication"
    title: "Survey paper published in Nature"
    content: "Our comprehensive survey on AI applications has been published in Nature journal."
  - date: "2024-11-25"
    type: "event"
    title: "Guest lecture by Prof. Smith"
    content: "Prof. Smith from MIT delivered an inspiring lecture on the future of artificial intelligence."
---

<style>
  /* 过滤器 */
  .news-filters {
    text-align: center;
    margin-bottom: 30px;
    padding: 15px;
    background-color: #f8f9fa;
    border-radius: 8px;
    max-width: 80vw;  /* 视口宽度，设置为页面的80% */
    margin-left: auto;  /* 添加这一行，居中显示 */
    margin-right: auto; /* 添加这一行，居中显示 */
  }

  .filter-btn {
    display: inline-block;
    margin: 3px 5px;
    padding: 6px 12px;
    background: #fff;
    border: 1px solid #dee2e6;
    border-radius: 15px;
    color: #495057;
    text-decoration: none;
    font-size: 15px;
    font-weight: 500;
    transition: all 0.2s ease;
    cursor: pointer;
  }

  .filter-btn:hover,
  .filter-btn.active {
    background: #007bff;
    color: white;
    border-color: #007bff;
    text-decoration: none;
  }

  /* 新闻列表 - 使用主题默认样式 */
  .news-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .news-item {
    margin-bottom: 1.875rem; /* 使用主题默认的margin */
    padding-bottom: 1.25rem;
    border-bottom: 1px solid #eee;
    transition: opacity 0.3s ease;
  }

  .news-item:last-child {
    border-bottom: none;
  }

  /* 新闻标题行 */
  .news-header {
    display: flex;
    align-items: baseline;
    margin-bottom: 0.625rem; /* 使用主题默认的margin */
    gap: 15px;
  }

  .news-date {
    color: var(--mid-col); /* 使用主题颜色变量 */
    font-size: 18px !important; /* 添加 !important 强制应用 */
    font-weight: 500;
    white-space: nowrap;
    min-width: 120px;
  }

  /* 移除自定义字体大小，使用主题默认的h3样式 */
  .news-title {
    font-size: 18px !important; /* 添加 !important 强制应用 */
    font-weight: 600;
    color: var(--text-col); /* 使用主题颜色变量 */
    margin: 0;
    line-height: 1.3;
    /* 移除了自定义的font-size，让主题的h3样式生效 */
  }

  /* 高亮新闻标题 */
  .news-item.highlight .news-title {
    color: #d63384;
  }

  /* 类型标签 */
  .news-type {
    display: inline-block;
    padding: 2px 8px;
    border-radius: 10px;
    font-size: 0.75rem; /* 使用相对单位 */
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.3px;
    margin-left: 10px;
  }

  .news-type.achievement {
    background: #fff2f2;
    color: #dc3545;
  }

  .news-type.award {
    background: #fff8e1;
    color: #ff8f00;
  }

  .news-type.publication {
    background: #f0f8f0;
    color: #28a745;
  }

  .news-type.event {
    background: #f8f0ff;
    color: #6f42c1;
  }

  .news-type.announcement {
    background: #f8f9fa;
    color: #6c757d;
  }

  /* 新闻内容 - 使用主题默认字体大小 */
  .news-content {
    font-size: 18px !important; /* 添加 !important 强制应用 */
    color: var(--text-col); /* 使用主题颜色变量 */
    font-size: 1rem; /* 使用主题相对字体大小 */
    line-height: 1.5;
    margin-left: 135px; /* 调整以适应稍大的日期字体 */
    margin-top: 0.5rem;
  }

  /* 响应式设计 */
  @media (max-width: 768px) {
    .news-header {
      flex-direction: column;
      align-items: flex-start;
      gap: 5px;
    }

    .news-content {
      margin-left: 0;
      margin-top: 0.5rem;
    }

    .news-date {
      min-width: auto;
    }

    .filter-btn {
      font-size: 12px;
      padding: 5px 10px;
      margin: 2px 3px;
    }
  }

  /* 空状态 */
  .empty-state {
    text-align: center;
    padding: 40px 20px;
    color: var(--mid-col); /* 使用主题颜色变量 */
    font-style: italic;
  }

  /* 隐藏状态 */
  .news-item.hidden {
    display: none;
  }
</style>

<!-- 过滤器 -->
<div class="news-filters">
  <h4 style="margin-bottom: 15px; color: #495057; font-size: 16px;">📰 Filter by Category:</h4>
  <button class="filter-btn active" onclick="filterNews('all')" data-filter="all">All</button>
  <button class="filter-btn" onclick="filterNews('achievement')" data-filter="achievement">Achievements</button>
  <button class="filter-btn" onclick="filterNews('award')" data-filter="award">Awards</button>
  <button class="filter-btn" onclick="filterNews('publication')" data-filter="publication">Publications</button>
  <button class="filter-btn" onclick="filterNews('event')" data-filter="event">Events</button>
  <button class="filter-btn" onclick="filterNews('announcement')" data-filter="announcement">Announcements</button>
</div>

<!-- 新闻列表 -->
<div class="news-list">
  {% if page.news_items and page.news_items.size > 0 %}
    {% assign sorted_news = page.news_items | sort: 'date' | reverse %}
    {% for news in sorted_news %}
      <div class="news-item{% if news.highlight %} highlight{% endif %}" data-type="{{ news.type | default: 'announcement' }}">
        <div class="news-header">
          <span class="news-date">{{ news.date | date: "%m/%d/%Y" }}</span>
          <h3 class="news-title">
            {{ news.title }}
            <span class="news-type {{ news.type | default: 'announcement' }}">{{ news.type | default: 'announcement' }}</span>
          </h3>
        </div>
        <div class="news-content">
          {{ news.content }}
        </div>
      </div>
    {% endfor %}
  {% else %}
    <div class="empty-state">
      No news available. Check back later for updates!
    </div>
  {% endif %}
</div>

<script>
  function filterNews(filterType) {
    // 更新按钮状态
    const buttons = document.querySelectorAll('.filter-btn');
    buttons.forEach(btn => {
      btn.classList.remove('active');
      if (btn.getAttribute('data-filter') === filterType) {
        btn.classList.add('active');
      }
    });
    
    // 过滤新闻项目
    const newsItems = document.querySelectorAll('.news-item');
    newsItems.forEach(item => {
      const itemType = item.getAttribute('data-type');
      if (filterType === 'all' || itemType === filterType) {
        item.classList.remove('hidden');
      } else {
        item.classList.add('hidden');
      }
    });
  }
</script>