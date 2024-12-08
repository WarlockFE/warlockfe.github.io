---
layout: page
title: Contact
permalink: /contact/
---

Please visit us on Discord using [our Discord invite](https://discord.gg/RrvTffra).
We're happy to answer any questions or address any problems you might be having.

### Authors ###

<ul class="contact-list">
{%- for author in site.authors -%}
  <li class="p-name">
  {%- if author[1].email -%}
    <a class="u-email" href="mailto:{{ author[1].email }}">{{ author[1].name }}</a>
  {%- else -%}
    {{ author[1].name }}
  {%- endif -%}
  </li>
{%- endfor -%}
</ul>
