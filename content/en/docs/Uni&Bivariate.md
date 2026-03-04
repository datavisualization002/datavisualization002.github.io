---
title: Univariate & Bivariate
slug: Univariate&Bivariate
---

<style>
.fl-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:14px;}
.fl-thumb{border:1px solid #e6e6e6;border-radius:12px;overflow:hidden;cursor:pointer;background:#fff;}
.fl-thumb img{display:block;width:100%;height:auto;}
.fl-cap{padding:10px;font-weight:600;}
.fl-modal{position:fixed;inset:0;background:rgba(0,0,0,.6);display:none;align-items:center;justify-content:center;padding:18px;z-index:9999;}
.fl-modal.open{display:flex;}
.fl-modal-content{background:#fff;border-radius:14px;max-width:1100px;width:100%;padding:10px;}
.fl-close{float:right;border:0;background:transparent;font-size:22px;cursor:pointer;padding:6px 10px;}
.fl-embed-wrap{padding:10px;}
.fl-embed-wrap .flourish-embed{min-height:520px;}
</style>

<script src="https://public.flourish.studio/resources/embed.js"></script>

<div class="fl-grid">
  <div class="fl-thumb" onclick="openFl('visualisation/27530571')">
    <img src="https://public.flourish.studio/visualisation/27530571/embed" alt="Figure 1">
    <div class="fl-cap">Figure 1 — Title</div>
  </div>

  <div class="fl-thumb" onclick="openFl('visualisation/27572844')">
    <img src="https://public.flourish.studio/visualisation/27572844/thumbnail" alt="Figure 2">
    <div class="fl-cap">Figure 2 — Title</div>
  </div>
</div>

<div id="flModal" class="fl-modal" onclick="closeFl(event)">
  <div class="fl-modal-content" onclick="event.stopPropagation()">
    <button class="fl-close" onclick="closeFl()">✕</button>
    <div class="fl-embed-wrap" id="flEmbed"></div>
  </div>
</div>

<script>
function openFl(src){
  const wrap = document.getElementById('flEmbed');
  wrap.innerHTML = `<div class="flourish-embed flourish-chart" data-src="${src}"></div>`;

  // Force Flourish embed.js to re-run and scan the newly injected div
  const old = document.getElementById('flourish-embed-js');
  if (old) old.remove();

  const s = document.createElement('script');
  s.id = 'flourish-embed-js';
  s.src = "https://public.flourish.studio/resources/embed.js?v=" + Date.now();
  s.async = true;
  document.body.appendChild(s);

  document.getElementById('flModal').classList.add('open');
}

function closeFl(){
  document.getElementById('flModal').classList.remove('open');
  document.getElementById('flEmbed').innerHTML = '';
}
</script>
