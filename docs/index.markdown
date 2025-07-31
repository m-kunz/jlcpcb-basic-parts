---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

#layout: home
---

# Table of Contents

---

<ul>
  {% for cat in site.data.directory %}
    <li>
      {% if cat[1][0] %}
        {% assign components_page = site.components | where: "name", cat[0] | first %}
        <a href="{{components_page.url}}">
          {{ cat[0] }}

        </a>

      {% else %}

        <h4> {{ cat[0] }}</h4>


        <ul>
          {% for entry in cat[1] %}
            <li>
              {% assign components_page = site.components | where: "name", entry[0] | first %}
              <a href="{{components_page.url}}">{{ entry[0] }}</a>
            </li>
          {% endfor %}
        </ul>
      {% endif %}
    </li>
  {% endfor %}
</ul>