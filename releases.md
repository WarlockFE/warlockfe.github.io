---
layout: page
title: Releases
permalink: /releases/
---
## Releases ##

{%- for release in site.github.releases -%}
  * [{{ release.name }}]({{ release.html_url }})
{%- endfor -%}
