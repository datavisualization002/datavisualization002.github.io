---
title: "Univariate & Bivariate"
slug: "univariate-bivariate"
---

<style>
.fl-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:14px;}
.fl-thumb{border:1px solid #e6e6e6;border-radius:12px;overflow:hidden;cursor:pointer;background:#fff;}
.fl-thumb img{display:block;width:100%;height:auto;}
.fl-cap{padding:10px;font-weight:600;}

.fl-modal{position:fixed;inset:0;background:rgba(0,0,0,.6);display:none;align-items:center;justify-content:center;padding:18px;z-index:9999;}
.fl-modal.open{display:flex;}
.fl-modal-content{background:#fff;border-radius:14px;max-width:1100px;width:100%;padding:10px;position:relative;}
.fl-close{position:absolute;right:12px;top:10px;border:0;background:transparent;font-size:22px;cursor:pointer;padding:6px 10px;z-index:2;}

.fl-embed-wrap{padding:10px;}
.fl-iframe{width:100%;height:75vh;border:0;border-radius:10px;}
</style>

<div class="fl-grid">
  <div class="fl-thumb" onclick="openFl(27530571)">
    <img src="https://public.flourish.studio/visualisation/27530571/thumbnail" alt="Figure 1">
    <div class="fl-cap">Figure 1 — Title</div>
  </div>

  <div class="fl-thumb" onclick="openFl(27572844)">
    <img src="https://public.flourish.studio/visualisation/27572844/thumbnail" alt="Figure 2">
    <div class="fl-cap">Figure 2 — Title</div>
  </div>
</div>

<div id="flModal" class="fl-modal" onclick="closeFl()">
  <div class="fl-modal-content" onclick="event.stopPropagation()">
    <button class="fl-close" onclick="closeFl()">✕</button>
    <div class="fl-embed-wrap" id="flEmbed"></div>
  </div>
</div>

<script>
function openFl(id){
  const wrap = document.getElementById('flEmbed');

  // Use Flourish's embed page inside an iframe (most reliable)
  wrap.innerHTML = `
    <iframe class="fl-iframe"
      src="https://public.flourish.studio/visualisation/${id}/embed"
      loading="lazy"
      allowfullscreen>
    </iframe>
  `;

  document.getElementById('flModal').classList.add('open');
}

function closeFl(){
  document.getElementById('flModal').classList.remove('open');
  document.getElementById('flEmbed').innerHTML = '';
}
</script>
