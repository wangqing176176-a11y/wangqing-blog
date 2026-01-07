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
  /* 首页首次访问弹窗（仅本页） */
  #wq-modal-mask{
    position:fixed; inset:0;
    background:rgba(0,0,0,.45);
    display:none;
    align-items:center;
    justify-content:center;
    z-index:9999;
    padding:20px;
  }
  #wq-modal{
    width:min(560px, 100%);
    background:var(--hx-background, #fff);
    border:1px solid rgba(0,0,0,.08);
    border-radius:16px;
    box-shadow:0 20px 60px rgba(0,0,0,.25);
    overflow:hidden;
  }
  #wq-modal header{
    padding:16px 18px;
    display:flex;
    gap:10px;
    align-items:center;
    justify-content:space-between;
    border-bottom:1px solid rgba(0,0,0,.08);
  }
  #wq-modal header strong{
    font-size:16px;
  }
  #wq-modal .body{
    padding:16px 18px;
    line-height:1.7;
    color:var(--hx-text, #111);
  }
  #wq-modal .actions{
    padding:14px 18px 18px;
    display:flex;
    gap:10px;
    justify-content:flex-end;
  }
  #wq-modal .btn{
    appearance:none;
    border:1px solid rgba(0,0,0,.12);
    background:rgba(0,0,0,.03);
    color:inherit;
    padding:10px 14px;
    border-radius:12px;
    cursor:pointer;
    font-weight:600;
  }
  #wq-modal .btn.primary{
    border-color:rgba(37,99,235,.25);
    background:rgba(37,99,235,.10);
  }
  #wq-modal .btn:hover{
    filter:brightness(.98);
  }
  #wq-modal a{
    text-decoration:underline;
  }
</style>

<div id="wq-modal-mask" role="dialog" aria-modal="true" aria-labelledby="wq-modal-title">
  <div id="wq-modal">
    <header>
      <strong id="wq-modal-title">📌 访问提示</strong>
      <button class="btn" id="wq-modal-close" type="button">关闭</button>
    </header>
    <div class="body">
      <p>使用本站前，请务必阅读 <a href="/about/">关于</a> 页面中的免责声明与使用说明。</p>
      <p>继续访问、阅读或下载本站内容，即视为您已理解并同意相关约定。</p>
    </div>
    <div class="actions">
      <a class="btn" href="/about/">去查看关于</a>
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
  try {
    if (localStorage.getItem(KEY) === "1") return;
  } catch(e) {}

  var mask = document.getElementById("wq-modal-mask");
  var ok = document.getElementById("wq-modal-ok");
  var close = document.getElementById("wq-modal-close");

  function hide() {
    mask.style.display = "none";
    try { localStorage.setItem(KEY, "1"); } catch(e) {}
  }

  // 显示
  mask.style.display = "flex";

  ok.addEventListener("click", hide);
  close.addEventListener("click", hide);

  // 点击遮罩关闭
  mask.addEventListener("click", function(e){
    if (e.target === mask) hide();
  });

  // ESC 关闭
  document.addEventListener("keydown", function(e){
    if (e.key === "Escape") hide();
  });
})();
</script>
