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
  /* Hextra 风格弹窗（暗黑/浅色自适配） */
  #wq-modal-mask{
    position:fixed; inset:0;
    display:none;
    align-items:center;
    justify-content:center;
    z-index:9999;
    padding:20px;

    /* 暗黑/浅色都舒服 */
    background:rgba(0,0,0,.55);
    backdrop-filter:saturate(120%) blur(6px);
    -webkit-backdrop-filter:saturate(120%) blur(6px);
  }

  #wq-modal{
    width:min(620px, 100%);
    border-radius:18px;
    overflow:hidden;

    /* 用 Hextra 的变量，自动适配深浅色 */
    background:var(--hx-background);
    color:var(--hx-text);
    border:1px solid var(--hx-border);

    /* 阴影在暗黑下不会刺眼 */
    box-shadow:0 24px 80px rgba(0,0,0,.35);
  }

  #wq-modal header{
    padding:16px 18px 12px;
    display:flex;
    align-items:flex-start;
    justify-content:space-between;
    gap:12px;
    border-bottom:1px solid var(--hx-border);
  }

  #wq-modal .title{
    display:flex;
    flex-direction:column;
    gap:4px;
  }

  #wq-modal .title strong{
    font-size:16px;
    line-height:1.2;
    font-weight:800;
    letter-spacing:.2px;
  }

  #wq-modal .title span{
    font-size:13px;
    color:var(--hx-muted);
  }

  #wq-modal .close{
    appearance:none;
    border:1px solid var(--hx-border);
    background:transparent;
    color:var(--hx-muted);
    border-radius:12px;
    width:38px; height:38px;
    cursor:pointer;
    display:grid;
    place-items:center;
  }
  #wq-modal .close:hover{
    background:rgba(127,127,127,.10);
    color:var(--hx-text);
  }

  #wq-modal .body{
    padding:14px 18px 6px;
    line-height:1.75;
    font-size:14px;
  }

  #wq-modal .body a{
    color:var(--hx-primary);
    text-decoration:underline;
    text-underline-offset:3px;
  }

  #wq-modal .actions{
    padding:14px 18px 18px;
    display:flex;
    gap:10px;
    justify-content:flex-end;
    flex-wrap:wrap;
  }

  #wq-modal .btn{
    appearance:none;
    border:1px solid var(--hx-border);
    background:transparent;
    color:var(--hx-text);
    padding:10px 14px;
    border-radius:999px;
    cursor:pointer;
    font-weight:700;
    font-size:14px;
  }

  #wq-modal .btn:hover{
    background:rgba(127,127,127,.10);
  }

  #wq-modal .btn.primary{
    border-color:rgba(59,130,246,.35);
    background:rgba(59,130,246,.14);
    color:var(--hx-text);
  }
  #wq-modal .btn.primary:hover{
    background:rgba(59,130,246,.20);
  }

  /* 小提示条（更像“公告”而不是“系统弹窗”） */
  #wq-modal .note{
    margin-top:10px;
    padding:10px 12px;
    border:1px dashed rgba(127,127,127,.35);
    border-radius:14px;
    color:var(--hx-muted);
    background:rgba(127,127,127,.06);
    font-size:13px;
  }
</style>

<div id="wq-modal-mask" role="dialog" aria-modal="true" aria-labelledby="wq-modal-title">
  <div id="wq-modal">
    <header>
      <div class="title">
        <strong id="wq-modal-title">📌 访问提示</strong>
        <span>首次访问将弹出一次</span>
      </div>
      <button class="close" id="wq-modal-close" type="button" aria-label="关闭">✕</button>
    </header>

    <div class="body">
      <div>使用本站前，请务必阅读 <a href="/about/">关于</a> 页面中的免责声明与使用说明。</div>
      <div>继续访问、阅读或下载本站内容，即视为您已理解并同意相关约定。</div>

      <div class="note">
        建议：如需长期使用本站资源，请先完整阅读「关于」页面内容。
      </div>
    </div>

    <div class="actions">
      <a class="btn" href="/about/">查看关于</a>
      <button class="btn primary" id="wq-modal-ok" type="button">我已知晓</button>
    </div>
  </div>
</div>

<script>
(function () {
  // 只在首页弹（/ 或 /index.html）
  var path = location.pathname.replace(/\/+$/, "/");
  var isHome = (path === "/" || path === "/index.html");
  if (!isHome) return;

  var KEY = "wq_disclaimer_seen";
  try { if (localStorage.getItem(KEY) === "1") return; } catch(e) {}

  var mask = document.getElementById("wq-modal-mask");
  var ok = document.getElementById("wq-modal-ok");
  var close = document.getElementById("wq-modal-close");

  function hide() {
    mask.style.display = "none";
    try { localStorage.setItem(KEY, "1"); } catch(e) {}
  }

  mask.style.display = "flex";
  ok.addEventListener("click", hide);
  close.addEventListener("click", hide);
  mask.addEventListener("click", function(e){ if (e.target === mask) hide(); });
  document.addEventListener("keydown", function(e){ if (e.key === "Escape") hide(); });
})();
</script>
