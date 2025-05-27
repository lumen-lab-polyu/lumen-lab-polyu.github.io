---
layout: page
title: Publications
subtitle:
full-width: true
---

<style>
  /* 调整publications页面的宽度并居中 */
  .container-md {
    max-width: 95% !important;
    margin-left: auto !important;
    margin-right: auto !important;
  }
  
  /* 确保表格居中并占用适当宽度 */
  table {
    width: 60% !important;
    margin-left: auto !important;
    margin-right: auto !important;
    margin-top: 20px;
  }
  
  /* 调整图片列宽度 */
  .pubimg {
    width: 200px !important;
    min-width: 200px;
    text-align: center !important;
  }
  
  /* Tag selector 样式 */
  .tag-selector {
    text-align: center;
    margin-bottom: 30px;
    padding: 15px;  /* 改为与news.md一致 */
    background-color: #f8f9fa;
    border-radius: 8px;  /* 改为与news.md一致 */
    max-width: 80vw;  /* 视口宽度，设置为页面的80% */
    margin-left: auto;  /* 居中显示 */
    margin-right: auto; /* 居中显示 */
  }
  
  .tag-btn {
    display: inline-block;
    margin: 3px 5px;  /* 改为与news.md一致 */
    padding: 6px 12px; /* 改为与news.md一致 */
    background-color: #ffffff;
    border: 1px solid #dee2e6;  /* 改为与news.md一致 */
    border-radius: 15px;  /* 改为与news.md一致 */
    color: #495057;
    text-decoration: none;
    font-size: 13px;  /* 改为与news.md一致 */
    font-weight: 500;
    transition: all 0.2s ease;  /* 改为与news.md一致 */
    cursor: pointer;
    outline: none;
  }
  
  .tag-btn:hover {
    background-color: #e9ecef;
    text-decoration: none;
    color: #495057;
    border-color: #adb5bd;
    transform: translateY(-1px);
  }
  
  .tag-btn.active {
    background-color: #007bff;  /* 改为与news.md一致 */
    color: white;
    border-color: #007bff;  /* 改为与news.md一致 */
    box-shadow: 0 2px 4px rgba(0,123,255,0.3);
  }
  
  /* 修复：使用更强的CSS选择器和!important来确保隐藏效果 */
  table#publications-table tr.publication-row {
    display: table-row !important;
    visibility: visible !important;
    opacity: 1 !important;
    transition: opacity 0.3s ease;
  }
  
  table#publications-table tr.publication-row.filter-hidden {
    display: none !important;
    visibility: hidden !important;
    opacity: 0 !important;
    height: 0 !important;
    overflow: hidden !important;
    margin: 0 !important;
    padding: 0 !important;
    border: none !important;
  }
</style>

<div style="text-align: center; margin-bottom: 20px;">
  You can also find publications on <a href="https://scholar.google.com/citations?user=YjSHPjcAAAAJ&hl=en">Google Scholar</a> which may include some preprints not yet listed here.
</div>

<!-- Tag Selector -->
<div class="tag-selector">
  <h4 style="margin-bottom: 15px; color: #495057; font-size: 16px;">📚 Filter by Research Area:</h4>
  <button class="tag-btn active" onclick="filterPublications('all')" data-tag="all">
    All Publications
  </button>
  {% assign all_tags = "" | split: "" %}
  {% for pub in site.data.pubs %}
    {% if pub.tags %}
      {% for tag in pub.tags %}
        {% unless all_tags contains tag %}
          {% assign all_tags = all_tags | push: tag %}
        {% endunless %}
      {% endfor %}
    {% endif %}
  {% endfor %}
  {% assign sorted_tags = all_tags | sort %}
  {% for tag in sorted_tags %}
    <button class="tag-btn" onclick="filterPublications('{{ tag }}')" data-tag="{{ tag }}">
      {{ tag | replace: "-", " " | replace: "_", " " | capitalize }}
    </button>
  {% endfor %}
</div>

<!-- Publications Count Display -->
<div id="publications-count" style="text-align: center; margin-bottom: 20px; color: #6c757d; font-style: italic;">
  Showing all publications
</div>

<!-- Publications Table -->
<table cellpadding="10" id="publications-table">
    {% for pub in site.data.pubs %}
        <tr class="publication-row" data-tags="{% if pub.tags %}{{ pub.tags | join: ',' }}{% endif %}" data-year="{{ pub.year | default: '2024' }}">
            {% include pub.html %}
        </tr>
    {% endfor %}
</table>

<script>
let currentFilter = 'all';

function filterPublications(selectedTag) {
    console.log('Filtering by tag:', selectedTag);
    
    // 更新当前过滤器
    currentFilter = selectedTag;
    
    // 移除所有按钮的 active 类
    const buttons = document.querySelectorAll('.tag-btn');
    buttons.forEach(btn => {
        btn.classList.remove('active');
        if (btn.getAttribute('data-tag') === selectedTag) {
            btn.classList.add('active');
        }
    });
    
    // 获取所有论文行
    const rows = document.querySelectorAll('#publications-table .publication-row');
    let visibleCount = 0;
    
    console.log('Total rows found:', rows.length);
    
    rows.forEach((row, index) => {
        const rowTags = row.getAttribute('data-tags') || '';
        console.log(`Row ${index + 1} tags:`, rowTags);
        
        let shouldShow = false;
        
        if (selectedTag === 'all') {
            shouldShow = true;
        } else {
            if (rowTags) {
                const tagArray = rowTags.split(',').map(tag => tag.trim().toLowerCase());
                const searchTag = selectedTag.toLowerCase().trim();
                shouldShow = tagArray.includes(searchTag);
                
                console.log(`Row ${index + 1}:`, {
                    tagArray: tagArray,
                    searchTag: searchTag,
                    shouldShow: shouldShow
                });
            }
        }
        
        // 简化显示/隐藏逻辑
        if (shouldShow) {
            row.classList.remove('filter-hidden');
            visibleCount++;
            console.log(`Showing row ${index + 1}`);
        } else {
            row.classList.add('filter-hidden');
            console.log(`Hiding row ${index + 1}`);
        }
    });
    
    console.log('Visible count:', visibleCount);
    
    // 更新计数显示
    updatePublicationsCount(selectedTag, visibleCount);
    
}

function updatePublicationsCount(tag, count) {
    const countDisplay = document.getElementById('publications-count');
    if (tag === 'all') {
        countDisplay.textContent = `Showing all ${count} publications`;
    } else {
        const tagDisplayName = tag.replace(/-/g, ' ').replace(/_/g, ' ').replace(/\b\w/g, l => l.toUpperCase());
        countDisplay.textContent = `Showing ${count} publication${count !== 1 ? 's' : ''} in "${tagDisplayName}"`;
    }
}

// 页面加载时默认显示所有论文
document.addEventListener('DOMContentLoaded', function() {
    console.log('DOM loaded, initializing...');
    setTimeout(() => {
        filterPublications('all');
    }, 100);
});

// 调试函数 - 检查行的显示状态
function debugFilter() {
    const rows = document.querySelectorAll('#publications-table .publication-row');
    console.log('=== Debug Filter Results ===');
    rows.forEach((row, index) => {
        const isHidden = row.classList.contains('filter-hidden');
        const computedStyle = window.getComputedStyle(row);
        console.log(`Row ${index + 1}:`, {
            tags: row.getAttribute('data-tags'),
            hasFilterHidden: isHidden,
            computedDisplay: computedStyle.display,
            computedVisibility: computedStyle.visibility
        });
    });
}

// 将调试函数暴露到全局作用域
window.debugFilter = debugFilter;
</script>
