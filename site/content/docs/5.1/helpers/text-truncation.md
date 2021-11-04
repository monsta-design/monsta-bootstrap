---
layout: docs
title: Text truncation
description: Truncate long strings of text with an ellipsis.
group: helpers
toc: false
---

For longer content, you can add a `.text-truncate` class to truncate the text with an ellipsis. **Requires `display: inline-block` or `display: block`.**

{{< example >}}
<!-- Block level -->
<div class="bs-row">
  <div class="bs-col-2 bs-text-truncate">
    This text is quite long, and will be truncated once displayed.
  </div>
</div>

<!-- Inline level -->
<span class="bs-d-inline-block bs-text-truncate" style="max-width: 150px;">
  This text is quite long, and will be truncated once displayed.
</span>
{{< /example >}}
