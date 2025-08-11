---
layout: page
title: Lab Photos
subtitle: Memories from our research journey

lab_photos:
  - year: 2025
    list:
    - month: August
      list:
        - event: Invited Talk at RIKEN AIP, Tokyo
          photos:
            - url: /assets/img/lab_photos/riken.jpg
              caption: "@ RIKEN AIP, Tokyo"
            - url: /assets/img/lab_photos/riken2.jpg
              caption: "@ RIKEN AIP, Tokyo"
             - url: /assets/img/lab_photos/riken3.jpg
              caption: "@ RIKEN AIP, Tokyo"
            - url: /assets/img/lab_photos/riken5.jpg
              caption: "@ RIKEN AIP, Tokyo"
            - url: /assets/img/lab_photos/riken6.jpg
              caption: "@ RIKEN AIP, Tokyo"          
      - month: June
        list:
          - event: Research Student Conference
            photos:
              - url: /assets/img/lab_photos/RSC2025-11.jpg
                caption: "Postering 1"
              - url: /assets/img/lab_photos/RSC2025-22.jpg
                caption: "Postering 2"
              - url: /assets/img/lab_photos/dinner1.jpg
                caption: "Enjoying dinner together"
  - year: 2024
    list:
      - month: October
        list:
          - event: ACM Multimedia 2024 Conference
            photos:
              - url: /assets/img/lab_photos/MM24_Logo1.jpg
                caption: "Conference logo"
              - url: /assets/img/lab_photos/MM24_Logo3.jpg
                caption: "City exploration"
              - url: /assets/img/lab_photos/MM24.jpg
                caption: "Conference hall"
              - url: /assets/img/lab_photos/MM24_Logo2.jpg
                caption: "Poster presentation"
              - url: /assets/img/lab_photos/MM24_Logo4.jpg
                caption: "Conference logo"
              - url: /assets/img/lab_photos/MM24_Melbourne1.jpg
                caption: "Melbourne city"
              - url: /assets/img/lab_photos/MM24_Logo5.jpg
                caption: "Conference logo"
              - url: /assets/img/lab_photos/MM24_Conference1.jpg
                caption: "Keynote session"
              - url: /assets/img/lab_photos/MM24_Melbourne2.jpg
                caption: "City exploration"
      - month: August
        list:
          - event: IJCAI 2024 Conference
            photos:
              - url: /assets/img/lab_photos/IJCAI24_Poster.jpg
                caption: "Poster presentation"
              # - url: /assets/img/lab_photos/404-southpark.jpg
              #   caption: "Presentation session"
              # - url: /assets/img/lab_photos/404-southpark.jpg
              #   caption: "Networking event"
      - month: July
        list:
          - event: Ngong Ping Hiking
            photos:
              - url: /assets/img/lab_photos/Ngong_Ping_Group_Photo.jpg
                caption: "Group Photo"
              - url: /assets/img/lab_photos/Ngong_Ping_Seaside1.jpg
                caption: "Seaside view"
              - url: /assets/img/lab_photos/Ngong_Ping_Mountain1.jpg
                caption: "Mountain hiking"
          - event: Victoria Harbour
            photos:
              - url: /assets/img/lab_photos/Victoria_Harbour.jpg
                caption: "Harbour view"
              - url: /assets/img/lab_photos/Victoria_Harbour2.jpg
                caption: "Golden Bauhinia Square"
      
      
---

<style>
  /* 🔧 移除年份标题显示 */
  .year-title {
    display: none;
  }

  /* 🔧 修改：事件标题样式 - 参考news页面风格 */
  .event-header {
    margin-bottom: 25px;
    text-align: left;
    padding-bottom: 15px;
    border-bottom: 1px solid #ecf0f1;
    /* 🔧 新增：flex布局以便年份显示在右侧 */
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }

  .event-title-wrapper {
    display: flex;
    align-items: center;
    gap: 12px;
    flex-wrap: wrap;
    flex: 1;
  }

  .event-title {
    font-size: 1.4rem;
    font-weight: 600;
    color: #2c3e50;
    margin: 0;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  /* 🔧 修改：将红色圆点替换为相机符号 */
  .event-title::before {
    content: '📷';
    font-size: 1.2rem;
    flex-shrink: 0;
  }

  /* 🔧 移除：胶囊形状的月份样式 */
  .event-date {
    display: none;
  }

  /* 🔧 修改：年份月份组合显示样式 - 2024.07格式 */
  .event-date-year {
    color: #999999 !important;
    font-size: 1.8rem !important;
    font-weight: 300 !important;
    text-align: right;
    flex-shrink: 0;
    margin-left: 20px;
    /* 🔧 确保年份在右侧对齐 */
    align-self: flex-start;
    margin-top: -5px; /* 微调位置 */
    line-height: 1.2;
  }

  /* 其他样式保持不变 */
  .photos-filters {
    text-align: center;
    margin-bottom: 30px;
    padding: 15px;
    background-color: #f8f9fa;
    border-radius: 8px;
    max-width: 80vw !important;
    margin-left: auto;
    margin-right: auto;
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
    font-size: 13px;
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

  .lab-photos-container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 20px;
  }

  .year-section {
    margin-bottom: 50px;
  }

  .event-container {
    margin-bottom: 40px;
    background: #f8f9fa;
    border-radius: 12px;
    padding: 25px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
    /* 🔧 新增：固定宽度 */
    max-width: 80vw !important; /* 或你想要的任何宽度 */
    margin-left: auto;
    margin-right: auto;
  }

  .event-photos-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }

  .photo-card {
    background: #fff;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    transition: all 0.3s ease;
    cursor: pointer;
  }

  .photo-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
  }

  .photo-card img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    transition: transform 0.3s ease;
  }

  .photo-card:hover img {
    transform: scale(1.05);
  }

  .photo-caption {
    padding: 15px 20px;
    background: #fff;
  }

  .photo-caption p {
    margin: 0;
    font-size: 0.95rem;
    color: #495057;
    line-height: 1.4;
    text-align: center;
  }

  .modal-overlay {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.9);
    z-index: 1000;
    justify-content: center;
    align-items: center;
  }

  .modal-content {
    position: relative;
    max-width: 90%;
    max-height: 90%;
    text-align: center;
  }

  .modal-image {
    max-width: 100%;
    max-height: 80vh;
    object-fit: contain;
    border-radius: 8px;
  }

  .modal-caption {
    background: rgba(255, 255, 255, 0.95);
    color: #2c3e50;
    padding: 15px;
    margin-top: 15px;
    border-radius: 8px;
    font-size: 1.1rem;
    font-weight: 500;
    max-width: 80vw;
    margin-left: auto;
    margin-right: auto;
  }

  .modal-close {
    position: absolute;
    top: -60px;
    right: 0;
    color: white;
    font-size: 2rem;
    cursor: pointer;
    background: rgba(0, 0, 0, 0.6);
    width: 50px;
    height: 50px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background 0.3s ease;
    z-index: 20;
  }

  .modal-close:hover {
    background: rgba(0, 0, 0, 0.8);
  }

  /* 响应式设计 */
  @media (max-width: 768px) {
    .event-photos-grid {
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
    }
    
    .photo-card img {
      height: 200px;
    }
    
    .lab-photos-container {
      padding: 10px;
    }

    .event-container {
      padding: 15px;
      margin-bottom: 30px;
    }

    .event-title {
      font-size: 1.2rem;
    }

    .filter-btn {
      font-size: 12px;
      padding: 5px 10px;
      margin: 2px 3px;
    }

    .event-title-wrapper {
      gap: 8px;
    }

    /* 🔧 移动端年份月份样式调整 */
    .event-header {
      flex-direction: column;
      align-items: flex-start;
    }

    .event-date-year {
      font-size: 1.2rem !important;
      margin-left: 0;
      margin-top: 10px;
      align-self: flex-end;
    }

    /* 🔧 移动端相机符号调整 */
    .event-title::before {
      font-size: 1rem;
    }
  }

  @media (max-width: 480px) {
    .event-photos-grid {
      grid-template-columns: 1fr;
    }
  }

  /* 加载动画 */
  .photo-card img {
    background: linear-gradient(90deg, #f0f0f0 25%, transparent 37%, #f0f0f0 63%);
    background-size: 400% 100%;
    animation: shimmer 1.5s ease-in-out infinite;
  }

  @keyframes shimmer {
    0% {
      background-position: 100% 50%;
    }
    100% {
      background-position: -100% 50%;
    }
  }

  .empty-state {
    text-align: center;
    padding: 40px;
    color: #7f8c8d;
    font-style: italic;
  }

  .year-section.hidden {
    display: none;
  }
</style>

<!-- 过滤器 -->
<div class="photos-filters">
  <h4 style="margin-bottom: 15px; color: #495057; font-size: 16px;">📸 Filter by Year:</h4>
  <button class="filter-btn active" onclick="filterPhotos('all')" data-filter="all">All Photos</button>
  <button class="filter-btn" onclick="filterPhotos('2025')" data-filter="2025">2025</button>
  <button class="filter-btn" onclick="filterPhotos('2024')" data-filter="2024">2024</button>
</div>

<div class="lab-photos-container">
  {% if page.lab_photos and page.lab_photos.size > 0 %}
    {% for year_data in page.lab_photos %}
      <div class="year-section" data-year="{{ year_data.year }}">
        <h2 class="year-title">{{ year_data.year }}</h2>
        
        {% comment %} 🔧 修改：按事件分组显示所有照片 {% endcomment %}
        {% for month_data in year_data.list %}
          {% if month_data.list and month_data.list.size > 0 %}
            {% for event in month_data.list %}
              <div class="event-container">
                <div class="event-header">
                  <div class="event-title-wrapper">
                    <h3 class="event-title">{{ event.event }}</h3>
                  </div>
                  <div class="event-date-year">
                    {% comment %} 🔧 格式化为 YYYY.MM 格式 {% endcomment %}
                    {% assign month_number = "01" %}
                    {% case month_data.month %}
                      {% when "January" %}{% assign month_number = "01" %}
                      {% when "February" %}{% assign month_number = "02" %}
                      {% when "March" %}{% assign month_number = "03" %}
                      {% when "April" %}{% assign month_number = "04" %}
                      {% when "May" %}{% assign month_number = "05" %}
                      {% when "June" %}{% assign month_number = "06" %}
                      {% when "July" %}{% assign month_number = "07" %}
                      {% when "August" %}{% assign month_number = "08" %}
                      {% when "September" %}{% assign month_number = "09" %}
                      {% when "October" %}{% assign month_number = "10" %}
                      {% when "November" %}{% assign month_number = "11" %}
                      {% when "December" %}{% assign month_number = "12" %}
                    {% endcase %}
                    {{ year_data.year }}.{{ month_number }}
                  </div>
                </div>
                
                <div class="event-photos-grid">
                  {% for photo in event.photos %}
                    <div class="photo-card" onclick="openModal('{{ photo.url | relative_url }}', '{{ photo.caption }}', '{{ event.event }}', '{{ month_data.month }} {{ year_data.year }}')">
                      <img src="{{ photo.url | relative_url }}" alt="{{ event.event }}" loading="lazy">
                      <div class="photo-caption">
                        <p>{{ photo.caption }}</p>
                      </div>
                    </div>
                  {% endfor %}
                </div>
              </div>
            {% endfor %}
          {% endif %}
        {% endfor %}
      </div>
    {% endfor %}
  {% else %}
    <div class="empty-state">
      <h3>No lab photos available yet.</h3>
      <p>Check back later for updates!</p>
    </div>
  {% endif %}
</div>

<!-- 🔧 修改：简单模态框 -->
<div id="photoModal" class="modal-overlay" onclick="closeModal()">
  <div class="modal-content" onclick="event.stopPropagation()">
    <span class="modal-close" onclick="closeModal()">&times;</span>
    <img id="modalImage" class="modal-image" src="" alt="">
    <div id="modalCaption" class="modal-caption"></div>
  </div>
</div>

<script>
  // 过滤照片函数
  function filterPhotos(filterType) {
    const buttons = document.querySelectorAll('.filter-btn');
    buttons.forEach(btn => {
      btn.classList.remove('active');
      if (btn.getAttribute('data-filter') === filterType) {
        btn.classList.add('active');
      }
    });
    
    const yearSections = document.querySelectorAll('.year-section');
    let visibleCount = 0;
    
    yearSections.forEach(section => {
      const year = section.getAttribute('data-year');
      
      let shouldShow = false;
      
      if (filterType === 'all') {
        shouldShow = true;
      } else {
        shouldShow = year === filterType;
      }
      
      if (shouldShow) {
        section.classList.remove('hidden');
        visibleCount++;
      } else {
        section.classList.add('hidden');
      }
    });
    
    console.log(`Filtered photos: ${visibleCount} sections visible for filter "${filterType}"`);
  }

  // 🔧 修改：简单的模态框功能
  function openModal(imageSrc, caption, eventTitle, date) {
    const modal = document.getElementById('photoModal');
    const modalImg = document.getElementById('modalImage');
    const modalCaption = document.getElementById('modalCaption');
    
    modal.style.display = 'flex';
    modalImg.src = imageSrc;
    modalCaption.innerHTML = `<strong>${eventTitle}</strong><br>${caption}<br><small style="color: #7f8c8d;">${date}</small>`;
    
    // 防止页面滚动
    document.body.style.overflow = 'hidden';
  }

  // 关闭模态框
  function closeModal() {
    const modal = document.getElementById('photoModal');
    modal.style.display = 'none';
    
    // 恢复页面滚动
    document.body.style.overflow = 'auto';
  }

  // ESC键关闭模态框
  document.addEventListener('keydown', function(event) {
    if (event.key === 'Escape') {
      closeModal();
    }
  });

  // 图片加载完成后移除加载动画
  document.addEventListener('DOMContentLoaded', function() {
    const images = document.querySelectorAll('.photo-card img');
    images.forEach(img => {
      img.addEventListener('load', function() {
        this.style.animation = 'none';
        this.style.background = 'none';
      });
    });
  });

  // 懒加载优化
  if ('IntersectionObserver' in window) {
    const imageObserver = new IntersectionObserver((entries, observer) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const img = entry.target;
          img.src = img.dataset.src || img.src;
          img.classList.remove('lazy');
          imageObserver.unobserve(img);
        }
      });
    });

    const images = document.querySelectorAll('img[loading="lazy"]');
    images.forEach(img => imageObserver.observe(img));
  }
</script>





