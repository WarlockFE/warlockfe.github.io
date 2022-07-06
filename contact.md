---
layout: page
title: Contact
permalink: /contact/
---

Please visit us on Slack at [warlockfe.slack.com](https://warlockfe.slack.com/) using the form below.
We're happy to answer any questions or address any problems you might be having.

<div id="CommunityInviter"></div>
<script>
  window.CommunityInviterAsyncInit = function () {
    CommunityInviter.init({
      app_url:'warlock',
      team_id:'warlockfe'
   })
  };

  (function(d, s, id){
    var js, fjs = d.getElementsByTagName(s)[0];
    if (d.getElementById(id)) {return;}
    js = d.createElement(s); js.id = id;
    js.src = "https://communityinviter.com/js/communityinviter.js";
    fjs.parentNode.insertBefore(js, fjs);
  }(document, 'script', 'Community_Inviter'));
</script>

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
