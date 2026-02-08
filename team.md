---
layout: page
# title: Team Members
subtitle: 
# full-width: true
members:
  - name: PI
    list:
      - full: true
        list:
          - name: Prof. Jingcai Guo
            photo_url: /assets/img/members/Jingcai_Guo.png
            web_url: https://jingcaiguo.github.io/

  - name: Postdocs/PhD Students
    list:
      - full: true
        list:
          - name: Dr. Xiaofeng Zou
            period: 2025/12 (Postdoc)
            affiliation: tbd
            photo_url: /assets/img/members/Xiaofeng_Zou.png
            web_url: https://scholar.google.com/citations?user=Yp5z3xwAAAAJ&hl=en
          - name: Mr. Zhijie Rao
            period: 2024/05 (PhD Student)
            photo_url: /assets/img/members/Zhijie_Rao.png
            web_url: https://zjrao.github.io/
          - name: Ms. Miaoge Li
            period: 2024/05 (PhD Student)
            photo_url: /assets/img/members/Miaoge_Li.png
            web_url: https://keepgoingjkg.github.io/about/
          - name: Mr. Yang Chen
            period: 2024/09 (PhD Student)
            photo_url: /assets/img/members/Yang_Chen.png
            web_url: https://cseeyangchen.github.io/
          - name: Mr. Tianqi Wang
            period: 2026/05 (PhD Student)
            photo_url: /assets/img/members/Tianqi_Wang.jpg
            web_url: https://tianqi-wang1.github.io/
          - name: Mr. Xiaorui Jiang
            period: 2026/09 (PhD Student)
            photo_url: /assets/img/members/Xiaorui_Jiang.jpg
            web_url: https://xiaorui-jiang.github.io/
          - name: Mr. Mingfeng Zha
            period: 2026/09 (PhD Student)
            photo_url: /assets/img/members/Mingfeng_Zha.jpg
            web_url: https://winter-flow.github.io/
            
  - name: Visitors
    list:
      - full: true
        list:
          - name: Mr. Yihua Shao
            period: 2025/01 (PhD Student at University of Trento)
            photo_url: /assets/img/members/Yihua_Shao.jpg
            web_url: https://github.com/YihuaJerry

  - name: Alumni
    list:
      - full: false
        list:
          - name: Tianqi Wang
            web_url: https://tianqi-wang1.github.io/
            position_at_lab: Research Assistant
            period: 2024/09-2025/09
            last_stop: Master Student, UCL London
            next_stop: Ph.D. Student (our lab), The Hong Polytechnic University
          - name: Fengxin Li
            web_url: https://fengxinlee.github.io/FengxinLI.github.io/
            position_at_lab: Visiting Ph.D. Student
            period: 2025/02-2025/09
            last_stop: Ph.D. Student, Renmin University of China
            next_stop: Renmin University of China
          - name: Zhijie Rao
            web_url: https://zjrao.github.io/
            position_at_lab: Research Assistant
            period: 2023/09-2024/05
            last_stop: Master Student, Xiamen University
            next_stop: Ph.D. Student (our lab), The Hong Polytechnic University
          - name: Jingming Liang
            web_url: https://mirrorigin.github.io/
            position_at_lab: Research Assistant
            period: 2023/09-2024/03
            last_stop: Master Student, Huazhong University of Science and Technology
            next_stop: Ph.D. Student, University of Iowa
---

<style>
  /* 表格居中样式 */
  .table-container {
    display: flex;
    justify-content: center;
    width: 100vw !important;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw !important;
    margin-right: -50vw !important;
  }
  
  .centered-table {
    width: 70vw !important;
    max-width: 70vw !important;
    margin: 0 auto !important;
    table-layout: fixed !important;
    border-collapse: collapse !important;
  }

  /* 调整头像成员之间的距离 */
  /* .row.justify-content-center {
    margin-left: -200px !important;
    margin-right: -200px !important;
  } */
  
  .row.justify-content-center .col-lg-3,
  .row.justify-content-center .col-md-4,
  .row.justify-content-center .col-sm-6 {
    padding-left: 100px !important;
    padding-right: 100px !important;
    margin-bottom: 40px !important;
  }

  /* 成员名字样式 */
  .member-name {
    font-size: 1.5rem !important; /* 增大字体 */
    font-weight: 600 !important;
    color: #007bff !important; /* 蓝色 */
    margin-bottom: 8px !important;
    line-height: 1.2 !important;
  }

  .member-name a {
    color: #007bff !important; /* 确保链接也是蓝色 */
    text-decoration: none !important;
  }

  .member-name a:hover {
    color: #0056b3 !important; /* 悬停时稍微深一点的蓝色 */
    text-decoration: underline !important;
  }

  /* Period信息样式 */
  .member-period {
    font-size: 1.5rem !important;
    color: #666 !important;
    font-style: italic !important;
    margin-top: 5px !important;
    margin-bottom: 0 !important;
  }
</style>

<div class="team-members-custom" style="margin-top: 30px;">
  {% for member_group in page.members %}
    <div class="member-group-section" style="margin-bottom: 40px;">
      <h2 class="text-center" style="margin-bottom: 20px;">{{ member_group.name }}</h2>
      <hr style="margin-bottom: 30px;">
      {% for item_list_container in member_group.list %}
        {% if item_list_container.full == false %}
          <div class="table-container">
            <table class="table table-borderless centered-table"> 
              <thead>
                <tr>
                  <th style="width: 15%;">Name</th>
                  <th style="width: 15%;">Period</th>
                  <th style="width: 20%;">Position @ Lab</th>
                  <th style="width: 25%;">Last Stop</th>
                  <th style="width: 25%;">Next Stop</th>
                </tr>
              </thead>
              <tbody>
                {% for member in item_list_container.list %}
                  <tr>
                    <td>
                      <strong>
                        {% if member.web_url %}
                          <a href="{{ member.web_url }}" target="_blank" style="color: #212529;">{{ member.name }}</a>
                        {% else %}
                          {{ member.name }}
                        {% endif %}
                      </strong>
                    </td>
                    <td>{{ member.period }}</td>
                    <td>{{ member.position_at_lab}}</td>
                    <td>{{ member.last_stop }}</td>
                    <td>{{ member.next_stop }}</td>
                  </tr>
                {% endfor %}
              </tbody>
            </table>
          </div>
        {% else %}
          <div class="row justify-content-center">
            {% for member in item_list_container.list %}
              <div class="col-lg-3 col-md-4 col-sm-6 text-center" style="margin-bottom: 30px;">
                {% if member.photo_url %}
                  <a href="{{ member.web_url }}" target="_blank">
                    <img src="{{ site.baseurl }}{{ member.photo_url }}" 
                         alt="{{ member.name }}" 
                         style="width: 100px; height: 100px; 
                                object-fit: cover; 
                                border-radius: 17%; 
                                margin-bottom: 15px; 
                                border: 1px solid #f0f0f0;
                                transition: transform 0.3s ease-in-out;"
                         onmouseover="this.style.transform='scale(1.1)'" 
                         onmouseout="this.style.transform='scale(1)'">
                  </a>
                {% else %}
                  <div style="width: 160px; height: 160px; background-color: #f0f0f0; border-radius: 50%; margin: 0 auto 15px; display: flex; align-items: center; justify-content: center; border: 3px solid #e0e0e0;">
                    <span style="font-size: 1.2em; color: #aaa;">No Photo</span>
                  </div>
                {% endif %}
                
                <div class="member-name">
                  {% if member.web_url %}
                    <a href="{{ member.web_url }}" target="_blank">{{ member.name }}</a> 
                  {% else %}
                    {{ member.name }}
                  {% endif %}
                </div>
                
                {% if member.period %}
                  <p class="member-period">{{ member.period }}</p>
                {% endif %}
                
                {% if member.affiliation %}
                  <p style="font-size: 0.9em; color: #666; margin-top: 5px;"><em>{{ member.affiliation }}</em></p>
                {% endif %}
              </div>
            {% endfor %}
          </div>
        {% endif %}
      {% endfor %}
    </div>
  {% endfor %}
</div>

