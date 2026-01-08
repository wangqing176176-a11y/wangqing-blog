---
title: PDF测试页面（密码访问）
date: 2026-01-08
---

{{< page-password "wang176176" >}}

## 📄 文档说明
这是配套 PDF 资料，可在线阅读或下载。

<div class="wq-pdf-card">
  <div class="wq-pdf-head">
    <div class="wq-pdf-title">
      <div class="wq-pdf-icon">📎</div>
      <div>
        <div class="wq-pdf-name">城铁工程系五育之星评选活动</div>
        <div class="wq-pdf-meta">PDF · 在线预览 / 可下载</div>
      </div>
    </div>

    <a class="wq-pdf-btn" href="./城铁工程系五育之星评选活动.pdf" download>
      下载 PDF
      <span class="wq-pdf-arrow">→</span>
    </a>
  </div>

  <div class="wq-pdf-frame">
    <iframe
      src="./城铁工程系五育之星评选活动.pdf"
      loading="lazy"
      title="PDF 预览"
    ></iframe>
  </div>
</div>

<style>
  /* ===== Apple 卡片风：PDF 预览模块（暗黑也好看） ===== */
  .wq-pdf-card{
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    background: rgba(255,255,255,.75);
    box-shadow: 0 14px 40px rgba(15,23,42,.08);
    overflow: hidden;
    margin: 18px 0 10px;
  }
  .wq-pdf-head{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap: 14px;
    padding: 14px 16px;
    border-bottom: 1px solid rgba(0,0,0,.06);
    background: rgba(248,250,252,.60);
  }
  .wq-pdf-title{
    display:flex;
    align-items:center;
    gap: 12px;
    min-width: 0;
  }
  .wq-pdf-icon{
    width: 38px;
    height: 38px;
    border-radius: 14px;
    display:grid;
    place-items:center;
    background: rgba(37,99,235,.10);
    border: 1px solid rgba(37,99,235,.18);
    flex: 0 0 auto;
  }
  .wq-pdf-name{
    font-weight: 800;
    line-height: 1.2;
    font-size: 15px;
    margin-bottom: 2px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .wq-pdf-meta{
    font-size: 12.5px;
    color: rgba(100,116,139,1);
  }

  /* 下载按钮：同色系，克制 Apple 风 */
  .wq-pdf-btn{
    display:inline-flex;
    align-items:center;
    gap: 8px;
    padding: 9px 12px;
    border-radius: 999px;
    border: 1px solid rgba(37,99,235,.22);
    background: rgba(37,99,235,.10);
    color: rgba(29,78,216,1) !important;
    text-decoration: none !important;
    font-weight: 800;
    font-size: 13px;
    white-space: nowrap;
    transition: background .15s ease, border-color .15s ease, transform .15s ease;
  }
  .wq-pdf-btn:hover{
    background: rgba(37,99,235,.14);
    border-color: rgba(37,99,235,.30);
    transform: translateY(-1px);
  }
  .wq-pdf-arrow{ opacity:.9; }

  /* PDF 预览窗：更像 macOS 组件 */
  .wq-pdf-frame{
    position: relative;
    padding: 0;
    background: rgba(255,255,255,.55);
  }
  .wq-pdf-frame iframe{
    width: 100%;
    height: 820px;          /* 想更高就改这里 */
    border: 0;
    display:block;
    background: transparent;
  }

  /* 暗黑模式适配 */
  html.dark .wq-pdf-card{
    border-color: rgba(255,255,255,.10);
    background: rgba(24,24,27,.55);
    box-shadow: 0 18px 60px rgba(0,0,0,.35);
  }
  html.dark .wq-pdf-head{
    border-bottom-color: rgba(255,255,255,.08);
    background: rgba(255,255,255,.03);
  }
  html.dark .wq-pdf-meta{
    color: rgba(209,213,219,.72);
  }
  html.dark .wq-pdf-icon{
    background: rgba(147,197,253,.10);
    border-color: rgba(147,197,253,.20);
  }
  html.dark .wq-pdf-btn{
    border-color: rgba(147,197,253,.22);
    background: rgba(147,197,253,.10);
    color: rgba(191,219,254,1) !important;
  }
  html.dark .wq-pdf-btn:hover{
    background: rgba(147,197,253,.14);
    border-color: rgba(147,197,253,.32);
  }
</style>
