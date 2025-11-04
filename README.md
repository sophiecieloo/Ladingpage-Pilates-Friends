<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pilates & Friends – Online Pilates Plattform</title>
  <style>
    :root {
      --primary-blue: #004c85;
      --accent-pink: #ff6f61;
      --light-blue: #ffebc2;
      --background-gray: #f9fafb;
      --white: #fff;
      --text-gray: #444;
      --footer-gray: #666;
      --stars-yellow: #ffc107;
      --cookie-black: rgba(0, 0, 0, 0.8);
      --gradient-bg: linear-gradient(135deg, #f9fafb 0%, #e0f7fa 100%);
    }
    body {
      font-family: 'Helvetica Neue', sans-serif;
      margin: 0;
      background: var(--gradient-bg);
      color: #222;
      animation: fadeIn 1s ease-in;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    header {
      background-color: var(--light-blue);
      text-align: center;
      padding: 3rem 1rem;
      border-radius: 0 0 30px 30px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      position: relative;
    }
    header::after {
      content: '';
      position: absolute;
      bottom: -20px;
      left: 50%;
      transform: translateX(-50%);
      width: 0;
      height: 0;
      border-left: 20px solid transparent;
      border-right: 20px solid transparent;
      border-top: 20px solid var(--light-blue);
    }
    header h1 {
      font-size: 2.5rem;
      color: var(--primary-blue);
      margin-bottom: 0.5rem;
      font-weight: 700;
    }
    header p {
      font-size: 1.2rem;
      color: #333;
    }
    .hero {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 3rem 2rem;
      gap: 2rem;
      position: relative;
    }
    .hero img {
      width: 90%;
      max-width: 800px;
      border-radius: 25px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      transition: transform 0.3s ease;
    }
    .hero img:hover {
      transform: scale(1.05);
    }
    .hero::before {
      content: '🧘‍♀️';
      position: absolute;
      top: 10%;
      left: 10%;
      font-size: 3rem;
      opacity: 0.3;
      animation: float 3s ease-in-out infinite;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    .content {
      text-align: center;
      padding: 3rem 2rem;
      background-color: var(--white);
      border-radius: 30px;
      margin: 2rem auto;
      max-width: 1000px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      position: relative;
    }
    .content::after {
      content: '💪';
      position: absolute;
      top: -15px;
      right: 20px;
      font-size: 2rem;
      opacity: 0.5;
    }
    .content h2 {
      color: var(--primary-blue);
      font-size: 2.2rem;
      margin-bottom: 1.5rem;
      font-weight: 600;
    }
    .content p {
      font-size: 1.2rem;
      line-height: 1.8;
      color: var(--text-gray);
      margin-bottom: 1rem;
    }
    .cta-button {
      background: linear-gradient(45deg, var(--accent-pink), #ff8a80);
      color: var(--white);
      padding: 1.2rem 2.5rem;
      border: none;
      border-radius: 35px;
      font-size: 1.3rem;
      cursor: pointer;
      transition: all 0.3s ease;
      text-decoration: none;
      display: inline-block;
      margin-top: 2rem;
      box-shadow: 0 5px 15px rgba(255, 111, 97, 0.3);
    }
    .cta-button:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 20px rgba(255, 111, 97, 0.4);
    }
    .reviews {
      background-color: var(--white);
      padding: 3rem 2rem;
      margin: 3rem auto;
      max-width: 1000px;
      border-radius: 30px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      text-align: center;
      position: relative;
    }
    .reviews::before {
      content: '⭐';
      position: absolute;
      top: -10px;
      left: 20px;
      font-size: 2rem;
      opacity: 0.5;
    }
    .reviews h3 {
      color: var(--primary-blue);
      font-size: 2rem;
      margin-bottom: 2rem;
      font-weight: 600;
    }
    .review {
      margin-bottom: 2rem;
      font-style: italic;
      padding: 1rem;
      background: rgba(255, 235, 194, 0.2);
      border-radius: 15px;
      transition: background 0.3s ease;
    }
    .review:hover {
      background: rgba(255, 235, 194, 0.4);
    }
    .stars {
      color: var(--stars-yellow);
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }
    .faq {
      background-color: var(--white);
      padding: 3rem 2rem;
      margin: 3rem auto;
      max-width: 1000px;
      border-radius: 30px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      text-align: left;
      position: relative;
    }
    .faq::before {
      content: '❓';
      position: absolute;
      top: -10px;
      left: 20px;
      font-size: 2rem;
      opacity: 0.5;
    }
    .faq h3 {
      color: var(--primary-blue);
      font-size: 2rem;
      margin-bottom: 2rem;
      font-weight: 600;
      text-align: center;
    }
    .faq details {
      margin-bottom: 1.5rem;
      border: 1px solid rgba(0, 76, 133, 0.2);
      border-radius: 15px;
      padding: 1rem;
      background: rgba(255, 235, 194, 0.1);
      transition: background 0.3s ease;
    }
    .faq details:hover {
      background: rgba(255, 235, 194, 0.3);
    }
    .faq summary {
      font-weight: 600;
      color: var(--primary-blue);
      cursor: pointer;
      font-size: 1.2rem;
    }
    .faq summary::marker {
      color: var(--accent-pink);
    }
    .faq p {
      margin-top: 0.5rem;
      color: var(--text-gray);
      line-height: 1.6;
    }
    footer {
      text-align: center;
      padding: 3rem 2rem;
      font-size: 1rem;
      color: var(--footer-gray);
      background: var(--gradient-bg);
      border-radius: 30px 30px 0 0;
    }
    .cookie-banner {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      background: var(--cookie-black);
      color: var(--white);
      padding: 1.5rem;
      text-align: center;
      font-size: 1rem;
      border-radius: 20px 20px 0 0;
    }
    .cookie-banner button {
      background: var(--accent-pink);
      border: none;
      color: var(--white);
      padding: 0.7rem 1.5rem;
      border-radius: 25px;
      margin-left: 1rem;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .cookie-banner button:hover {
      background: #ff4a3d;
    }
  </style>
  <!-- Meta Pixel Code -->
  <script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', '1351510266720040');
  fbq('track', 'PageView');
  </script>
  <noscript><img height="1" width="1" style="display:none"
  src="https://www.facebook.com/tr?id=1351510266720040&ev=PageView&noscript=1"/></noscript>
</head>
<body>
  <header>
    <h1>Pilates & Friends – Deine Online Pilates Plattform</h1>
    <p>Über 1.300 Videos mit Top-Trainer*innen. Trainiere wann und wo du willst – <strong>der erste Monat kostet nur 1 €!</strong></p>
  </header>

  <section class="hero">
    <img src="https://www.pilatesandfriends.com/sites/default/files/styles/wide/public/2022-11/Headerbild%20Startseite.jpg?itok=lB7ebDvf" alt="Pilates für Schwangere">
    <img src="https://pilatesandfriends.com/sites/default/files/styles/1260x720/public/2024-01/WhatsApp%20Image%202024-01-28%20at%2011.54.30%20%282%29.webp?h=ef2175f4&itok=gRmHELej" alt="Wohlbefinden und Fitness">
    <img src="https://pilatesandfriends.com/sites/default/files/styles/1260x720/public/2023-11/Rundr%C3%BCcken%20%282%29.webp?h=6fb9eaa3&itok=cgeerOcB" alt="Pilates Training und Balance">
  </section>

  <section class="content">
    <h2>Erlebe Pilates & Friends</h2>
    <p>Ob zu Hause, unterwegs oder im Studio – mit <strong>Pilates & Friends</strong> hast du Zugang zu mehr als <strong>1.300 professionell produzierten Videos</strong> in den Bereichen Pilates, Yoga, Tanz und Faszien-Training. Egal ob du Einsteiger*in bist, schwanger, dich in der Rückbildung befindest oder deine Technik verfeinern willst – hier findest du dein perfektes Programm.</p>
    <p>Mit erfahrenen Trainer*innen, flexiblen Programmen und neuen Kursen jede Woche bleibst du motiviert und erreichst deine Ziele – Schritt für Schritt.</p>
    <a href="https://www.pilatesandfriends.com#aff=edsiane&cam=Site-Pixel&utm_source=meta&utm_medium=cpc&utm_campaign=landing_aff" class="cta-button" onclick="fbq('track', 'Lead');">Jetzt testen – 1. Monat nur 1 €!</a>
  </section>

  <section class="reviews">
    <h3>Was unsere Mitglieder sagen</h3>
    <div class="review">
      <div class="stars">★★★★★</div>
      <p>„Ich trainiere seit Monaten mit Pilates & Friends und liebe die Vielfalt der Kurse!“ – <strong>Anna K.</strong></p>
    </div>
    <div class="review">
      <div class="stars">★★★★★</div>
      <p>„Perfekt für meine Rückbildung nach der Schwangerschaft. Super Trainerinnen!“ – <strong>Julia W.</strong></p>
    </div>
    <div class="review">
      <div class="stars">★★★★★</div>
      <p>„Ich kann trainieren, wann immer ich will – das ist genau, was ich brauche!“ – <strong>Lisa F.</strong></p>
    </div>
  </section>

  <section class="faq">
    <h3>Häufig gestellte Fragen (FAQ)</h3>
    <details>
      <summary>Wie viel kostet die Mitgliedschaft?</summary>
      <p>Der erste Monat kostet nur 1 €. Danach beträgt der monatliche Preis 29,90 €. Du kannst jederzeit kündigen.</p>
    </details>
    <details>
      <summary>Kann ich die Videos offline ansehen?</summary>
      <p>Ja, viele Videos können heruntergeladen werden, um offline zu trainieren. Du brauchst nur eine stabile Internetverbindung für den Download.</p>
    </details>
    <details>
      <summary>Gibt es Kurse für Anfänger*innen?</summary>
      <p>Absolut! Unsere Plattform bietet Kurse für alle Levels, von Einsteiger*innen bis Fortgeschrittene. Wähle einfach dein Niveau aus.</p>
    </details>
    <details>
      <summary>Wie kann ich meine Mitgliedschaft kündigen?</summary>
      <p>Du kannst jederzeit in deinem Konto kündigen. Es gibt keine Bindung – einfach und unkompliziert.</p>
    </details>
    <details>
      <summary>Brauche ich spezielle Ausrüstung?</summary>
      <p>Nein, die meisten Übungen können mit deinem Körpergewicht durchgeführt werden. Eine Matte ist empfehlenswert, aber nicht zwingend erforderlich.</p>
    </details>
  </section>

  <footer>
    <p>© 2025 Pilates & Friends – Alle Rechte vorbehalten.</p>
  </footer>

  <div class="cookie-banner" id="cookie-banner">
    Diese Website verwendet Cookies, um Ihr Erlebnis zu verbessern.
    <button onclick="acceptCookies()">Akzeptieren</button>
  </div>
  <script>
    function acceptCookies() {
      document.getElementById('cookie-banner').style.display = 'none';
      localStorage.setItem('cookiesAccepted', 'true');
    }
    if(localStorage.getItem('cookiesAccepted')) {
      document.getElementById('cookie-banner').style.display = 'none';
    }
  </script>
</body>
</html>

