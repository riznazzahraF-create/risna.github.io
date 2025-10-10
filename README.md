<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portofolio Isna</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Rubik:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: "Poppins", sans-serif;
      transition: all 0.6s ease-in-out;
    }

    header {
      text-align: center;
      padding: 3rem 1rem 2rem;
    }

    header h1 {
      font-size: 2.8rem;
      font-weight: 700;
      margin-bottom: 0.3rem;
      letter-spacing: 1px;
    }

    header p {
      font-size: 1.1rem;
      opacity: 0.9;
    }

    section {
      padding: 3rem 2rem;
      max-width: 900px;
      margin: auto;
      text-align: center;
    }

    .card {
      margin: 1.5rem auto;
      padding: 2rem;
      border-radius: 16px;
      transition: all 0.4s ease;
      width: 85%;
    }

    .card:hover {
      transform: translateY(-8px);
    }

    .btn {
      display: inline-block;
      margin-top: 1.5rem;
      padding: 0.8rem 1.6rem;
      border-radius: 12px;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s;
    }

    .btn:hover {
      transform: scale(1.05);
    }

    footer {
      text-align: center;
      padding: 2rem;
      font-size: 0.9rem;
      letter-spacing: 0.3px;
    }

    /* 🌙 DARK FUTURISTIC MODE */
    body.dark {
      background: radial-gradient(circle at top left, #0f172a, #1e293b);
      color: #e2e8f0;
    }

    .dark header h1 { color: #38bdf8; }
    .dark .card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255,255,255,0.1);
      box-shadow: 0 0 25px rgba(56,189,248,0.15);
      backdrop-filter: blur(12px);
    }
    .dark .btn {
      background: #38bdf8;
      color: #0f172a;
    }

    /* ☀️ BRIGHT MODERN STUDENT MODE */
    body.bright {
      background: linear-gradient(180deg, #f9fafb, #e0f2fe);
      color: #1e293b;
      font-family: "Rubik", sans-serif;
    }

    .bright header h1 { color: #3b82f6; }
    .bright .card {
      background: #ffffff;
      border: 2px solid #dbeafe;
      box-shadow: 0 6px 24px rgba(0,0,0,0.06);
    }
    .bright .btn {
      background: #3b82f6;
      color: #fff;
    }

    /* 🌟 Switcher Button */
    .switcher {
      position: fixed;
      bottom: 1.5rem;
      right: 1.5rem;
      background: #ffffff;
      color: #000;
      border: none;
      border-radius: 50%;
      width: 55px;
      height: 55px;
      font-size: 1.4rem;
      cursor: pointer;
      box-shadow: 0 4px 15px rgba(0,0,0,0.25);
      transition: all 0.3s;
      z-index: 999;
    }

    .switcher:hover {
      transform: scale(1.1);
    }

    /* ✨ Simple Fade Animation */
    .fade-in {
      animation: fadeIn 1.2s ease forwards;
      opacity: 0;
    }

    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>

<body class="dark" id="theme">
  <header class="fade-in">
    <h1>Hai, Saya Isna 👋</h1>
    <p>Pelajar yang senang belajar coding, desain, dan membuat hal keren dari ide sederhana.</p>
  </header>

  <section class="fade-in" style="animation-delay: 0.3s;">
    <h2>💡 Tentang Saya</h2>
    <div class="card">
      <p>Saya seorang pelajar yang tertarik pada dunia teknologi, terutama di bidang web development dan desain digital.  
      Saya percaya bahwa belajar tidak harus rumit — cukup konsisten dan nikmati prosesnya.</p>
    </div>
  </section>

  <section class="fade-in" style="animation-delay: 0.6s;">
    <h2>🚀 Proyek Saya</h2>
    <div class="card">
      <p>🌐 <b>Website Portfolio</b> — Menampilkan perjalanan dan hasil karya saya di dunia pemrograman.</p>
    </div>
    <div class="card">
      <p>🎮 <b>Mini Game Edukatif</b> — Game sederhana berbasis JavaScript untuk melatih logika dan konsentrasi.</p>
    </div>
    <a href="#" class="btn">Lihat Semua Proyek</a>
  </section>

  <section class="fade-in" style="animation-delay: 0.9s;">
    <h2>🎯 Tujuan Saya</h2>
    <div class="card">
      <p>Menjadi developer kreatif yang bisa menggabungkan logika, desain, dan keindahan dalam setiap proyek yang saya buat. 🌟</p>
    </div>
  </section>

  <footer class="fade-in" style="animation-delay: 1.2s;">
    <p>© 2025 Isna | Dibuat dengan 💙, semangat belajar, dan secangkir kopi ☕</p>
  </footer>

  <button class="switcher" onclick="switchTheme()">🌓</button>

  <script>
    // Fungsi untuk ganti tema Dark <-> Bright
    const theme = document.getElementById('theme');
    function switchTheme() {
      if (theme.classList.contains('dark')) {
        theme.classList.remove('dark');
        theme.classList.add('bright');
      } else {
        theme.classList.remove('bright');
        theme.classList.add('dark');
      }
    }

    // Animasi fade saat scroll
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('fade-in');
        }
      });
    });

    document.querySelectorAll('section, footer').forEach(el => observer.observe(el));
  </script>
</body>
</html>
