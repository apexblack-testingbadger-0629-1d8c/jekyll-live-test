---
layout: null
---
# YAML Deserialization Test
{{ site.data.evil.yaml_test | default: "NO DATA LOADED" }}
{% for item in site.data.evil %}
Item: {{ item[0] }} = {{ item[1] }}
{% endfor %}
