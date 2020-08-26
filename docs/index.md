---
title: bluefeet
subTitle: Where the Wookiee nerds out.
icon: ⛺
showComments: false
isHome: true
urlPath: index.html
---

<div class="row row-cols-1 row-cols-md-2 doc-row">
{{#each docs}}{{#unless isHome}}
  <div class="col doc-col">
    <a href="{{urlPath}}" class="doc-a">
      <div class="doc">
        <div class="doc-icon">{{icon}}</div>
        <div class="doc-title">{{title}}</div>
        <div class="doc-date">{{modifyDate}}</div>
      </div>
    </a>
  </div>
{{/unless}}{{/each}}
</div>
