<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Tu Nota Secreta ✨</title>
<style>
  :root{--card-bg:#fff;--accent:#2b6cb0;--soft:#f3f6fb;--shadow: 0 6px 18px rgba(8,20,50,.08);}
  body{font-family:system-ui,-apple-system,Segoe UI,Roboto,'Helvetica Neue',Arial; margin:0; background: linear-gradient(180deg,#f7fbff 0%, #fcfcff 100%); color:#14213d;}
  .wrap{max-width:920px;margin:36px auto;padding:18px;}
  header{display:flex;align-items:center;gap:12px}
  header h1{font-size:20px;margin:0}
  .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:16px;margin-top:18px}
  .note{background:var(--card-bg);border-radius:12px;padding:14px;box-shadow:var(--shadow);cursor:pointer;overflow:hidden;transition:transform .22s ease,box-shadow .22s ease;}
  .note:hover{transform:translateY(-6px)}
  .note .title{display:flex;justify-content:space-between;align-items:center}
  .note h2{font-size:16px;margin:0}
  .note p.meta{margin:8px 0 0 0;font-size:13px;color:#4a5568}
  .content{max-height:0;overflow:hidden;transition:max-height .36s ease;padding-top:0}
  .content.open{padding-top:12px;max-height:600px}
  .thumb{width:100%;height:160px;background:#efefef;border-radius:8px;display:block;object-fit:cover;margin-top:10px}
  .media{margin-top:10px}
  .btn{display:inline-block;padding:8px 12px;border-radius:8px;background:var(--accent);color:white;text-decoration:none;font-weight:600;margin-top:10px}
  footer{margin-top:22px;font-size:13px;color:#6b7280}
  /* small animation for opening note */
  .note.open {box-shadow:0 18px 40px rgba(8,20,50,.14); transform:translateY(-8px) scale(1.01)}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='44' height='44'><rect rx='10' width='44' height='44' fill='%232b6cb0'/><text x='50%' y='54%' font-size='20' text-anchor='middle' fill='white' font-family='Arial' dy='.3em'>✉️</text></svg>" alt="" width="44" height="44">
    <div>
      <h1>Tu nota secreta — ¡Desliza y abre!</h1>
      <div style="font-size:13px;color:#6b7280">Escanea y toca cada nota para abrirla. Incluye imagen, audio y video.</div>
    </div>
  </header>

  <div class="grid" id="grid">
    <!-- Nota 1 -->
    <article class="note" data-id="n1">
      <div class="title">
        <h2>Nota 1 — Un dulce inicio</h2>
        <div style="font-size:12px;color:#6b7280">Miércoles</div>
      </div>
      <p class="meta">Un pequeño detalle para endulzar tu día.</p>
      <div class="content" aria-hidden="true">
        <img class="thumb" src="https://images.unsplash.com/photo-1544025162-d76694265947?q=80&w=800&auto=format&fit=crop&crop=entropy" alt="Galletas">
        <div class="media">
          <p>¡Que tengas un miércoles con una sonrisa! 🍪</p>
        </div>
      </div>
    </article>

    <!-- Nota 2 -->
    <article class="note" data-id="n2">
      <div class="title">
        <h2>Nota 2 — Pequeña cortesía</h2>
        <div style="font-size:12px;color:#6b7280">Viernes</div>
      </div>
      <p class="meta">Un gesto que llega puntual.</p>
      <div class="content" aria-hidden="true">
        <img class="thumb" src="https://images.unsplash.com/photo-1504754524776-8f4f37790ca0?q=80&w=800&auto=format&fit=crop&crop=entropy" alt="Café">
        <div class="media">
          <p>Que tu viernes tenga un momento de calma. ☕</p>
          <audio controls style="width:100%;margin-top:8px">
            <source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg">
            Tu navegador no soporta audio.
          </audio>
        </div>
      </div>
    </article>

    <!-- Nota 3 con vídeo -->
    <article class="note" data-id="n3">
      <div class="title">
        <h2>Nota 3 — Un pequeño clip</h2>
        <div style="font-size:12px;color:#6b7280">Miércoles</div>
      </div>
      <p class="meta">Una sonrisa en formato video.</p>
      <div class="content" aria-hidden="true">
        <img class="thumb" src="https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=800&auto=format&fit=crop&crop=entropy" alt="Regalo">
        <div class="media">
          <!-- YouTube embed: reemplaza VIDEO_ID -->
          <div style="position:relative;padding-top:56.25%;border-radius:8px;overflow:hidden;margin-top:8px">
            <iframe src="https://www.youtube.com/embed/VIDEO_ID?rel=0&showinfo=0" style="position:absolute;top:0;left:0;width:100%;height:100%;border:0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
      </div>
    </article>

    <!-- Nota 4 -->
    <article class="note" data-id="n4">
      <div class="title">
        <h2>Nota 4 — Casi al final</h2>
        <div style="font-size:12px;color:#6b7280">Viernes</div>
      </div>
      <p class="meta">Preparando la sorpresa final.</p>
      <div class="content" aria-hidden="true">
        <img class="thumb" src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=800&auto=format&fit=crop&crop=entropy" alt="Sorpresa">
        <div class="media">
          <p>Un abrebocas antes de la sorpresa final — ¡emocionada/o? ✨</p>
        </div>
      </div>
    </article>

    <!-- Nota 5 -->
    <article class="note" data-id="n5">
      <div class="title">
        <h2>Nota 5 — Última pista</h2>
        <div style="font-size:12px;color:#6b7280">Miércoles / Viernes</div>
      </div>
      <p class="meta">La próxima vez… la gran sorpresa.</p>
      <div class="content" aria-hidden="true">
        <img class="thumb" src="https://images.unsplash.com/photo-1546413113-6e7f17f7fbf9?q=80&w=800&auto=format&fit=crop&crop=entropy" alt="Final">
        <div class="media">
          <p>Que tu día termine con alegría y curiosidad. 🎉</p>
        </div>
      </div>
    </article>
  </div>

  <footer>Si quieres volver a ver una nota, vuelve a tocarla. (No pedimos datos personales)</footer>
</div>

<script>
  // Toggle open/close notes
  document.querySelectorAll('.note').forEach(n=>{
    n.addEventListener('click', ()=>{
      const wasOpen = n.classList.contains('open');
      // close all
      document.querySelectorAll('.note').forEach(x=>{
        x.classList.remove('open');
        x.querySelector('.content').classList.remove('open');
        x.querySelector('.content').setAttribute('aria-hidden','true');
      });
      if(!wasOpen){
        n.classList.add('open');
        const c = n.querySelector('.content');
        c.classList.add('open');
        c.setAttribute('aria-hidden','false');
        // ensure max-height adapts (use scrollHeight)
        c.style.maxHeight = c.scrollHeight + 'px';
      }
    });
  });

  // make content collapse smoothly when window resized
  window.addEventListener('resize', ()=>{
    document.querySelectorAll('.content.open').forEach(c=>{
      c.style.maxHeight = c.scrollHeight + 'px';
    });
  });
</script>
</body>
</html>
