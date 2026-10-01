---
# AI Benchmarks — custom content-page layout (not part of stock Mr. Green
# Jekyll Theme, which only ships per-feature layouts: about/links/projects/
# archives/post-list/home/privacy-policy). Modeled directly on their
# privacy-policy.md layout (simplest content wrapper: default chrome +
# markdown-style div) since our 16 pages are plain reference markdown.
layout: default
---
<div class="multipurpose-container">
  <div class="markdown-style">
    {{ content }}
  </div>
</div>
