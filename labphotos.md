---
layout: page
title: Lab Photos
subtitle: Memories from our research journey

lab_photos:
  - year: 2025
    list:
      - month: March
        list:
          - event: New PhD admits welcome dinner with Geometry, Vision, and Learning Lab
            photo_url: /assets/img/lab_photos/404-southpark.jpg
      - month: February
        list:
          - event: Post-RSS deadline lunch with lead authors
            photo_url: /assets/img/lab_photos/404-southpark.jpg
  - year: 2024
    list:
      - month: September
        list:
          - event: Welcome Ph.D. students
            photo_url: /assets/img/lab_photos/404-southpark.jpg
      - month: August
        list:
          - event: Unitree G1 demo
            photo_url: /assets/img/lab_photos/404-southpark.jpg
          - event: Unitree Go2 demo
            photo_url: /assets/img/lab_photos/404-southpark.jpg
          - event: Detroit Pizza Depot
            photo_url: /assets/img/lab_photos/404-southpark.jpg
          - event: Happy birthday to Daniel!🎂
            photo_url: /assets/img/lab_photos/404-southpark.jpg
---

<style>
  /* 过滤器样式 - 与news.md保持一致 */
  .photos-filters {
    text-align: center;
    margin-bottom: 30px;
    padding: 15px;
    background-color: #f8f9fa;
    border-radius: 8px;
    max-width: 80vw;
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

  /* 页面容器样式 */
  .lab-photos-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }

  /* 年份标题样式 */
  .year-section {
    margin-bottom: 40px;
  }

  .year-title {
    font-size: 2.5rem;
    font-weight: bold;
    color: #2c3e50;
    margin-bottom: 30px;
    text-align: center;
    border-bottom: 3px solid #3498db;
    padding-bottom: 10px;
  }

  /* 月份标题样式 */
  .month-section {
    margin-bottom: 30px;
  }

  .month-title {
    font-size: 1.8rem;
    font-weight: 600;
    color: #34495e;
    margin-bottom: 20px;
    border-left: 4px solid #e74c3c;
    padding-left: 15px;
  }

  /* 照片网格布局 */
  .photos-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 25px;
    margin-bottom: 25px;
  }

  /* 照片卡片样式 */
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

  .photo-caption h4 {
    margin: 0;
    font-size: 1.1rem;
    font-weight: 600;
    color: #2c3e50;
    line-height: 1.4;
  }

  .photo-date {
    font-size: 0.9rem;
    color: #7f8c8d;
    margin-top: 5px;
  }

  /* 模态框样式 */
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
    background: rgba(255, 255, 255, 0.9);
    color: #2c3e50;
    padding: 15px;
    margin-top: 10px;
    border-radius: 8px;
    font-size: 1.1rem;
    font-weight: 500;
  }

  .modal-close {
    position: absolute;
    top: -40px;
    right: 0;
    color: white;
    font-size: 2rem;
    cursor: pointer;
    background: rgba(0, 0, 0, 0.5);
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background 0.3s ease;
  }

  .modal-close:hover {
    background: rgba(0, 0, 0, 0.8);
  }

  /* 响应式设计 */
  @media (max-width: 768px) {
    .year-title {
      font-size: 2rem;
    }
    
    .month-title {
      font-size: 1.5rem;
    }
    
    .photos-grid {
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 15px;
    }
    
    .photo-card img {
      height: 200px;
    }
    
    .lab-photos-container {
      padding: 10px;
    }

    .filter-btn {
      font-size: 12px;
      padding: 5px 10px;
      margin: 2px 3px;
    }
  }

  @media (max-width: 480px) {
    .photos-grid {
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

  /* 空状态样式 */
  .empty-state {
    text-align: center;
    padding: 40px;
    color: #7f8c8d;
    font-style: italic;
  }

  /* 隐藏状态 */
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
        
        {% for month_data in year_data.list %}
          <div class="month-section">
            <h3 class="month-title">{{ month_data.month }}</h3>
            
            {% if month_data.list and month_data.list.size > 0 %}
              <div class="photos-grid">
                {% for photo in month_data.list %}
                  <div class="photo-card" onclick="openModal('{{ photo.photo_url }}', '{{ photo.event }}', '{{ month_data.month }} {{ year_data.year }}')">
                    <img src="{{ photo.photo_url | relative_url }}" alt="{{ photo.event }}" loading="lazy">
                    <div class="photo-caption">
                      <h4>{{ photo.event }}</h4>
                      <div class="photo-date">{{ month_data.month }} {{ year_data.year }}</div>
                    </div>
                  </div>
                {% endfor %}
              </div>
            {% else %}
              <div class="empty-state">
                <p>No photos available for this month.</p>
              </div>
            {% endif %}
          </div>
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

<!-- 模态框 -->
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
    // 更新按钮状态
    const buttons = document.querySelectorAll('.filter-btn');
    buttons.forEach(btn => {
      btn.classList.remove('active');
      if (btn.getAttribute('data-filter') === filterType) {
        btn.classList.add('active');
      }
    });
    
    // 过滤年份区块
    const yearSections = document.querySelectorAll('.year-section');
    let visibleCount = 0;
    
    yearSections.forEach(section => {
      const year = section.getAttribute('data-year');
      
      let shouldShow = false;
      
      if (filterType === 'all') {
        shouldShow = true;
      } else {
        // 按年份过滤
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

  // 打开模态框
  function openModal(imageSrc, caption, date) {
    const modal = document.getElementById('photoModal');
    const modalImg = document.getElementById('modalImage');
    const modalCaption = document.getElementById('modalCaption');
    
    modal.style.display = 'flex';
    modalImg.src = imageSrc;
    modalCaption.innerHTML = `<strong>${caption}</strong><br><small>${date}</small>`;
    
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





