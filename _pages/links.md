---
title: "社交媒体"
layout: single
permalink: /links/
author_profile: false
sidebar:
  nav: "docs"
---

你可以到以下网站，查看其他用户对三拼输入法的评论，也可以留下自己的使用感受和真实评价。<br>
如果你喜欢本输入法，请将三拼输入法介绍给更多的朋友。

{% for cat in site.data.links %}
## {{ cat.category }}

<div class="feature__wrapper" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 15px;">
  {% for item in cat.items %}
    <div class="archive__item" style="border: 1px solid var(--border-color, #f2f3f5); padding: 12px; border-radius: 6px; background: transparent; margin-top:0; display: flex; align-items: center; gap: 12px;">

      <div style="flex: 1; min-width: 0;">
        <h3 class="archive__item-title" style="margin-top: 0; margin-bottom: 2px; font-size: 0.95rem; line-height: 1.3; white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">
          <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer" style="text-decoration: none;">{{ item.title }}</a>
        </h3>
        {% if item.desc %}
          <p class="archive__item-excerpt" style="font-size: 0.8rem; color: var(--muted-text-color, #6f777d); margin: 0; line-height: 1.4; white-space: nowrap; overflow: hidden; text-overflow: ellipsis;" title="{{ item.desc }}">{{ item.desc }}</p>
        {% endif %}
      </div>
      
    </div>
  {% endfor %}
</div>
{% endfor %}



