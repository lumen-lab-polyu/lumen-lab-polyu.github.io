---
layout: page
# title: Team Members
subtitle: 
# full-width: true
members:
  - name: Principal Investigator
    list:
      - full: true
        list:
          - name: Jingcai Guo
            photo_url: /assets/img/members/Jingcai_Guo.png
            web_url: https://jingcaiguo.github.io/

  - name: Ph.D. Students
    list:
      - full: true
        list:
          - name: Zhijie Rao
            photo_url: /assets/img/members/Zhijie_Rao.png
            web_url: https://zjrao.github.io/
          - name: Miaoge Li
            photo_url: /assets/img/members/Miaoge_Li.png
            web_url: https://keepgoingjkg.github.io/about/
          - name: Yang Chen
            photo_url: /assets/img/members/Yang_Chen.png
            web_url: https://cseeyangchen.github.io/

  - name: Visiting Ph.D. Students
    list:
      - full: true
        list:
          - name: Fengxin Li
            photo_url: /assets/img/members/Fengxin_Li.png
            web_url: https://fengxinlee.github.io/FengxinLI.github.io/

  - name: Alumni
    list:
      - name: Research Assistant
        full: false
        list:
          - name: Jingming Liang
            web_url: https://mirrorigin.github.io/
            period: 2023/09-2024/03
            last_stop: Master, Huazhong University of Science and Technology
            next_stop: Ph.D. Student, University of Iowa
---

<div class="team-members-custom" style="margin-top: 30px;">
  {% for member_group in page.members %}
    <div class="member-group-section" style="margin-bottom: 40px;">
      <h2 class="text-center" style="margin-bottom: 20px;">{{ member_group.name }}</h2>
      <hr style="margin-bottom: 30px;">
      {% for item_list_container in member_group.list %}
        {% if item_list_container.full == false %}
          {% if item_list_container.name %}
            <h3 class="text-center" style="margin-top: 20px; margin-bottom: 15px;">{{ item_list_container.name }}</h3>
          {% endif %}
          <div class="row justify-content-center">
            <div class="col-md-10 col-lg-10">
              <table class="table table-borderless"> 
                <thead>
                  <tr>
                    <th style="width: 20%;">Name</th>
                    <th style="width: 20%;">Period</th>
                    <th style="width: 30%;">Last Stop</th>
                    <th style="width: 30%;">Next Stop</th>
                  </tr>
                </thead>
                <tbody>
                  {% for member in item_list_container.list %}
                    <tr>
                      <td style="vertical-align: middle;">
                        <strong>
                          {% if member.web_url %}
                            <a href="{{ member.web_url }}" target="_blank" style="color: #212529;">{{ member.name }}</a>
                          {% else %}
                            {{ member.name }}
                          {% endif %}
                        </strong>
                      </td>
                      <td style="vertical-align: middle;">{{ member.period }}</td>
                      <td style="vertical-align: middle;">{{ member.last_stop }}</td>
                      <td style="vertical-align: middle;">{{ member.next_stop }}</td>
                    </tr>
                  {% endfor %}
                </tbody>
              </table>
            </div>
          </div>
        {% else %}
          <div class="row justify-content-center">
            {% for member in item_list_container.list %}
              <div class="col-lg-3 col-md-4 col-sm-6 text-center" style="margin-bottom: 30px;">
                {% if member.photo_url %}
                  <a href="{{ member.web_url }}" target="_blank">
                    <img src="{{ site.baseurl }}{{ member.photo_url }}" 
                         alt="{{ member.name }}" 
                         style="width: 160px; height: 160px; 
                                object-fit: cover; 
                                border-radius: 50%; 
                                margin-bottom: 15px; 
                                border: 3px solid #f0f0f0;
                                transition: transform 0.3s ease-in-out;"
                         onmouseover="this.style.transform='scale(1.1)'" 
                         onmouseout="this.style.transform='scale(1)'">
                  </a>
                {% else %}
                  <div style="width: 160px; height: 160px; background-color: #f0f0f0; border-radius: 50%; margin: 0 auto 15px; display: flex; align-items: center; justify-content: center; border: 3px solid #e0e0e0;">
                    <span style="font-size: 1.2em; color: #aaa;">No Photo</span>
                  </div>
                {% endif %}
                <h5 style="margin-bottom: 5px;">
                  {% if member.web_url %}
                    <a href="{{ member.web_url }}" target="_blank" style="color: #212529;">{{ member.name }}</a> 
                  {% else %}
                    {{ member.name }}
                  {% endif %}
                </h5>
                {% if member.affiliation %}<p style="font-size: 0.9em; color: #666;"><em>{{ member.affiliation }}</em></p>{% endif %}
              </div>
            {% endfor %}
          </div>
        {% endif %}
      {% endfor %}
    </div>
  {% endfor %}
</div>

