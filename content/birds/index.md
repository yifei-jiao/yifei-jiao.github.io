---
title: "See Birds"
type: landing  # 告诉 Hugo 这是一个由组件构成的页面

sections:
  - block: collection
    content:
      title: My Bird Photography
      filters:
        folders:
          - birds # 指向文件夹
    design:
      view: card # 使用卡片视图
      columns: '2' # 设置为 2 列
---
