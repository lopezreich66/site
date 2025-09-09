<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Choice Store — Loja Moderna</title>
  <meta name="description" content="Site exemplo moderno e responsivo — hero, features, galeria, rodapé e formulário de contato." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1724; /* escuro */
      --card:#0b1220;
      --muted:#94a3b8;
      --accent:#7c3aed; /* roxo */
      --glass: rgba(255,255,255,0.04);
      --radius:14px;
      color-scheme: dark;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,'Helvetica Neue',Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(124,58,237,0.12), transparent),
                  linear-gradient(180deg, #071021 0%, #081226 100%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:32px;
    }
    .container{max-width:1100px;margin:0 auto}

    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:54px;height:54px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#06b6d4);display:flex;align-items:center;justify-content:center;font-weight:800}
    .brand h1{font-size:18px;margin:0}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px;font-weight:600}
    nav a.cta{background:linear-gradient(90deg,var(--accent),#06b6d4);padding:10px 14px;border-radius:10px;color:#fff}

    /* HERO */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;margin-top:36px}
    .hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:28px;border-radius:var(--radius);backdrop-filter:blur(6px);box-shadow:0 6px 30px rgba(2,6,23,0.6)}
    .hero h2{margin:0;font-size:32px}
    .hero p{color:var(--muted);margin-top:12px}
    .actions{display:flex;gap:12px;margin-top:18px}
    .btn{padding:12px 16px;border-radius:12px;border:0;font-weight:700;cursor:pointer}
    .btn-primary{background:var(--accent);color:white}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}

    /* cards features */
    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:22px}
    .feature{background:var(--card);padding:18px;border-radius:12px}
    .feature h3{margin:0 0 8px 0}
    .feature p{color:var(--muted);font-size:14px;margin:0}

    /* right column mockup */
    .mockup{background:linear-gradient(180deg, rgba(255,255,255,0.03), transparent);border-radius:14px;padding:18px}
    .product{display:flex;gap:12px;align-items:center;padding:10px;background:var(--glass);border-radius:12px;margin-bottom:12px}
    .product img{width:70px;height:70px;border-radius:10px;object-fit:cover}
    .price{font-weight:700}

    /* gallery */
    .gallery{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-top:26px}
    .gallery img{width:100%;height:120px;object-fit:cover;border-radius:10px}

    /* CTA */
    .cta{display:flex;align-items:center;justify-content:space-between;margin-top:26px;padding:18px;background:linear-gradient(90deg, rgba(124,58,237,0.12), rgba(6,182,212,0.06));border-radius:12px}

    footer{margin-top:28px;color:var(--muted);display:flex;justify-content:space-between;align-items:center}

    /* responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr;}
      .gallery{grid-template-columns:repeat(2,1fr)}
      .features{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:540px){
      body{padding:18px}
      .features{grid-template-columns:1fr}
      .gallery img{height:96px}
      nav a{display:none}
    }

    /* small form */
    .form{display:flex;gap:8px}
    .form input{flex:1;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.06);background:transparent;color:inherit}
    .form button{padding:12px 14px;border-radius:10px;border:0;background:var(--accent);color:white}

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">CS</div>
        <div>
          <h1>Choice Store</h1>
          <div style="font-size:12px;color:var(--muted)">Produtos selecionados • Entrega rápida</div>
        </div>
      </div>
      <nav>
        <a href="#features">Recursos</a>
        <a href="#prod">Produtos</a>
        <a href="#contato" class="cta">Comprar agora</a>
      </nav>
    </header>

    <section class="hero">
      <div class="hero-card">
        <h2>Encontre os melhores produtos — rápido e sem complicação</h2>
        <p>Smartwatches, tênis, batons e muito mais com curadoria diária e frete eficiente. Design limpo, busca rápida e checkout em 1 minuto.</p>

        <div class="actions">
          <button class="btn btn-primary">Ver coleções</button>
          <button class="btn btn-ghost">Como funciona</button>
        </div>

        <div class="features" id="features" style="margin-top:22px">
          <div class="feature">
            <h3>Entrega Expressa</h3>
            <p>Rastreamento em tempo real e envio em menos de 48h para as principais cidades.</p>
          </div>
          <div class="feature">
            <h3>Pagamentos Seguros</h3>
            <p>Cartão, boleto e pix com checkout protegido e parcelamento flexível.</p>
          </div>
          <div class="feature">
            <h3>Devolução Fácil</h3>
            <p>7 dias para troca ou devolução sem burocracia.</p>
          </div>
        </div>
      </div>

      <aside class="mockup">
        <div style="font-size:13px;color:var(--muted);margin-bottom:8px">Destaques do dia</div>
        <div class="product">
          <img src="https://images.unsplash.com/photo-1526178616301-3a3712d9f0eb?q=80&w=400&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="smartwatch">
          <div>
            <div style="font-weight:700">Smartwatch X2</div>
            <div style="font-size:13px;color:var(--muted)">Monitor cardíaco • 7 dias bateria</div>
          </div>
          <div style="margin-left:auto;text-align:right">
            <div class="price">R$ 349</div>
            <div style="font-size:12px;color:var(--muted)">ou 6x s/juros</div>
          </div>
        </div>

        <div class="product">
          <img src="https://images.unsplash.com/photo-1519741491600-4c0f6bdd92b7?q=80&w=400&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="tenis">
          <div>
            <div style="font-weight:700">Tênis Runner</div>
            <div style="font-size:13px;color:var(--muted)">Confortável • Solado anti-impacto</div>
          </div>
          <div style="margin-left:auto;text-align:right">
            <div class="price">R$ 179</div>
            <div style="font-size:12px;color:var(--muted)">em até 4x</div>
          </div>
        </div>

        <div style="font-size:13px;color:var(--muted);margin-top:6px">Receba novidades</div>
        <form class="form" onsubmit="event.preventDefault();alert('Obrigado! Você será notificado.');">
          <input type="email" placeholder="seu@email.com" required />
          <button type="submit">Inscrever</button>
        </form>
      </aside>
    </section>

    <section style="margin-top:26px">
      <h2 style="margin:0 0 12px 0">Galeria</h2>
      <div class="gallery">
        <img src="https://images.unsplash.com/photo-1512496015851-a90fb38ba796?q=80&w=800&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="gal1">
        <img src="https://images.unsplash.com/photo-1519744792095-2f2205e87b6f?q=80&w=800&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="gal2">
        <img src="https://images.unsplash.com/photo-1483985988355-763728e1935b?q=80&w=800&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="gal3">
        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=800&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="gal4">
      </div>
    </section>

    <section class="cta">
      <div>
        <strong style="font-size:18px">Pronto para melhorar sua loja?</strong>
        <div style="color:var(--muted);font-size:13px;margin-top:6px">Crie sua vitrine, edite produtos e acompanhe vendas em um painel simples.</div>
      </div>
      <div>
        <button class="btn btn-primary" onclick="alert('Vamos começar!')">Criar minha loja</button>
      </div>
    </section>

    <footer>
      <div>© <span id="ano"></span> Choice Store — Todos os direitos reservados</div>
      <div style="display:flex;gap:18px;align-items:center">
        <div style="font-size:13px;color:var(--muted)">Suporte</div>
        <div style="font-size:13px;color:var(--muted)">Contato</div>
      </div>
    </footer>
  </div>

  <script>
    document.getElementById('ano').textContent = new Date().getFullYear();
  </script>
</body>
</html>
