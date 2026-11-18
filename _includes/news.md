<span class="anchor" id="news"></span>

# 📰 {% if page.lang == 'zh-CN' %}最新动态{% else %}News{% endif %}

{% assign news_items = site.data.news | sort: "date" | reverse %}
{% for item in news_items -%}
{% assign news_text = item[page.lang] -%}
{% if news_text and news_text != empty -%}
- **{{ item.date | replace: "-", "." }}** {{ news_text }}
{% endif -%}
{% endfor %}
