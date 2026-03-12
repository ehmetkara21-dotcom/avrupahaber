[avrupahaber 2.html](https://github.com/user-attachments/files/25941213/avrupahaber.2.html)
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AvrupaHaber — Avrupa'nın Sesi</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=Source+Serif+4:ital,wght@0,300;0,400;1,300&family=Barlow:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #f5f2eb;
  --white: #ffffff;
  --dark: #0a0a0a;
  --red: #c0181e;
  --red2: #e8222a;
  --muted: #666;
  --border: #d4cfc5;
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  background: var(--bg);
  color: var(--dark);
  font-family: 'Barlow', sans-serif;
  overflow-x: hidden;
}

::-webkit-scrollbar { width: 3px; }
::-webkit-scrollbar-thumb { background: var(--red); }

/* TOP BAR */
.topbar {
  background: var(--dark);
  color: #aaa;
  padding: 7px 48px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.68rem;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

.topbar .breaking { color: var(--red); font-weight: 700; }

/* TICKER */
.ticker {
  background: var(--red);
  color: white;
  padding: 7px 0;
  overflow: hidden;
}

.ticker-inner {
  display: flex;
  white-space: nowrap;
  animation: tick 35s linear infinite;
}

@keyframes tick {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

.ticker-item {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 0 36px;
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

/* NAV */
nav {
  background: var(--white);
  border-bottom: 3px solid var(--dark);
  padding: 0 48px;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 20px rgba(0,0,0,0.08);
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 0;
  border-bottom: 1px solid var(--border);
}

.logo-wrap { text-decoration: none; cursor: pointer; }

.logo-top {
  font-size: 0.55rem;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: var(--red);
  font-weight: 700;
  display: block;
  margin-bottom: 2px;
}

.logo-main {
  font-family: 'Playfair Display', serif;
  font-size: 2.2rem;
  font-weight: 900;
  color: var(--dark);
  line-height: 1;
  display: block;
}

.logo-main span { color: var(--red); }

.logo-bottom {
  font-family: 'Source Serif 4', serif;
  font-size: 0.72rem;
  font-style: italic;
  color: var(--muted);
  display: block;
  margin-top: 2px;
}

.nav-right {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 8px;
}

.nav-right .edition {
  font-size: 0.65rem;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--muted);
}

.search-btn {
  background: var(--red);
  color: white;
  border: none;
  padding: 8px 20px;
  font-family: 'Barlow', sans-serif;
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  cursor: pointer;
  transition: background 0.2s;
}

.search-btn:hover { background: var(--red2); }

.nav-menu {
  display: flex;
  list-style: none;
}

.nav-menu li a {
  display: block;
  padding: 12px 18px;
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--dark);
  text-decoration: none;
  border-bottom: 3px solid transparent;
  transition: all 0.2s;
  margin-bottom: -3px;
}

.nav-menu li a:hover, .nav-menu li a.active {
  color: var(--red);
  border-bottom-color: var(--red);
}

/* HERO */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 48px;
}

.hero-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 32px;
  padding: 32px 0;
}

.hero-main { cursor: pointer; }

.hero-main img {
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
  display: block;
  transition: filter 0.3s;
}

.hero-main:hover img { filter: brightness(1.05); }

.hero-cat {
  display: inline-block;
  background: var(--red);
  color: white;
  font-size: 0.6rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 5px 12px;
  margin: 16px 0 10px;
}

.hero-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.6rem, 3vw, 2.4rem);
  font-weight: 900;
  line-height: 1.15;
  margin-bottom: 12px;
  transition: color 0.2s;
}

.hero-main:hover .hero-title { color: var(--red); }

.hero-desc {
  font-family: 'Source Serif 4', serif;
  font-size: 1rem;
  line-height: 1.7;
  color: #444;
  margin-bottom: 14px;
}

.hero-meta {
  font-size: 0.72rem;
  color: var(--muted);
  display: flex;
  gap: 16px;
}

.hero-meta .author { font-weight: 600; color: var(--dark); }
.hero-meta .time { color: var(--red); }

/* SIDE STORIES */
.hero-side {
  border-left: 1px solid var(--border);
  padding-left: 32px;
  display: flex;
  flex-direction: column;
}

.side-story {
  padding: 18px 0;
  border-bottom: 1px solid var(--border);
  cursor: pointer;
}

.side-story:first-child { padding-top: 0; }
.side-story:last-child { border-bottom: none; padding-bottom: 0; }

.side-story img {
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
  margin-bottom: 10px;
  transition: filter 0.3s;
}

.side-story:hover img { filter: brightness(1.05); }

.side-cat {
  font-size: 0.58rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--red);
  margin-bottom: 6px;
}

.side-title {
  font-family: 'Playfair Display', serif;
  font-size: 1rem;
  font-weight: 700;
  line-height: 1.3;
  margin-bottom: 6px;
  transition: color 0.2s;
}

.side-story:hover .side-title { color: var(--red); }

.side-meta { font-size: 0.68rem; color: var(--muted); }

/* SECTION DIVIDER */
.sec-div {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 28px 0 24px;
}

.sec-div-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.1rem;
  font-weight: 900;
  white-space: nowrap;
}

.sec-div-title span { color: var(--red); }

.sec-div-line { flex: 1; height: 2px; background: var(--border); }

.sec-div-link {
  font-size: 0.65rem;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--red);
  text-decoration: none;
  font-weight: 600;
  white-space: nowrap;
}

/* NEWS GRID */
.news-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
  padding-bottom: 48px;
}

.news-card { cursor: pointer; }

.news-card img {
  width: 100%;
  aspect-ratio: 3/2;
  object-fit: cover;
  display: block;
  margin-bottom: 14px;
  transition: filter 0.3s;
}

.news-card:hover img { filter: brightness(1.05); }

.news-cat {
  font-size: 0.58rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--red);
  margin-bottom: 7px;
}

.news-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.1rem;
  font-weight: 700;
  line-height: 1.35;
  margin-bottom: 8px;
  transition: color 0.2s;
}

.news-card:hover .news-title { color: var(--red); }

.news-desc {
  font-family: 'Source Serif 4', serif;
  font-size: 0.88rem;
  line-height: 1.65;
  color: #555;
  margin-bottom: 10px;
}

.news-meta {
  font-size: 0.68rem;
  color: var(--muted);
  display: flex;
  gap: 12px;
}

.news-meta .author { font-weight: 600; color: var(--dark); }

/* OPINION */
.opinion-section {
  background: var(--dark);
  padding: 48px 0;
  margin-bottom: 0;
}

.opinion-head {
  display: flex;
  align-items: center;
  gap: 16px;
  margin-bottom: 32px;
}

.opinion-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.4rem;
  font-weight: 900;
  color: white;
  white-space: nowrap;
}

.opinion-title span { color: var(--red); font-style: italic; }
.opinion-line { flex: 1; height: 1px; background: rgba(255,255,255,0.15); }

.opinion-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.opinion-card {
  border-left: 3px solid var(--red);
  padding-left: 20px;
  cursor: pointer;
}

.opinion-big-quote {
  font-family: 'Playfair Display', serif;
  font-size: 4rem;
  color: rgba(255,255,255,0.08);
  line-height: 1;
  margin-bottom: -10px;
}

.opinion-card-title {
  font-family: 'Playfair Display', serif;
  font-size: 1rem;
  font-weight: 700;
  color: white;
  line-height: 1.4;
  margin-bottom: 12px;
  transition: color 0.2s;
}

.opinion-card:hover .opinion-card-title { color: var(--red); }

.opinion-author {
  display: flex;
  align-items: center;
  gap: 10px;
}

.opinion-avatar {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--red);
}

.opinion-author-name {
  font-size: 0.75rem;
  font-weight: 600;
  color: white;
}

.opinion-author-title {
  font-size: 0.65rem;
  color: #888;
}

/* KATEGORI BAR */
.kat-bar {
  background: var(--white);
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  padding: 28px 0;
}

.kat-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 0;
}

.kat-item {
  padding: 16px 24px;
  border-right: 1px solid var(--border);
  cursor: pointer;
  transition: background 0.2s;
  text-align: center;
}

.kat-item:last-child { border-right: none; }
.kat-item:hover { background: #f0ece3; }

.kat-icon { font-size: 1.4rem; margin-bottom: 6px; display: block; }

.kat-name {
  font-family: 'Playfair Display', serif;
  font-size: 0.85rem;
  font-weight: 700;
  margin-bottom: 3px;
}

.kat-count { font-size: 0.65rem; color: var(--muted); }

/* FOOTER */
footer {
  background: var(--dark);
  color: #aaa;
  padding: 52px 0 0;
}

.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 48px;
  padding-bottom: 40px;
  border-bottom: 1px solid rgba(255,255,255,0.08);
}

.footer-brand .logo-main { color: white; font-size: 1.8rem; }
.footer-brand .logo-main span { color: var(--red); }
.footer-brand .logo-top { color: var(--red); }

.footer-brand p {
  font-family: 'Source Serif 4', serif;
  font-size: 0.88rem;
  line-height: 1.7;
  color: #888;
  margin-top: 14px;
  max-width: 260px;
}

.footer-col h4 {
  font-size: 0.6rem;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--red);
  margin-bottom: 18px;
  font-weight: 700;
}

.footer-col ul { list-style: none; }
.footer-col ul li { margin-bottom: 10px; }

.footer-col ul li a {
  color: #888;
  text-decoration: none;
  font-size: 0.85rem;
  transition: color 0.2s;
}

.footer-col ul li a:hover { color: white; }

.footer-bottom {
  padding: 18px 0;
  display: flex;
  justify-content: space-between;
  font-size: 0.7rem;
  color: #555;
  letter-spacing: 1px;
}

.footer-bottom .red { color: var(--red); }

/* HABER DETAY MODAL */
.modal-bg {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.85);
  z-index: 200;
  display: none;
  align-items: flex-start;
  justify-content: center;
  overflow-y: auto;
  padding: 40px 20px;
  backdrop-filter: blur(4px);
}

.modal-bg.active { display: flex; }

.modal-box {
  background: var(--white);
  width: 90%;
  max-width: 760px;
  padding: 52px;
  position: relative;
  animation: modalIn 0.3s ease both;
}

@keyframes modalIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.modal-close {
  position: absolute;
  top: 20px; right: 24px;
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--muted);
  transition: color 0.2s;
}

.modal-close:hover { color: var(--red); }

.modal-cat {
  display: inline-block;
  background: var(--red);
  color: white;
  font-size: 0.6rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 5px 12px;
  margin-bottom: 16px;
}

.modal-title {
  font-family: 'Playfair Display', serif;
  font-size: 2rem;
  font-weight: 900;
  line-height: 1.2;
  margin-bottom: 16px;
}

.modal-meta {
  font-size: 0.75rem;
  color: var(--muted);
  display: flex;
  gap: 16px;
  padding-bottom: 20px;
  border-bottom: 2px solid var(--dark);
  margin-bottom: 24px;
}

.modal-meta .author { font-weight: 700; color: var(--dark); }
.modal-meta .time { color: var(--red); }

.modal-img {
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
  margin-bottom: 24px;
}

.modal-body {
  font-family: 'Source Serif 4', serif;
  font-size: 1.05rem;
  line-height: 1.85;
  color: #333;
}

.modal-body p { margin-bottom: 18px; }

/* SEARCH OVERLAY */
.search-overlay {
  position: fixed;
  inset: 0;
  background: rgba(10,10,10,0.97);
  z-index: 300;
  display: none;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.search-overlay.active { display: flex; }

.search-box {
  width: 90%;
  max-width: 680px;
  position: relative;
}

.search-box input {
  width: 100%;
  background: none;
  border: none;
  border-bottom: 2px solid var(--red);
  color: white;
  font-family: 'Playfair Display', serif;
  font-size: 2.5rem;
  font-style: italic;
  padding: 16px 0;
  outline: none;
}

.search-box input::placeholder { color: #555; }

.search-x {
  position: absolute;
  top: -50px; right: 0;
  background: none;
  border: none;
  color: #666;
  font-size: 1.3rem;
  cursor: pointer;
  transition: color 0.2s;
}

.search-x:hover { color: var(--red); }

.search-hint {
  margin-top: 16px;
  font-size: 0.7rem;
  letter-spacing: 2px;
  color: #555;
  text-transform: uppercase;
}

@media (max-width: 900px) {
  .topbar { padding: 7px 20px; }
  nav { padding: 0 20px; }
  .container { padding: 0 20px; }
  .hero-grid { grid-template-columns: 1fr; }
  .hero-side { border-left: none; padding-left: 0; border-top: 1px solid var(--border); padding-top: 24px; }
  .news-grid { grid-template-columns: 1fr; }
  .opinion-grid { grid-template-columns: 1fr; }
  .kat-grid { grid-template-columns: repeat(2, 1fr); }
  .footer-grid { grid-template-columns: 1fr; padding: 0 20px 32px; }
  .footer-bottom { padding: 14px 20px; flex-direction: column; gap: 6px; }
  .nav-menu { display: none; }
  .modal-box { padding: 28px 20px; }
  .opinion-section { padding: 32px 0; }
  .kat-bar { padding: 20px 0; }
}
</style>
</head>
<body>

<!-- SEARCH -->
<div class="search-overlay" id="searchOv">
  <div class="search-box">
    <button class="search-x" onclick="closeSearch()">✕</button>
    <input type="text" placeholder="Haber ara...">
    <p class="search-hint">Aramak için yaz</p>
  </div>
</div>

<!-- HABER MODAL -->
<div class="modal-bg" id="haberModal">
  <div class="modal-box">
    <button class="modal-close" onclick="closeHaber()">✕</button>
    <div class="modal-cat" id="mCat">Politika</div>
    <h1 class="modal-title" id="mTitle">Haber Başlığı</h1>
    <div class="modal-meta">
      <span class="author" id="mAuthor">Yazar</span>
      <span class="time" id="mTime">2 saat önce</span>
      <span id="mLoc">Brüksel</span>
    </div>
    <img class="modal-img" id="mImg" src="" alt="">
    <div class="modal-body" id="mBody"></div>
  </div>
</div>

<!-- TOP BAR -->
<div class="topbar">
  <span class="breaking">● Son Dakika</span>
  <span>12 Mart 2026 — Avrupa Baskısı</span>
  <span>🌤 Brüksel 8°C · Berlin 5°C · Paris 11°C</span>
</div>

<!-- TICKER -->
<div class="ticker">
  <div class="ticker-inner">
    <span class="ticker-item">AB Zirvesi Bugün Brüksel'de Toplandı</span>
    <span class="ticker-item">Almanya'da Koalisyon Müzakereleri Sürüyor</span>
    <span class="ticker-item">Fransa'da Grev Dalgası Büyüyor</span>
    <span class="ticker-item">NATO Savunma Bakanları Toplandı</span>
    <span class="ticker-item">Avrupa Borsaları Güne Yükselişle Başladı</span>
    <span class="ticker-item">İtalya'da Hükümet Krizi Derinleşiyor</span>
    <span class="ticker-item">AB Zirvesi Bugün Brüksel'de Toplandı</span>
    <span class="ticker-item">Almanya'da Koalisyon Müzakereleri Sürüyor</span>
    <span class="ticker-item">Fransa'da Grev Dalgası Büyüyor</span>
    <span class="ticker-item">NATO Savunma Bakanları Toplandı</span>
    <span class="ticker-item">Avrupa Borsaları Güne Yükselişle Başladı</span>
    <span class="ticker-item">İtalya'da Hükümet Krizi Derinleşiyor</span>
  </div>
</div>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a class="logo-wrap" href="#">
      <span class="logo-top">Avrupa · Gündem · Analiz</span>
      <span class="logo-main">Avrupa<span>Haber</span></span>
      <span class="logo-bottom">Avrupa'nın Türkçe Sesi</span>
    </a>
    <div class="nav-right">
      <span class="edition">12 Mart 2026 · Sayı 847</span>
      <button class="search-btn" onclick="openSearch()">⌕ Ara</button>
    </div>
  </div>
  <ul class="nav-menu">
    <li><a href="#" class="active">Anasayfa</a></li>
    <li><a href="#">Politika</a></li>
    <li><a href="#">Ekonomi</a></li>
    <li><a href="#">Dünya</a></li>
    <li><a href="#">Kültür</a></li>
    <li><a href="#">Spor</a></li>
    <li><a href="#">Teknoloji</a></li>
    <li><a href="#">Köşe Yazıları</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="container">
  <div class="hero-grid">
    <div class="hero-main" onclick="openHaber('Politika','AB Liderler Zirvesi: Ukrayna Desteği ve Savunma Bütçesi Masada','Muhabirimiz','3 saat önce','Brüksel','https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?w=900&q=80','<p>Avrupa Birliği liderleri, bugün Brüksel\'deki olağanüstü zirvede Ukrayna\'ya verilecek askeri yardım paketini ve ortak savunma bütçesinin artırılmasını görüşüyor.</p><p>Zirveye katılan 27 üye ülkenin liderleri, savunma harcamalarının GSYİH\'nin yüzde üçüne çıkarılması teklifini masaya yatırdı. Almanya Başbakanı öncülüğünde hazırlanan taslak metin, gece boyunca süren müzakereler sonucunda şekillendi.</p><p>Fransa Cumhurbaşkanı, ortak Avrupa ordusunun kurulması çağrısını yeniledi. Öte yandan Macaristan ve Slovakya, bazı maddelere itiraz ediyor.</p>')">
      <img src="https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?w=900&q=80" alt="">
      <div class="hero-cat">Politika</div>
      <h1 class="hero-title">AB Liderler Zirvesi: Ukrayna Desteği ve Savunma Bütçesi Masada</h1>
      <p class="hero-desc">Avrupa Birliği'nin 27 üye ülkesinin liderleri, bugün Brüksel'de Ukrayna'ya yönelik askeri yardım paketi ve savunma harcamalarının artırılmasını görüşmek üzere bir araya geldi.</p>
      <div class="hero-meta">
        <span class="author">Muhabirimiz</span>
        <span class="time">3 saat önce</span>
        <span>Brüksel</span>
      </div>
    </div>

    <div class="hero-side">
      <div class="side-story" onclick="openHaber('Ekonomi','Avrupa Merkez Bankası Faiz Kararını Açıkladı','Ekonomi Masası','1 saat önce','Frankfurt','https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?w=500&q=80','<p>Avrupa Merkez Bankası, enflasyonla mücadele kapsamında faiz oranlarını sabit tutma kararı aldı. Karar, piyasaların beklentileriyle örtüşüyor.</p><p>AMB Başkanı yaptığı açıklamada, enflasyonun yüzde iki hedefine yaklaştığını ancak henüz istenen seviyeye ulaşılmadığını vurguladı.</p>')">
        <img src="https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?w=500&q=80" alt="">
        <div class="side-cat">Ekonomi</div>
        <div class="side-title">Avrupa Merkez Bankası Faiz Kararını Açıkladı</div>
        <div class="side-meta">1 saat önce · Frankfurt</div>
      </div>
      <div class="side-story" onclick="openHaber('Dünya','Fransa\'da Emeklilik Reformuna Karşı Büyük Grev','Paris Muhabirimiz','5 saat önce','Paris','https://images.unsplash.com/photo-1502602898657-3e91760cbb34?w=500&q=80','<p>Fransa\'da emeklilik reformuna karşı başlayan grev dalgası, ülke genelinde ulaşım ve eğitim başta olmak üzere pek çok sektörü felç etti.</p><p>Sendikalar, hükümetin emeklilik yaşını 64\'e yükseltme planına karşı çıkarak sokağa indi. Başkent Paris\'te yüz binlerce kişi meydanlara aktı.</p>')">
        <img src="https://images.unsplash.com/photo-1502602898657-3e91760cbb34?w=500&q=80" alt="">
        <div class="side-cat">Dünya</div>
        <div class="side-title">Fransa'da Emeklilik Reformuna Karşı Büyük Grev</div>
        <div class="side-meta">5 saat önce · Paris</div>
      </div>
    </div>
  </div>

  <!-- SON HABERLER -->
  <div class="sec-div">
    <div class="sec-div-title"><span>◆</span> Son Haberler</div>
    <div class="sec-div-line"></div>
    <a href="#" class="sec-div-link">Tümünü Gör →</a>
  </div>

  <div class="news-grid">
    <div class="news-card" onclick="openHaber('İsviçre','Kerzers\'te Otobüs Yangını: 6 Kişi Hayatını Kaybetti','AvrupaHaber','12 Mart 2026','Kerzers, İsviçre','https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=600&q=80','<p>İsviçre\'nin Fribourg kantonuna bağlı Kerzers kasabasında korkunç bir olay yaşandı. Posta otobüsünde seyahat eden bir yolcu, araç içinde kendini ateşe verdi. Yangın bir dakikadan kısa sürede tüm otobüse yayıldı.</p><p>Olayda otobüs sürücüsü dahil 6 kişi hayatını kaybetti, 5 kişi ise yaralandı. Hayatını kaybedenler arasında yerel bir radyo sunucusu da bulunuyor.</p><p>Yetkililere göre şüpheli fail, daha önce psikiyatrik açıdan \"istikrarsız\" olarak tanınan bir İsviçre vatandaşıydı. Olay günü fiziksel bir rahatsızlık nedeniyle hastanede bulunuyordu; ancak hastaneden izinsiz ayrıldı ve kısa süre sonra trajedi yaşandı.</p><p>Bern Kantonu polisi, failin hastane kayıtlarında kayıp olarak bildirildiğini doğruladı. İsviçre Cumhurbaşkanı Parmelin olayı kınarken, ülke genelinde saygı duruşu düzenlendi.</p>')">
      <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=600&q=80" alt="">
      <div class="news-cat">🔴 Son Dakika · İsviçre</div>
      <div class="news-title">Kerzers'te Otobüs Yangını: 6 Kişi Hayatını Kaybetti</div>
      <p class="news-desc">Bir yolcunun kendini ateşe vermesi sonucu çıkan yangında 6 kişi öldü. Şüpheli fail hastaneden kaçmış bir kişi.</p>
      <div class="news-meta"><span class="author">AvrupaHaber</span><span>12 Mart 2026</span></div>
    </div>
    <div class="news-card" onclick="openHaber('Almanya','Almanya\'da Koalisyon Hükümeti Kuruldu','Berlin Bürosu','2 saat önce','Berlin','https://images.unsplash.com/photo-1467269204594-9661b134dd2b?w=600&q=80','<p>Almanya\'da haftalarca süren müzakereler sonucunda üç partinin bir araya geldiği koalisyon hükümeti resmen kuruldu. Yeni hükümet, ekonomik reform ve enerji dönüşümünü öncelikli hedefler olarak belirledi.</p>')">
      <img src="https://images.unsplash.com/photo-1467269204594-9661b134dd2b?w=600&q=80" alt="">
      <div class="news-cat">Almanya</div>
      <div class="news-title">Almanya'da Koalisyon Hükümeti Resmen Kuruldu</div>
      <p class="news-desc">Haftalarca süren müzakereler sonucunda üç partinin oluşturduğu koalisyon hükümeti bugün yemin etti.</p>
      <div class="news-meta"><span class="author">Berlin Bürosu</span><span>2 saat önce</span></div>
    </div>
    <div class="news-card" onclick="openHaber('İspanya','Madrid\'de Tarihi Seçim Sonuçları','Madrid Muhabirimiz','4 saat önce','Madrid','https://images.unsplash.com/photo-1539037116277-4db20889f2d4?w=600&q=80','<p>İspanya\'da gerçekleştirilen genel seçimlerde sol-merkez koalisyon, sağ blok karşısında beklenmedik bir zafer kazandı. Seçim sonuçları Avrupa siyasetinde yeni bir denge yaratabilir.</p>')">
      <img src="https://images.unsplash.com/photo-1539037116277-4db20889f2d4?w=600&q=80" alt="">
      <div class="news-cat">İspanya</div>
      <div class="news-title">Madrid'de Tarihi Seçim Zaferi: Sol Blok Önde</div>
      <p class="news-desc">İspanya genel seçimlerinde sol-merkez koalisyon beklenmedik bir zafer kazandı.</p>
      <div class="news-meta"><span class="author">Madrid Muhabirimiz</span><span>4 saat önce</span></div>
    </div>
    <div class="news-card" onclick="openHaber('Teknoloji','Avrupa\'nın Yapay Zeka Yasası Yürürlüğe Girdi','Teknoloji Masası','6 saat önce','Brüksel','https://images.unsplash.com/photo-1677442135703-1787eea5ce01?w=600&q=80','<p>Dünyada bir ilk olan Avrupa Yapay Zeka Yasası bugün resmi olarak yürürlüğe girdi. Yasa kapsamında yüksek riskli yapay zeka sistemleri sıkı denetime tabi tutulacak.</p>')">
      <img src="https://images.unsplash.com/photo-1677442135703-1787eea5ce01?w=600&q=80" alt="">
      <div class="news-cat">Teknoloji</div>
      <div class="news-title">Avrupa'nın Yapay Zeka Yasası Bugün Yürürlüğe Girdi</div>
      <p class="news-desc">Dünyada bir ilk olan AB Yapay Zeka Yasası resmi olarak hayata geçti. Şirketler için yeni kurallar başlıyor.</p>
      <div class="news-meta"><span class="author">Teknoloji Masası</span><span>6 saat önce</span></div>
    </div>
  </div>
</div>

<!-- KATEGORİ BAR -->
<div class="kat-bar">
  <div class="container">
    <div class="kat-grid">
      <div class="kat-item"><span class="kat-icon">🏛️</span><div class="kat-name">Politika</div><div class="kat-count">142 haber</div></div>
      <div class="kat-item"><span class="kat-icon">📈</span><div class="kat-name">Ekonomi</div><div class="kat-count">98 haber</div></div>
      <div class="kat-item"><span class="kat-icon">🌍</span><div class="kat-name">Dünya</div><div class="kat-count">215 haber</div></div>
      <div class="kat-item"><span class="kat-icon">⚽</span><div class="kat-name">Spor</div><div class="kat-count">76 haber</div></div>
      <div class="kat-item"><span class="kat-icon">💻</span><div class="kat-name">Teknoloji</div><div class="kat-count">54 haber</div></div>
    </div>
  </div>
</div>

<!-- KÖŞE YAZILARI -->
<div class="opinion-section">
  <div class="container">
    <div class="opinion-head">
      <div class="opinion-title">Köşe <span>Yazıları</span></div>
      <div class="opinion-line"></div>
    </div>
    <div class="opinion-grid">
      <div class="opinion-card" onclick="openHaber('Köşe Yazısı','Avrupa\'nın Savunma Açmazı','Prof. Dr. Mehmet Yılmaz','Dün','Brüksel','https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?w=600&q=80','<p>Avrupa, onlarca yıldır ABD\'nin güvenlik şemsiyesi altında yaşadı. Şimdi bu şemsiye kapanıyor ve kıta kendi savunmasını inşa etmek zorunda. Peki bu mümkün mü?</p><p>Savunma sanayii, bütçe, siyasi irade... Bunların hepsi büyük soru işaretleri taşıyor. Ancak Ukrayna savaşı, Avrupa\'yı uyandırdı.</p>')">
        <div class="opinion-big-quote">"</div>
        <div class="opinion-card-title">Avrupa'nın Savunma Açmazı: Kıta Kendi Ordusunu Kurabilir mi?</div>
        <div class="opinion-author">
          <img class="opinion-avatar" src="https://i.pravatar.cc/80?img=11" alt="">
          <div>
            <div class="opinion-author-name">Prof. Dr. Mehmet Yılmaz</div>
            <div class="opinion-author-title">Dış Politika Analisti</div>
          </div>
        </div>
      </div>
      <div class="opinion-card" onclick="openHaber('Köşe Yazısı','Euro\'nun Geleceği','Elif Kaya','2 gün önce','Frankfurt','https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?w=600&q=80','<p>Avrupa tek para birimi Euro, kurulduğundan bu yana pek çok kriz atlattı. Bugün yeni bir sınav dönemi başlıyor. Enflasyon, siyasi bölünme ve küresel rekabet Euro\'yu zorluyor.</p>')">
        <div class="opinion-big-quote">"</div>
        <div class="opinion-card-title">Euro'nun Geleceği: Tek Para Birimi Yeni Sınavda</div>
        <div class="opinion-author">
          <img class="opinion-avatar" src="https://i.pravatar.cc/80?img=5" alt="">
          <div>
            <div class="opinion-author-name">Elif Kaya</div>
            <div class="opinion-author-title">Ekonomi Editörü</div>
          </div>
        </div>
      </div>
      <div class="opinion-card" onclick="openHaber('Köşe Yazısı','Göç Krizi ve Avrupa','Can Demir','3 gün önce','Atina','https://images.unsplash.com/photo-1532375810709-75b1da00537c?w=600&q=80','<p>Göç meselesi, Avrupa siyasetinin en sancılı konularından biri olmaya devam ediyor. Sağ partilerin yükselişi, bu sorunun nasıl ele alındığıyla doğrudan bağlantılı.</p>')">
        <div class="opinion-big-quote">"</div>
        <div class="opinion-card-title">Göç Krizi Avrupa'yı Bölüyor: Çözüm Nerede?</div>
        <div class="opinion-author">
          <img class="opinion-avatar" src="https://i.pravatar.cc/80?img=8" alt="">
          <div>
            <div class="opinion-author-name">Can Demir</div>
            <div class="opinion-author-title">Balkanlar Muhabiri</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <a class="logo-wrap" href="#">
          <span class="logo-top">Avrupa · Gündem · Analiz</span>
          <span class="logo-main">Avrupa<span>Haber</span></span>
        </a>
        <p>Avrupa'dan bağımsız, tarafsız ve derinlemesine habercilik. Türkçe konuşan dünyanın Avrupa sesi.</p>
      </div>
      <div class="footer-col">
        <h4>Kategoriler</h4>
        <ul>
          <li><a href="#">Politika</a></li>
          <li><a href="#">Ekonomi</a></li>
          <li><a href="#">Dünya</a></li>
          <li><a href="#">Kültür</a></li>
          <li><a href="#">Spor</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Ülkeler</h4>
        <ul>
          <li><a href="#">Almanya</a></li>
          <li><a href="#">Fransa</a></li>
          <li><a href="#">İtalya</a></li>
          <li><a href="#">İspanya</a></li>
          <li><a href="#">Hollanda</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h4>Kurumsal</h4>
        <ul>
          <li><a href="#">Hakkımızda</a></li>
          <li><a href="#">İletişim</a></li>
          <li><a href="#">Reklam</a></li>
          <li><a href="#">Gizlilik</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 <span class="red">AvrupaHaber</span> — Tüm Hakları Saklıdır</span>
      <span>Avrupa'nın Türkçe Sesi</span>
    </div>
  </div>
</footer>

<script>
const haberler = {};

function openHaber(cat, title, author, time, loc, img, body) {
  document.getElementById('mCat').textContent = cat;
  document.getElementById('mTitle').textContent = title;
  document.getElementById('mAuthor').textContent = author;
  document.getElementById('mTime').textContent = time;
  document.getElementById('mLoc').textContent = loc;
  document.getElementById('mImg').src = img;
  document.getElementById('mBody').innerHTML = body;
  document.getElementById('haberModal').classList.add('active');
  document.body.style.overflow = 'hidden';
}

function closeHaber() {
  document.getElementById('haberModal').classList.remove('active');
  document.body.style.overflow = '';
}

function openSearch() {
  document.getElementById('searchOv').classList.add('active');
  setTimeout(() => document.querySelector('.search-box input').focus(), 100);
}

function closeSearch() {
  document.getElementById('searchOv').classList.remove('active');
}

document.getElementById('haberModal').addEventListener('click', e => { if(e.target === e.currentTarget) closeHaber(); });
document.getElementById('searchOv').addEventListener('click', e => { if(e.target === e.currentTarget) closeSearch(); });
document.addEventListener('keydown', e => { if(e.key==='Escape'){ closeHaber(); closeSearch(); } });
</script>
</body>
</html>
