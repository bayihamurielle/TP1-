<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ogooué Numérique — Actualités</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --forest-900:#0c211b;
    --forest-800:#12312a;
    --forest-700:#1b473c;
    --gold-500:#c99a4a;
    --gold-300:#e3c07d;
    --cream-100:#f6f1e7;
    --cream-200:#e9e0cc;
    --ink:#0c211b;
    --radius:14px;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--cream-100);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    line-height:1.55;
  }
  h1,h2,h3{font-family:'Fraunces',serif;margin:0;}
  a{color:inherit;}
  img{max-width:100%;display:block;}

  /* -------- Header -------- */
  header.site-header{
    background:var(--forest-900);
    color:var(--cream-100);
    padding:1.75rem 1.5rem 3.25rem;
    position:relative;
  }
  .header-inner{
    max-width:1100px;
    margin:0 auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:1rem;
    flex-wrap:wrap;
  }
  .brand{display:flex;align-items:center;gap:.7rem;}
  .brand-mark{
    width:38px;height:38px;border-radius:50%;
    background:conic-gradient(from 200deg, var(--gold-300), var(--gold-500), var(--forest-700));
    flex-shrink:0;
  }
  .brand-name{font-family:'Fraunces',serif;font-size:1.35rem;font-weight:600;letter-spacing:.2px;}
  .brand-tagline{font-size:.78rem;color:var(--cream-200);opacity:.75;margin-top:-2px;}

  .site-title{
    max-width:1100px;margin:2.5rem auto 0;
  }
  .site-title h1{font-size:clamp(2rem,4.5vw,3.2rem);font-weight:700;max-width:700px;}
  .site-title p{color:var(--cream-200);opacity:.85;max-width:520px;margin-top:.6rem;font-size:1.02rem;}

  /* river divider — signature element */
  .river-divider{
    display:block;width:100%;height:56px;margin-top:-1px;
  }

  /* -------- Nav -------- */
  nav.main-nav{
    background:var(--forest-800);
    border-bottom:1px solid rgba(233,224,204,.12);
  }
  nav.main-nav ul{
    max-width:1100px;margin:0 auto;padding:0 1.5rem;
    list-style:none;display:flex;gap:2rem;flex-wrap:wrap;
  }
  nav.main-nav a{
    display:inline-block;padding:.9rem 0;color:var(--cream-200);
    text-decoration:none;font-size:.95rem;font-weight:500;
    border-bottom:2px solid transparent;transition:border-color .2s, color .2s;
  }
  nav.main-nav a:hover,
  nav.main-nav a:focus-visible{color:var(--gold-300);border-color:var(--gold-500);}
  nav.main-nav a[aria-current="page"]{color:var(--gold-300);border-color:var(--gold-500);}

  /* -------- Layout -------- */
  .page-wrap{
    max-width:1100px;margin:0 auto;padding:2.75rem 1.5rem 4rem;
    display:grid;grid-template-columns:1fr 300px;gap:2.5rem;
  }
  @media (max-width:800px){.page-wrap{grid-template-columns:1fr;}}

  main{display:flex;flex-direction:column;gap:1.75rem;min-width:0;}

  .section-label{
    text-transform:uppercase;letter-spacing:.12em;font-size:.75rem;
    color:var(--forest-700);font-weight:700;margin-bottom:.75rem;
    display:flex;align-items:center;gap:.6rem;
  }
  .section-label::after{content:"";flex:1;height:1px;background:var(--cream-200);}

  article.news-card{
    background:#fff;border-radius:var(--radius);overflow:hidden;
    display:grid;grid-template-columns:220px 1fr;gap:0;
    box-shadow:0 1px 2px rgba(12,33,27,.05), 0 8px 24px -16px rgba(12,33,27,.25);
    border:1px solid rgba(12,33,27,.06);
  }
  article.news-card img{width:100%;height:100%;object-fit:cover;min-height:160px;}
  .news-body{padding:1.4rem 1.5rem;display:flex;flex-direction:column;gap:.55rem;}
  .news-date{
    font-size:.78rem;color:var(--gold-500);font-weight:600;
    text-transform:uppercase;letter-spacing:.06em;
  }
  .news-date time{color:inherit;}
  article.news-card h2{font-size:1.32rem;font-weight:600;line-height:1.25;}
  article.news-card p.summary{font-size:.95rem;color:#3d453f;margin:0;}
  .read-more{
    align-self:flex-start;margin-top:.3rem;font-size:.88rem;font-weight:600;
    color:var(--forest-800);text-decoration:none;border-bottom:1px solid var(--gold-500);
    padding-bottom:1px;
  }
  .read-more:hover{color:var(--gold-500);}

  @media (max-width:640px){
    article.news-card{grid-template-columns:1fr;}
    article.news-card img{min-height:180px;}
  }

  /* -------- Aside -------- */
  aside{
    background:var(--forest-800);color:var(--cream-100);
    border-radius:var(--radius);padding:1.75rem 1.5rem;
    height:max-content;position:sticky;top:1.5rem;
  }
  aside h2{font-size:1.15rem;font-weight:600;margin-bottom:.4rem;}
  aside p{font-size:.88rem;color:var(--cream-200);opacity:.85;margin:0 0 1.2rem;}

  form.subscribe{display:flex;flex-direction:column;gap:.8rem;}
  form.subscribe label{font-size:.82rem;font-weight:600;color:var(--cream-200);}
  form.subscribe input[type="email"]{
    width:100%;padding:.65rem .8rem;border-radius:8px;border:1px solid rgba(233,224,204,.25);
    background:rgba(246,241,231,.06);color:var(--cream-100);font-size:.92rem;font-family:inherit;
  }
  form.subscribe input[type="email"]::placeholder{color:rgba(233,224,204,.45);}
  form.subscribe input[type="email"]:focus-visible,
  form.subscribe button:focus-visible,
  nav.main-nav a:focus-visible{outline:2px solid var(--gold-300);outline-offset:2px;}

  .checkbox-row{display:flex;align-items:flex-start;gap:.55rem;}
  .checkbox-row input[type="checkbox"]{margin-top:.2rem;accent-color:var(--gold-500);width:16px;height:16px;flex-shrink:0;}
  .checkbox-row label{font-size:.82rem;font-weight:400;color:var(--cream-200);opacity:.9;}

  form.subscribe button{
    margin-top:.3rem;padding:.75rem 1rem;border:none;border-radius:8px;
    background:var(--gold-500);color:var(--forest-900);font-weight:700;font-size:.92rem;
    cursor:pointer;transition:background .2s;font-family:inherit;
  }
  form.subscribe button:hover{background:var(--gold-300);}

  /* -------- Footer -------- */
  footer.site-footer{
    background:var(--forest-900);color:var(--cream-200);
    padding:2.25rem 1.5rem;
  }
  .footer-inner{
    max-width:1100px;margin:0 auto;display:flex;justify-content:space-between;
    flex-wrap:wrap;gap:1rem;font-size:.85rem;opacity:.75;
  }
  .footer-inner nav ul{list-style:none;display:flex;gap:1.25rem;padding:0;margin:0;}
  .footer-inner nav a{text-decoration:none;color:inherit;}
  .footer-inner nav a:hover{color:var(--gold-300);}
</style>
</head>
<body>

<header class="site-header">
  <div class="header-inner">
    <div class="brand">
      <span class="brand-mark" aria-hidden="true"></span>
      <div>
        <div class="brand-name">Ogooué Numérique</div>
        <div class="brand-tagline">Actualités tech &amp; université</div>
      </div>
    </div>
  </div>

  <div class="site-title">
    <h1>Ce qui se construit, se déploie, se lance.</h1>
    <p>Les nouvelles du numérique gabonais, article par article — campus, startups et projets publics.</p>
  </div>

  <svg class="river-divider" viewBox="0 0 1440 60" preserveAspectRatio="none" aria-hidden="true">
    <path d="M0,30 C 240,60 480,0 720,25 C 960,50 1200,10 1440,35 L1440,60 L0,60 Z" fill="#f6f1e7"></path>
  </svg>
</header>

<nav class="main-nav" aria-label="Navigation principale">
  <ul>
    <li><a href="#accueil" aria-current="page">Accueil</a></li>
    <li><a href="#universite">Université</a></li>
    <li><a href="#startups">Startups</a></li>
    <li><a href="#politiques">Politiques publiques</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="page-wrap">
  <main id="accueil">
    <p class="section-label">À la une</p>

    <article class="news-card">
      <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?w=500&auto=format&fit=crop&q=60" alt="Amphithéâtre universitaire moderne avec étudiants">
      <div class="news-body">
        <p class="news-date"><time datetime="2026-07-10">10 juillet 2026</time></p>
        <h2>L'UNG lance sa deuxième promotion de licence en cybersécurité</h2>
        <p class="summary">Cent-vingt étudiants rejoignent le nouveau cursus, conçu avec des partenaires régionaux pour répondre à la demande croissante en compétences numériques.</p>
        <a class="read-more" href="#">Lire l'article</a>
      </div>
    </article>

    <article class="news-card">
      <img src="https://images.unsplash.com/photo-1521737604893-d14cc237f11d?w=500&auto=format&fit=crop&q=60" alt="Équipe de jeunes entrepreneurs travaillant sur des ordinateurs portables">
      <div class="news-body">
        <p class="news-date"><time datetime="2026-07-06">6 juillet 2026</time></p>
        <h2>Une startup de Libreville remporte le prix francophone de l'agritech</h2>
        <p class="summary">L'application de suivi des cultures développée par une équipe locale a été distinguée lors du sommet francophone de l'innovation à Dakar.</p>
        <a class="read-more" href="#">Lire l'article</a>
      </div>
    </article>

    <article class="news-card">
      <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?w=500&auto=format&fit=crop&q=60" alt="Câbles et infrastructure réseau dans un centre de données">
      <div class="news-body">
        <p class="news-date"><time datetime="2026-06-28">28 juin 2026</time></p>
        <h2>Le Gabon annonce un nouveau centre de données national à Owendo</h2>
        <p class="summary">Le projet vise à réduire la dépendance à l'hébergement à l'étranger et à accélérer les services publics numériques d'ici 2028.</p>
        <a class="read-more" href="#">Lire l'article</a>
      </div>
    </article>
  </main>

  <aside aria-labelledby="newsletter-heading">
    <h2 id="newsletter-heading">Restez informé</h2>
    <p>Recevez les actualités du numérique gabonais chaque semaine, sans spam.</p>
    <form class="subscribe" action="#" method="post">
      <div>
        <label for="email">Adresse e-mail</label>
        <input type="email" id="email" name="email" placeholder="vous@exemple.com" required>
      </div>
      <div class="checkbox-row">
        <input type="checkbox" id="consent" name="consent" required>
        <label for="consent">J'accepte de recevoir la newsletter et j'ai lu la politique de confidentialité.</label>
      </div>
      <button type="submit">S'abonner</button>
    </form>
  </aside>
</div>

<footer class="site-footer">
  <div class="footer-inner">
    <span>© 2026 Ogooué Numérique — Université Numérique du Gabon</span>
    <nav aria-label="Liens de pied de page">
      <ul>
        <li><a href="#">Mentions légales</a></li>
        <li><a href="#">Confidentialité</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</footer>

</body>
</html>
