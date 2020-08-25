---
title: bluefeet
subTitle: Where the Wookiee nerds out.
icon: ⛺
showComments: false
isHome: true
urlPath: index.html
---

<div class="row row-cols-1 row-cols-lg-2">
{{#each docs}}
  <div class="col">
    <a href="{{urlPath}}" class="doc-a">
      <div class="row doc-tile">
        <div class="col-auto doc-tile-icon">{{icon}}</div>
        <div class="col doc-tile-title">{{title}}</div>
        <div class="col-auto doc-tile-date">{{modifyDate}}</div>
      </div>
    </a>
  </div>
{{/each}}
</div>
