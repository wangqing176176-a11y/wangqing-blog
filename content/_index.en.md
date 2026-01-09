---
title: Notice
toc: false
---

<div class="lang-notice">
  <div class="lang-badge">🌐</div>
  <h2>内容提示 / Notice</h2>

  <p class="cn">
    由于地区与博主技术条件限制，本站目前未提供完整的英文内容支持。<br>
    请切换至<strong>中文界面</strong>以访问本站的全部文章与功能。
  </p>

  <p class="cn tip">
    如需英文阅读体验，可在中文界面使用第三方翻译功能进行翻译
    （例如 Google 翻译、Safari 浏览器自带翻译）。
  </p>

  <hr class="lang-hr" />

  <p class="en">
    Due to regional and technical limitations, the English version of this site is currently unavailable.<br>
    Please switch to the <strong>Chinese version</strong> to access the full content and features.
  </p>

  <p class="en tip">
    For English reading, you may use built-in or third-party translation tools on the Chinese version
    (e.g. Google Translate or Safari translation).
  </p>

  <div class="lang-actions">
    <a class="lang-btn primary" href="/">切换至中文 / Switch to Chinese</a>
  </div>

  <div class="lang-foot">
    本站以中文内容为准 · Chinese content is the source of truth.
  </div>
</div>

<style>
.lang-notice{
  max-width:760px;
  margin:64px auto;
  padding:28px 28px 22px;
  border-radius:18px;
  border:1px solid rgba(37,99,235,.16);
  background:rgba(37,99,235,.04);
  box-shadow:0 12px 32px rgba(15,23,42,.06);
  text-align:center;
}

.lang-badge{
  width:44px;height:44px;
  margin:0 auto 10px;
  border-radius:16px;
  display:grid;place-items:center;
  background:rgba(37,99,235,.10);
  border:1px solid rgba(37,99,235,.18);
  font-size:20px;
}

.lang-notice h2{
  margin:6px 0 14px;
  font-size:22px;
  font-weight:800;
  color:rgba(15,23,42,1);
}

.lang-notice p{
  margin:10px 0;
  line-height:1.75;
  font-size:14.5px;
  color:rgba(51,65,85,1);
}

.lang-notice p.en{
  font-size:14px;
  color:rgba(71,85,105,1);
}

.lang-notice .tip{
  font-size:13.5px;
  color:rgba(100,116,139,1);
}

.lang-hr{
  margin:16px auto;
  width:86%;
  border:none;
  height:1px;
  background:rgba(0,0,0,.06);
}

.lang-actions{
  display:flex;
  justify-content:center;
  margin-top:14px;
}

.lang-btn{
  padding:9px 18px;
  border-radius:999px;
  font-weight:800;
  font-size:14px;
  text-decoration:none !important;
  border:1px solid #2563eb;
  background:#2563eb;
  color:#fff !important;
  transition:background .15s ease, transform .15s ease;
}

.lang-btn:hover{
  background:#1d4ed8;
  transform:translateY(-1px);
}

.lang-foot{
  margin-top:14px;
  font-size:12px;
  color:rgba(148,163,184,1);
}

/* Dark mode */
html.dark .lang-notice{
  border-color:rgba(96,165,250,.22);
  background:rgba(96,165,250,.10);
  box-shadow:0 18px 60px rgba(0,0,0,.35);
}
html.dark .lang-notice h2{ color:rgba(226,232,240,1); }
html.dark .lang-notice p,
html.dark .lang-notice .tip,
html.dark .lang-notice p.en{
  color:rgba(226,232,240,.75);
}
html.dark .lang-hr{ background:rgba(255,255,255,.08); }

@media (max-width:640px){
  .lang-notice{
    margin:38px 14px;
    padding:22px 18px 18px;
  }
  .lang-hr{ width:100%; }
}
</style>
