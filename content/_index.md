---
title: 
toc: false
---

## Welcome 👋

Hi, I'm **WangQing**.

这里是我的个人站点，用来记录  **学习笔记 · 文档整理 · 资源分享**。

> 📌 **使用本站前，请务必阅读「[关于](/about)」页面。**  
> 继续访问、阅读或下载本站内容，即视为您已理解并同意相关说明与约定。


## Explore

{{< cards >}}
  {{< card link="docs" title="文档" subtitle="教程 / 笔记 / 索引" icon="book-open" >}}
  {{< card link="https://onedrive-cf-index-ng-2lk.pages.dev/" title="网盘" subtitle="OneDrive 文件资源" icon="cloud" >}}
  {{< card link="about" title="关于" subtitle="站点说明 / 使用声明 / 联系方式" icon="user" >}}
{{< /cards >}}



## Documentation

### 🕒 最近更新
> 按时间排序，展示最新内容

{{< recent-docs >}}



### ⭐ 推荐阅读
> 我认为值得反复查看的内容

- 📘 [从这里开始：文档索引](/docs/)
- 🧰 [工具与资源整理](/docs/)
- 👤 [关于我](/about/)



<style>
  .site-modal {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.45);
    backdrop-filter: blur(6px);
    -webkit-backdrop-filter: blur(6px);
    z-index: 9999;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 18px;
  }

  .site-modal-content {
    /* 默认浅色（保持你第一版质感） */
    background: #ffffff;
    color: #111827;
    border: 1px solid rgba(17, 24, 39, 0.10);

    max-width: 520px;
    width: calc(100% - 32px);
    padding: 24px 28px;
    border-radius: 12px;
    box-shadow: 0 10px 40px rgba(0,0,0,.2);
    font-size: 15px;
    line-height: 1.7;
  }

  .site-modal-content h3 {
    margin: 0 0 10px;
    font-size: 18px;
    font-weight: 800;
    letter-spacing: .2px;
  }

  .site-modal-content p {
    margin: 10px 0;
  }

  .site-modal-content a {
    color: #2563eb;
    font-weight: 700;
    text-decoration: none;
  }
  .site-modal-content a:hover {
    text-decoration: underline;
    text-underline-offset: 3px;
  }

  .site-modal-actions {
    text-align: right;
    margin-top: 18px;
  }

  .site-modal-actions button {
    background: #2563eb;
    color: #fff;
    border: none;
    padding: 8px 16px;
    border-radius: 8px;
    cursor: pointer;
    font-size: 14px;
    font-weight: 700;
  }
  .site-modal-actions button:hover {
    opacity: 0.92;
  }

  /* ===== 暗黑模式适配（优先用 Hextra 变量，保证协调） ===== */
  html.dark .site-modal {
    background: rgba(0, 0, 0, 0.60);
  }
  html.dark .site-modal-content {
    background: var(--hx-background, #0b1220);
    color: var(--hx-text, #e5e7eb);
    border: 1px solid var(--hx-border, rgba(255,255,255,.10));
    box-shadow: 0 18px 70px rgba(0,0,0,.55);
  }
  html.dark .site-modal-content a {
    color: var(--hx-primary, #60a5fa);
  }
  html.dark .site-modal-actions button {
    background: rgba(96, 165, 250, 0.18);
    color: var(--hx-text, #e5e7eb);
    border: 1px solid rgba(96, 165, 250, 0.35);
  }
  html.dark .site-modal-actions button:hover {
    background: rgba(96, 165, 250, 0.25);
    opacity: 1;
  }

  /* 如果系统暗黑但主题没加 dark class，也兜底一下 */
  @media (prefers-color-scheme: dark) {
    .site-modal-content {
      background: var(--hx-background, #0b1220);
      color: var(--hx-text, #e5e7eb);
      border: 1px solid var(--hx-border, rgba(255,255,255,.10));
    }
  }
</style>
  ok.addEventListener("click", hide);
  close.addEventListener("click", hide);
  mask.addEventListener("click", function(e){ if (e.target === mask) hide(); });
  document.addEventListener("keydown", function(e){ if (e.key === "Escape") hide(); });
})();
</script>
