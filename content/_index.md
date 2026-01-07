---
title: Welcome!
toc: false
---

## Welcome 👋

Hi, I'm **WangQing**.

这里是我的个人站点，用来记录  
**学习笔记 · 文档整理 · 资源分享**。

---

## Explore

{{< cards >}}
  {{< card link="docs" title="文档" subtitle="教程 / 笔记 / 索引" icon="book-open" >}}
  {{< card link="https://onedrive-cf-index-ng-2lk.pages.dev/" title="网盘" subtitle="OneDrive 文件资源" icon="cloud" >}}
  {{< card link="about" title="关于" subtitle="简介 / 计划 / 联系方式" icon="user" >}}
{{< /cards >}}

---

## Documentation

### 🕒 最近更新
> 按时间排序，展示最新内容

<ul class="hx-list">
{{ range first 5 (where .Site.RegularPages.ByDate.Reverse "Section" "docs") }}
  <li>
    <span style="color:#6b7280; margin-right:8px;">
      {{ .Date.Format "2006-01-02" }}
    </span>
    <a href="{{ .RelPermalink }}">{{ .Title }}</a>
  </li>
{{ end }}
</ul>

---

### ⭐ 推荐阅读
> 我认为值得反复查看的内容

- 📘 [从这里开始：文档索引](/docs/)
- 🧰 [工具与资源整理](/docs/)
- 👤 [关于我](/about/)
