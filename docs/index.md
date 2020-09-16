---
title: bluefeet
icon: ⛺
isHome: true
urlPath: index.html
---

<div class="docs">
{{#each docs}}{{#unless isHome}}
  <a href="{{urlPath}}">
    <div class="doc">
      <div class="doc-icon">{{icon}}</div>
      <div class="doc-title">{{title}}</div>
      <div class="doc-date">{{modifyDate}}</div>
    </div>
  </a>
{{/unless}}{{/each}}
</div>
