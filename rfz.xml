---
layout: null
permalink: /rfz.xml
---
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0">
<channel>
  <title>O Espírito Zombeteiro</title>
  <link>{{ "/RFZ_O_Espírito_Zombeteiro" | absolute_url }}</link>
  <description>Textos de Rafael M. Milhomens no Filosofia-Net</description>
  {% assign textos = site.pages | where: "autor", "rfz" | sort: "data" | reverse %}
  {% for t in textos %}
  <item>
    <title>{{ t.title | xml_escape }}</title>
    <link>{{ t.url | absolute_url }}</link>
    <guid>{{ t.url | absolute_url }}</guid>
    <pubDate>{{ t.data | date_to_rfc822 }}</pubDate>
  </item>
  {% endfor %}
</channel>
</rss>