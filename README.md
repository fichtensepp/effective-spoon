<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Lorenscheid — Forst- und Gartendienst</title>
  <meta name="description" content="Lorenscheid Forst- und Gartendienst — Ihr Partner rund um Haus, Garten und Wald. Leistungen, Tipps & Tricks, Kontakt."/>
  <style>
    :root{
      --green-light: #9dd46b;
      --green-mid:   #6bb139;
      --green-dark:  #1e5f2a;
      --accent:      #18472a;
      --bg:          linear-gradient(180deg,var(--green-light), #7bc14a 40%, var(--green-mid) 80%, #2c7a30);
      --maxwidth: 1100px;
      --radius: 12px;
      --glass: rgba(255,255,255,0.06);
      --text: #052007;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "Helvetica Neue", Arial, sans-serif;
      color:var(--text);
      background: var(--bg);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    /* container */
    .wrap{
      max-width:var(--maxwidth);
      margin:0 auto;
      padding:20px;
    }

    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      padding:18px 10px;
      position:sticky;
      top:0;
      z-index:40;
      backdrop-filter: blur(6px);
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.00));
      border-bottom: 1px solid rgba(0,0,0,0.06);
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .logo{
      width:74px;
      height:74px;
      border-radius:50%;
      background: white;
      display:grid;
      place-items:center;
      box-shadow: 0 6px 18px rgba(0,0,0,0.12);
      flex-shrink:0;
    }
    .logo svg{width:62px;height:62px}
    .title{
      line-height:1;
    }
    .title h1{margin:0;font-size:18px;letter-spacing: -0.5px;}
    .title p{margin:0;font-size:12px;color:#083b1e;font-weight:600}

    nav ul{display:flex;gap:14px;list-style:none;margin:0;padding:0}
    nav a{
      text-decoration:none;
      color:var(--text);
      padding:8px 10px;
      border-radius:8px;
      font-weight:600;
      font-size:14px;
    }
    nav a:hover{background: rgba(255,255,255,0.06)}

    /* hero */
    .hero{
      display:grid;
      grid-template-columns: 1fr 320px;
      gap:20px;
      align-items:center;
      padding:36px 10px;
    }
    .hero-card{
      background: rgba(255,255,255,0.06);
      padding:24px;
      border-radius:16px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.12);
    }
    .hero h2{margin:0 0 8px;font-size:28px}
    .hero p.lead{margin:0 0 14px;color:#083b1e;font-weight:600}

    .cta-row{display:flex;gap:12px;flex-wrap:wrap}
    .btn{
      background:var(--accent);
      color:white;
      padding:10px 14px;
      border-radius:10px;
      text-decoration:none;
      display:inline-block;
      font-weight:700;
    }
    .btn.ghost{background:transparent;color:white;border:1px solid rgba(255,255,255,0.14)}

    .qr-box{
      background: rgba(255,255,255,0.04);
      border-radius:14px;
      padding:16px;
      text-align:center;
      display:flex;
      flex-direction:column;
      gap:10px;
      align-items:center;
    }
    .qr-box img{width:160px;height:160px;object-fit:contain;border-radius:10px;background:white;padding:6px}

    /* main sections */
    main{padding:18px 10px 80px}
    .sections{display:grid;gap:28px}

    .cards-grid{
      display:grid;
      grid-template-columns: repeat(4,1fr);
      gap:18px;
    }
    .card{
      background: rgba(255,255,255,0.04);
      padding:16px;
      border-radius:12px;
      min-height:180px;
    }
    .card h3{margin:0 0 8px;font-size:16px;color:white;background:var(--accent);display:inline-block;padding:6px 10px;border-radius:8px}
    .card ul{margin:12px 0 0;padding-left:18px;color:white}
    .card li{margin:8px 0;font-weight:600;font-size:14px}

    /* Tips & Tricks */
    .tips{
      background: rgba(255,255,255,0.03);
      padding:18px;border-radius:14px;
      display:grid;gap:12px;
    }
    .season-buttons{display:flex;gap:8px;flex-wrap:wrap}
    .season-btn{background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.06);padding:8px 10px;border-radius:8px;cursor:pointer;font-weight:700}
    .season-btn.active{background:white;color:var(--accent)}
    .season-content{padding:12px;border-radius:10px;background:rgba(0,0,0,0.03)}

    .tips-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:10px}
    .tip-card{background:rgba(255,255,255,0.02);padding:12px;border-radius:10px;min-height:120px}
    .tip-card h4{margin:0 0 8px}

    /* contact */
    .contact{
      display:grid;grid-template-columns:1fr 340px;gap:18px;align-items:start;
    }
    .contact-card{
      padding:18px;border-radius:12px;background:rgba(255,255,255,0.04);
    }
    .contact .bigphone{font-size:20px;font-weight:800;margin:6px 0}
    .contact-form input,.contact-form textarea{
      width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.08);margin-bottom:8px;font-size:14px
    }
    .contact-form button{padding:10px 12px;border-radius:8px;border:0;background:var(--accent);color:white;font-weight:800;cursor:pointer}

    footer{
      margin-top:28px;padding:18px;border-radius:12px;background:rgba(0,0,0,0.06);color:rgba(255,255,255,0.9);
      display:flex;justify-content:space-between;align-items:center;gap:10px;flex-wrap:wrap;
    }

    /* Forest silhouette bottom decoration */
    .forest-deco{
      position:fixed;left:0;right:0;bottom:0;height:140px;pointer-events:none;
      background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="1600" height="140" viewBox="0 0 1600 140"><g fill="%23143a18"><path d="M0 120 L30 70 L60 120 L90 50 L120 120 L150 60 L180 120 L210 30 L240 120 L270 80 L300 120 L330 50 L360 120 L390 90 L420 120 L450 40 L480 120 L510 70 L540 120 L570 90 L600 120 L630 70 L660 120 L690 60 L720 120 L750 80 L780 120 L810 50 L840 120 L870 90 L900 120 L930 60 L960 120 L990 80 L1020 120 L1050 50 L1080 120 L1110 70 L1140 120 L1170 90 L1200 120 L1230 30 L1260 120 L1290 70 L1320 120 L1350 50 L1380 120 L1410 80 L1440 120 L1470 60 L1500 120 L1530 90 L1560 120 L1600 120 L1600 140 L0 140 Z"/></g></svg>');
      background-repeat:repeat-x;
      background-position: bottom left;
      opacity:0.95;
      z-index:5;
    }

    /* responsive */
    @media (max-width:1024px){
      .cards-grid{grid-template-columns: repeat(2,1fr)}
      .hero{grid-template-columns:1fr 260px}
      .tips-grid{grid-template-columns:repeat(2,1fr)}
      .contact{grid-template-columns:1fr}
    }
    @media (max-width:640px){
      header{padding:12px}
      .hero{grid-template-columns:1fr;gap:12px}
      .cards-grid{grid-template-columns:1fr}
      .tips-grid{grid-template-columns:1fr}
      nav ul{display:none}
    }

  </style>
</head>
<body>
  <div class="forest-deco" aria-hidden="true"></div>

  <header class="wrap" role="banner">
    <div class="brand">
      <div class="logo" aria-hidden="true">
        <!-- Placeholder circular logo - replace with your logo.svg -->
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <circle cx="50" cy="50" r="48" fill="#ffffff"/>
          <g transform="translate(12,12)" fill="#1e5f2a">
            <path d="M12 34 L22 6 L28 34 Z"/>
            <path d="M34 40 L46 8 L52 40 Z"/>
            <path d="M2 44 L18 12 L32 44 Z"/>
          </g>
        </svg>
      </div>
      <div class="title">
        <h1>Lorenscheid</h1>
        <p>Forst- und Gartendienst — Ihr Partner rund um Haus, Garten und Wald</p>
      </div>
    </div>

    <nav aria-label="Hauptnavigation">
      <ul>
        <li><a href="#leistungen">Leistungen</a></li>
        <li><a href="#tipps">Tipps &amp; Tricks</a></li>
        <li><a href="#kontakt">Kontakt</a></li>
      </ul>
    </nav>
  </header>

  <main class="wrap" role="main">
    <section class="hero">
      <div class="hero-card">
        <h2>Da wo Gartenpflege auf Baumkonzept trifft</h2>
        <p class="lead">Seit 2024 — Nachhaltige Pflege für Garten & Wald. Vertrauen, Kompetenz und Naturverbundenheit.</p>
        <p>Wir arbeiten naturnah, praktisch und transparent. Auf Wunsch beraten wir gerne persönlich vor Ort.</p>
        <div class="cta-row" style="margin-top:12px">
          <a class="btn" href="#kontakt">Jetzt Kontakt</a>
          <a class="btn ghost" href="#tipps">Tipps &amp; Tricks</a>
          <a class="btn ghost" href="images/flyer-front.jpg" target="_blank" rel="noopener">Flyer ansehen</a>
        </div>
      </div>

      <aside class="qr-box" aria-label="QR-Code">
        <!-- Replace src with your QR image or keep as placeholder -->
        <img src="images/qr.png" alt="QR-Code zu Kontakt / Webseite (bitte images/qr.png ersetzen)">
        <div style="font-weight:800;color:white">Nicht fündig geworden?</div>
        <div style="font-size:13px;color:#edf9ec">Wir finden Ihre Lösung — scannen Sie den QR-Code oder rufen Sie an.</div>
      </aside>
    </section>

    <section id="leistungen" class="sections">
      <h2 style="margin:0 0 6px">Leistungen</h2>
      <p style="margin:0 0 10px">Alle Leistungen wie auf dem Flyer — übersichtlich gruppiert.</p>

      <div class="cards-grid" aria-hidden="false">
        <!-- Garten -->
        <div class="card" aria-labelledby="garten-title">
          <h3 id="garten-title">Garten</h3>
          <ul>
            <li>Heckenschnitt</li>
            <li>Baumkronenrückschnitt / Kronensicherung</li>
            <li>Rasenmähen</li>
            <li>Beet-Service – neu anlegen</li>
            <li>Unkrautentfernung &amp; Unkraut-Jäten</li>
            <li>Vertikutieren</li>
            <li>Wegebau &amp; Pflasterarbeiten</li>
            <li>Fundament- und Betonarbeiten (inkl. Baggerarbeiten)</li>
            <li>Beratung und Unterstützung</li>
          </ul>
        </div>

        <!-- Wald -->
        <div class="card" aria-labelledby="wald-title">
          <h3 id="wald-title">Wald</h3>
          <ul>
            <li>Fällungen</li>
            <li>Rodung</li>
            <li>Waldwegebau</li>
            <li>Pflanzung</li>
            <li>Jungbestandspflege</li>
            <li>Mäharbeiten</li>
            <li>Mulcharbeiten / Forstmulchen / Schlegelmulchen</li>
            <li>Lichtraumprofil &amp; Rückearbeiten</li>
            <li>Problembaumfällungen</li>
            <li>Entwässerungsgraben-Reinigung</li>
          </ul>
        </div>

        <!-- Vermietung -->
        <div class="card" aria-labelledby="vermietung-title">
          <h3 id="vermietung-title">Vermietung</h3>
          <ul>
            <li><strong>Sägen:</strong> (z. B. Stihl MS-Modelle)</li>
            <li><strong>Heckenscheren:</strong> Stihl HS-/HL Serien (gäbe es vor Ort)</li>
            <li><strong>Steinsäge &amp; Pflastersäge:</strong> z. B. Stihl TS-800</li>
            <li><strong>Rüttelplatte + Gummi</strong></li>
            <li><strong>Rüttel- / Verdichtungsgeräte</strong></li>
            <li><strong>Stabentaster manuell</strong> – bis ca. 13 m Reichweite</li>
            <li>Weitere Geräte auf Anfrage</li>
          </ul>
        </div>

        <!-- Sonstiges -->
        <div class="card" aria-labelledby="sonstiges-title">
          <h3 id="sonstiges-title">Sonstiges</h3>
          <ul>
            <li>Anlegen von Blumenbeeten und Kräuterbeeten</li>
            <li>Blühwiesen &amp; Bienenwiesen anlegen</li>
            <li>Teich- &amp; Wasseranlagen</li>
            <li>Naturgarten-Gestaltung mit natürlichen Sitzplätzen</li>
            <li>Blühwiesen als Lebensräume – helfen Sie Bienen &amp; Schmetterlingen</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="tipps" style="margin-top:24px">
      <h2>Tipps &amp; Tricks — Hilfe zum Selbermachen</h2>
      <p>Praktische Anleitungen für jede Jahreszeit. Der Kunde soll sich informiert fühlen — nicht zum Kontakt gezwungen.</p>

      <div class="tips">
        <div class="season-buttons" role="tablist" aria-label="Jahreszeiten">
          <button class="season-btn active" data-season="spring" role="tab">Frühling</button>
          <button class="season-btn" data-season="summer" role="tab">Sommer</button>
          <button class="season-btn" data-season="autumn" role="tab">Herbst</button>
          <button class="season-btn" data-season="winter" role="tab">Winter</button>
        </div>

        <div id="seasonArea" class="season-content" role="tabpanel" aria-live="polite">
          <!-- default: spring content -->
          <div data-season-content="spring">
            <h3>Frühling — was jetzt wichtig ist</h3>
            <div class="tips-grid">
              <div class="tip-card">
                <h4>Rasen</h4>
                <p>Vertikutieren (leichter), kahle Stellen nachsäen, im zeitigen Frühjahr erst höher mähen; später nach und nach kürzer schneiden. Erste Düngung sparsam.</p>
              </div>
              <div class="tip-card">
                <h4>Hecken &amp; Sträucher</h4>
                <p>Form- und Erhaltungsschnitt kurz vor oder nach dem Austrieb; starke Rückschnitte nur außerhalb der Brutzeit planen (Vögel beachten).</p>
              </div>
              <div class="tip-card">
                <h4>Beete &amp; Pflanzen</h4>
                <p>Boden lockern und mit Kompost versorgen, Stauden teilen, frostempfindliche Pflanzen nach letzten Frösten einsetzen.</p>
              </div>
            </div>
          </div>

          <div data-season-content="summer" style="display:none">
            <h3>Sommer — Pflege bei Hitze</h3>
            <div class="tips-grid">
              <div class="tip-card">
                <h4>Gießen</h4>
                <p>Tief und seltener gießen (morgens) statt häufiger Kurz-Bewässerung; fördert tiefere Wurzeln und Trockenresistenz.</p>
              </div>
              <div class="tip-card">
                <h4>Rasen</h4>
                <p>Rasen möglichst nicht zu kurz schneiden (lässt Boden weniger austrocknen). Bei Trockenheit längere Schnitte und Mulch einsetzen.</p>
              </div>
              <div class="tip-card">
                <h4>Schädlings-Check</h4>
                <p>Regelmäßig kontrollieren, befallene Blätter entfernen, Nützlinge (Insektenhotel, blühende Randstreifen) fördern.</p>
              </div>
            </div>
          </div>

          <div data-season-content="autumn" style="display:none">
            <h3>Herbst — Vorbereitung auf den Winter</h3>
            <div class="tips-grid">
              <div class="tip-card">
                <h4>Laub &amp; Mulch</h4>
                <p>Laub nicht sofort entsorgen: als Mulch oder Kompost nutzen. Laub im Rasen ggf. zusammenrechen, Stauden mit Mulch schützen.</p>
              </div>
              <div class="tip-card">
                <h4>Pflanzen &amp; Setzlinge</h4>
                <p>Herbst ist Pflanzzeit für Hecken und Gehölze — ausreichend wässern und gut anfrieren lassen.</p>
              </div>
              <div class="tip-card">
                <h4>Rasenpflege</h4>
                <p>Letzter, etwas niedrigere Schnitt, Herbstdüngung hilft dem Rasen durch den Winter.</p>
              </div>
            </div>
          </div>

          <div data-season-content="winter" style="display:none">
            <h3>Winter — Ruhe &amp; Vorbereitung</h3>
            <div class="tips-grid">
              <div class="tip-card">
                <h4>Gerätepflege</h4>
                <p>Motorsägen, Heckenscheren &amp; Geräte reinigen, Öl &amp; Filter prüfen — so sind sie im Frühjahr einsatzbereit.</p>
              </div>
              <div class="tip-card">
                <h4>Schnitt</h4>
                <p>Form- und Aufbauschnitte an Obstbäumen und Gehölzen in der Ruheperiode durchführen (geeignete Tage wählen).</p>
              </div>
              <div class="tip-card">
                <h4>Natur &amp; Tiere</h4>
                <p>Vogelfütterung planen, Rückzugszonen für Igel &amp; Kleintiere lassen — ein naturnaher Garten hilft Arten über den Winter.</p>
              </div>
            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="kontakt" style="margin-top:24px">
      <h2>Kontakt</h2>
      <div class="contact">
        <div class="contact-card">
          <strong>Kevin Lorenscheid</strong><br>
          <div class="bigphone">Telefon: <a href="tel:+491733127779">0173 3127 779</a></div>
          <div>E-Mail: <a href="mailto:fg-dienstleistung@gmx.net">fg-dienstleistung@gmx.net</a></div>
          <div style="margin-top:8px">Standort: Im Herzen Oberschwabens — Ostrach</div>
          <p style="margin-top:12px">Nicht fündig geworden? Scannen Sie den QR-Code im Header oder kontaktieren Sie mich — ich finde Ihre Lösung.</p>
          <p style="font-style:italic;color:#063514;font-weight:700">Wir arbeiten nachhaltig: Natur schützen, nicht nur pflegen.</p>
        </div>

        <aside class="contact-card" aria-labelledby="form-title">
          <h3 id="form-title">Kurze Nachricht senden</h3>
          <form class="contact-form" onsubmit="sendMail(event)">
            <input id="name" placeholder="Ihr Name" required />
            <input id="email" type="email" placeholder="Ihre E-Mail" required />
            <textarea id="message" rows="5" placeholder="Kurz beschreiben, worum es geht..." required></textarea>
            <button type="submit">E-Mail öffnen &amp; senden</button>
            <p style="font-size:12px;margin-top:8px;color:#083b1e">Das Formular öffnet Ihr E-Mailprogramm (kein Server nötig). Alternativ: an <a href="mailto:fg-dienstleistung@gmx.net">fg-dienstleistung@gmx.net</a> schreiben.</p>
          </form>
        </aside>
      </div>
    </section>

    <footer class="wrap">
      <div>Seit 2024 — Lorenscheid Forst- &amp; Gartendienst</div>
      <div style="opacity:0.95">Impressum / Datenschutz &middot; Standort: Ostrach</div>
    </footer>
  </main>

  <script>
    // Saison-Tab-Logik
    const seasonBtns = document.querySelectorAll('.season-btn');
    const seasonArea = document.getElementById('seasonArea');

    seasonBtns.forEach(btn=>{
      btn.addEventListener('click', ()=>{
        seasonBtns.forEach(b=>b.classList.remove('active'));
        btn.classList.add('active');
        const season = btn.dataset.season;
        // hide all season contents and show selected
        const all = seasonArea.querySelectorAll('[data-season-content]');
        all.forEach(node=>{
          node.style.display = node.getAttribute('data-season-content') === season ? '' : 'none';
        });
      });
    });

    // Kontaktformular via mailto (öffnet Mailclient)
    function sendMail(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      const subject = encodeURIComponent('Anfrage über Webseite — ' + name);
      const body = encodeURIComponent(
        'Name: ' + name + '\\n' +
        'E-Mail: ' + email + '\\n\\n' +
        message
      );
      window.location.href = 'mailto:fg-dienstleistung@gmx.net?subject=' + subject + '&body=' + body;
    }
  </script>
</body>
</html>
