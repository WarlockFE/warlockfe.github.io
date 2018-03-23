---
layout: page
title: Contact
permalink: /contact/
---

Please visit use on Slack at [warlockfe.slack.com](https://warlockfe.slack.com/), if you have any questions or suggestions
or if you would like to get involved with the project.

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
