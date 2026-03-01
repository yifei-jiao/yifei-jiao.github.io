---
title: "See Birds"
resources:
  - src: "*.jpg"
    name: gallery
---

DEBUG: 资源数量是 {{ printf "%d" (len .Resources) }}

{{< gallery album="gallery" >}}
