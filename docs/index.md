
# JLCPCB Basic and Preferred Part Overview


{% for category in site.components %}
  <h2>
    <a href="{{ category.url }}">
      {{ category.name }}
    </a>
  </h2>
  <p>{{ category.content | markdownify }}</p>
{% endfor %}