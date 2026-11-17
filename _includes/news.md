<span class="anchor" id="news"></span>

# 📰 {% if page.lang == 'zh-CN' %}最新动态{% else %}News{% endif %}

{% assign news_items = site.data.news | sort: "date" | reverse %}
{% for item in news_items -%}
- **{{ item.date | replace: "-", "." }}** {{ item[page.lang] }}
{% endfor %}
