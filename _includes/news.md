<span class="anchor" id="news"></span>

# 📰 News

{% assign news_items = site.data.news | sort: "date" | reverse %}
{% for item in news_items -%}
- **{{ item.date | replace: "-", "." }}** {{ item[page.lang] }}
{% endfor %}
