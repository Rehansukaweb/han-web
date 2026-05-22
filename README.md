<html lang="id">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>IT - Institute Trading | Professional Education</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --c-primary: #00b140;
  --c-primary-light: #00ff88;
  --c-grad: linear-gradient(135deg, var(--c-primary), var(--c-primary-light));
  --c-bg: #f5fff7;
  --c-surface: #ffffff;
  --c-text: #111827;
  --c-text-muted: #4b5563;
  --shadow-soft: 0 15px 40px rgba(0, 177, 64, 0.06);
  --shadow-hover: 0 20px 50px rgba(0, 177, 64, 0.15);
  --border-soft: 1px solid rgba(0, 177, 64, 0.1);
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body{
  font-family: 'Poppins', sans-serif;
  background: var(--c-bg);
  color: var(--c-text);
  overflow-x: hidden;
  line-height: 1.7;
}

/* NAVBAR */
header{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 18px 7%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  z-index: 1000;
  border-bottom: 1px solid rgba(0,0,0,0.03);
  transition: all 0.4s ease;
}

.logo{
  display: flex;
  align-items: center;
  gap: 14px;
}

.logo-circle{
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: var(--c-grad);
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.2rem;
  color: white;
  font-weight: 800;
  box-shadow: 0 10px 20px rgba(0, 177, 64, 0.25);
  animation: floating 4s ease-in-out infinite;
}

.logo h2{
  font-size: 1.4rem;
  color: var(--c-primary);
  font-weight: 800;
  letter-spacing: -0.5px;
}

.logo p {
  font-size: 0.7rem;
  color: var(--c-text-muted);
  font-weight: 600;
  letter-spacing: 1px;
  text-transform: uppercase;
}

nav{
  display: flex;
  gap: 40px;
}

nav a{
  text-decoration: none;
  color: var(--c-text);
  font-weight: 600;
  font-size: 0.95rem;
  transition: 0.3s ease;
  position: relative;
}

nav a::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background: var(--c-primary);
  transition: 0.3s ease;
}

nav a:hover{
  color: var(--c-primary);
}

nav a:hover::after {
  width: 100%;
}

/* HERO */
.hero{
  min-height: 100vh;
  padding: 180px 7% 100px;
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  align-items: center;
  gap: 60px;
  background: 
    radial-gradient(circle at 10% 20%, rgba(214, 255, 228, 0.7) 0%, transparent 40%),
    radial-gradient(circle at 90% 80%, rgba(197, 255, 217, 0.6) 0%, transparent 40%);
}

.badge{
  display: inline-flex;
  align-items: center;
  padding: 8px 18px;
  background: rgba(0, 177, 64, 0.1);
  color: var(--c-primary);
  font-weight: 700;
  border-radius: 50px;
  margin-bottom: 25px;
  font-size: 0.9rem;
  border: var(--border-soft);
  letter-spacing: 0.5px;
}

.hero h1{
  font-size: 4rem;
  line-height: 1.15;
  margin-bottom: 25px;
  font-weight: 800;
  color: #0a1128;
  letter-spacing: -1px;
}

.hero h1 span{
  background: var(--c-grad);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero p{
  font-size: 1.15rem;
  line-height: 1.8;
  color: var(--c-text-muted);
  max-width: 95%;
  margin-bottom: 40px;
}

.hero-buttons{
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}

.btn{
  padding: 16px 35px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.05rem;
  transition: all 0.3s ease;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

.btn-primary{
  background: var(--c-grad);
  color: white;
  box-shadow: 0 10px 20px rgba(0, 177, 64, 0.2);
}

.btn-primary:hover{
  transform: translateY(-4px);
  box-shadow: 0 15px 30px rgba(0, 177, 64, 0.35);
}

.btn-secondary{
  background: white;
  color: var(--c-primary);
  box-shadow: var(--shadow-soft);
  border: 1px solid rgba(0, 177, 64, 0.15);
}

.btn-secondary:hover{
  border-color: var(--c-primary);
  color: var(--c-primary);
  transform: translateY(-4px);
  box-shadow: var(--shadow-hover);
}

/* HERO RIGHT (CARD) */
.hero-card{
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(20px);
  padding: 50px 45px;
  border-radius: 35px;
  box-shadow: var(--shadow-hover);
  border: var(--border-soft);
  position: relative;
  overflow: hidden;
  animation: floating 5s ease-in-out infinite;
}

.hero-card::before{
  content: '';
  position: absolute;
  width: 300px;
  height: 300px;
  background: var(--c-grad);
  top: -120px;
  right: -120px;
  border-radius: 50%;
  opacity: 0.1;
  filter: blur(50px);
}

.hero-card h2{
  font-size: 1.5rem;
  margin-bottom: 35px;
  font-weight: 800;
  color: #0a1128;
  text-align: center;
  letter-spacing: 1px;
}

.stat-box{
  background: white;
  padding: 22px 25px;
  border-radius: 20px;
  margin-bottom: 18px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.03);
  border: 1px solid #f4f4f4;
  display: flex;
  align-items: center;
  gap: 25px;
}

.stat-box h3{
  font-size: 2.2rem;
  color: var(--c-primary);
  font-weight: 800;
  min-width: 80px;
}

.stat-box p {
  color: var(--c-text-muted);
  font-size: 0.95rem;
  font-weight: 600;
  line-height: 1.4;
}

.progress{
  width: 100%;
  height: 14px;
  background: #edf2f7;
  border-radius: 50px;
  overflow: hidden;
  margin-top: 35px;
}

.progress-fill{
  height: 100%;
  width: 90%;
  background: var(--c-grad);
  border-radius: 50px;
  animation: grow 3s cubic-bezier(0.1, 0.8, 0.3, 1) forwards;
}

.progress-text{
  margin-top: 15px;
  font-weight: 700;
  font-size: 0.95rem;
  color: var(--c-primary);
  text-align: right;
}

/* SECTION GLOBAL */
section{
  padding: 120px 7%;
}

.section-title{
  text-align: center;
  margin-bottom: 70px;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

.section-title span{
  display: inline-block;
  color: var(--c-primary);
  font-weight: 700;
  letter-spacing: 2px;
  font-size: 0.9rem;
  text-transform: uppercase;
  background: rgba(0, 177, 64, 0.1);
  padding: 8px 20px;
  border-radius: 50px;
  margin-bottom: 20px;
}

.section-title h2{
  font-size: 3rem;
  color: #0a1128;
  font-weight: 800;
  line-height: 1.2;
  margin-bottom: 20px;
}

.section-title p {
  font-size: 1.1rem;
  color: var(--c-text-muted);
}

/* GRID & CARDS (TENTANG KAMI) */
.grid{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 35px;
}

.card{
  background: var(--c-surface);
  padding: 50px 40px;
  border-radius: 30px;
  box-shadow: var(--shadow-soft);
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
  border: 1px solid rgba(255,255,255,0.8);
  z-index: 1;
}

.card::before{
  content: '';
  position: absolute;
  width: 150px;
  height: 150px;
  background: var(--c-grad);
  opacity: 0.04;
  top: -50px;
  right: -50px;
  border-radius: 50%;
  transition: all 0.5s ease;
  z-index: -1;
}

.card:hover{
  transform: translateY(-12px);
  box-shadow: var(--shadow-hover);
}

.card:hover::before {
  transform: scale(2);
  opacity: 0.08;
}

.card h3{
  margin-bottom: 20px;
  font-size: 1.5rem;
  font-weight: 800;
  color: #0a1128;
  display: flex;
  align-items: center;
  gap: 15px;
}

.card p{
  color: var(--c-text-muted);
  line-height: 1.8;
  font-size: 1rem;
}

/* ACCORDION (PROGRAM) */
.accordion-wrapper {
  max-width: 900px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.accordion-btn {
  background: var(--c-surface);
  padding: 35px 45px;
  border-radius: 25px;
  box-shadow: var(--shadow-soft);
  width: 100%;
  text-align: left;
  font-size: 1.35rem;
  font-weight: 700;
  font-family: inherit;
  border: 1px solid rgba(0,0,0,0.02);
  cursor: pointer;
  transition: all 0.3s ease;
  color: #0a1128;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.accordion-btn span {
  font-size: 1.8rem;
  font-weight: 400;
  color: var(--c-primary);
  transition: transform 0.4s ease;
}

.accordion-btn.active span {
  transform: rotate(45deg);
}

.accordion-btn:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-hover);
}

.accordion-btn.premium-acc {
  background: var(--c-grad);
  color: white;
  border: none;
}

.accordion-btn.premium-acc span {
  color: white;
}

.accordion-content {
  padding: 0 45px;
  background: var(--c-surface);
  border-radius: 0 0 25px 25px;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s cubic-bezier(0.1, 0.8, 0.3, 1), padding 0.5s ease;
  box-shadow: var(--shadow-soft);
  margin-top: -30px; 
  position: relative;
  z-index: -1; 
}

.accordion-content p {
  color: var(--c-text-muted);
  line-height: 1.9;
  padding: 55px 0 35px 0;
  font-size: 1.05rem;
}

.accordion-content ul {
  padding: 0 0 35px 20px;
  color: var(--c-text-muted);
  line-height: 1.9;
  font-size: 1.05rem;
}

.accordion-content li {
  margin-bottom: 10px;
}

/* RULES & MATERI */
.rules{
  display: flex;
  flex-direction: column;
  gap: 25px;
  max-width: 900px;
  margin: auto;
}

.rule{
  background: var(--c-surface);
  padding: 35px 45px;
  border-radius: 20px;
  box-shadow: var(--shadow-soft);
  transition: all 0.3s ease;
  border-left: 8px solid var(--c-primary);
}

.rule:hover{
  transform: translateX(15px);
  box-shadow: var(--shadow-hover);
}

.rule h4 {
  color: #0a1128;
  font-size: 1.3rem;
  margin-bottom: 15px;
  font-weight: 800;
}

.rule p {
  color: var(--c-text-muted);
  line-height: 1.8;
  font-size: 1.05rem;
}

/* CONTACT BOX */
.contact-wrapper {
  max-width: 1000px;
  margin: auto;
  display: grid;
  grid-template-columns: 1fr;
  gap: 40px;
}

.contact-box{
  background: var(--c-surface);
  padding: 70px 50px;
  border-radius: 40px;
  text-align: center;
  box-shadow: var(--shadow-hover);
  position: relative;
}

.contact-box::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 10px;
  background: var(--c-grad);
  border-radius: 40px 40px 0 0;
}

.contact-box h2{
  font-size: 2.5rem;
  color: #0a1128;
  margin-bottom: 15px;
  font-weight: 800;
}

.contact-box h2 span {
  color: var(--c-primary);
}

.contact-box p {
  color: var(--c-text-muted);
  font-size: 1.15rem;
  margin-bottom: 30px;
}

.contact-box h3{
  font-size: 3.5rem;
  margin: 20px 0;
  color: var(--c-primary);
  font-weight: 800;
  letter-spacing: 3px;
}

.payment-methods {
  margin-top: 50px;
  padding-top: 30px;
  border-top: 1px solid #eee;
}

.payment-methods p {
  font-size: 0.9rem;
  font-weight: 600;
  color: #888;
  margin-bottom: 15px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.payment-badges {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
}

.payment-badge {
  background: #f8f9fa;
  padding: 8px 20px;
  border-radius: 10px;
  font-weight: 700;
  color: #333;
  border: 1px solid #e9ecef;
  font-size: 0.95rem;
}

/* FOOTER */
footer{
  background: #008731;
  padding: 70px 20px;
  text-align: center;
  color: white;
}

footer h2{
  font-size: 1.8rem;
  margin-bottom: 15px;
  font-weight: 800;
}

footer p {
  opacity: 0.9;
  font-size: 1rem;
  margin-bottom: 10px;
}

/* ANIMATION */
@keyframes floating{
  0%, 100%{ transform: translateY(0); }
  50%{ transform: translateY(-20px); }
}

@keyframes grow{
  from{ width: 0%; }
  to{ width: 90%; }
}

/* RESPONSIVE */
@media(max-width:1100px){
  .hero{ grid-template-columns: 1fr; padding-top: 150px; gap: 50px; }
  .hero h1{ font-size: 3.5rem; }
  .hero-card { margin: 0 auto; max-width: 550px; width: 100%; }
  nav{ display: none; }
}

@media(max-width:600px){
  .hero h1{ font-size: 2.6rem; }
  .hero p { font-size: 1.05rem; }
  .section-title h2{ font-size: 2.2rem; }
  .btn{ width: 100%; }
  .contact-box{ padding: 50px 25px; }
  .contact-box h3 { font-size: 2.5rem; }
  section { padding: 90px 5%; }
  .accordion-btn { padding: 25px 30px; font-size: 1.15rem; }
  .card { padding: 35px 25px; }
}
</style>
</head>

<body>

<header>
  <div class="logo">
    <div class="logo-circle">IT</div>
    <div>
      <h2>Institute Trading</h2>
      <p>by RHN Capital Finance</p>
    </div>
  </div>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">Filosofi</a>
    <a href="#program">Program & Kurikulum</a>
    <a href="#materi">Silabus Edukasi</a>
    <a href="#rules">S.O.P Trading</a>
    <a href="#contact">Kemitraan</a>
  </nav>
</header>

<section class="hero" id="home">
  <div>
    <div class="badge">Institusi Edukasi Finansial Terpercaya</div>
    <h1>Menciptakan <span>Trader Profesional</span> Yang Konsisten & Disiplin</h1>
    <p>Didukung oleh ekosistem <strong>RHN CAPITAL FINANCE</strong>, Institute Trading hadir secara eksklusif untuk membangun trader dengan penguasaan psikologi tingkat tinggi, manajemen risiko institusional, dan akurasi teknikal menuju kebebasan finansial jangka panjang.</p>
    <div class="hero-buttons">
      <a href="https://wa.me/6285717426626" class="btn btn-primary">Konsultasi Mentor Gratis</a>
      <a href="#program" class="btn btn-secondary">Jelajahi Kurikulum</a>
    </div>
  </div>
  
  <div class="hero-card">
    <h2>STANDAR AKURASI INSTITUSI</h2>
    <div class="stat-box">
      <h3>90%</h3>
      <p>Penguasaan Psikologi &<br>Manajemen Ekuitas (Margin)</p>
    </div>
    <div class="stat-box">
      <h3>10%</h3>
      <p>Eksekusi Teknis, Pemetaan Likuiditas & Penggunaan Alat</p>
    </div>
    <div class="progress"><div class="progress-fill"></div></div>
    <div class="progress-text">Fokus Pada Pertumbuhan Akun Jangka Panjang</div>
  </div>
</section>

<section id="about">
  <div class="section-title">
    <span>Filosofi & Pendekatan Kami</span>
    <h2>Pondasi Menuju Profesionalisme</h2>
    <p>Kami tidak mengajarkan skema cepat kaya. Kami mencetak analis pasar dan pengelola risiko yang bertindak secara objektif layaknya institusi keuangan modern.</p>
  </div>
  <div class="grid">
    <div class="card">
      <h3>🧠 Psikologi Baja (Trading Mindset)</h3>
      <p>Melatih kendali emosional absolut. Kami mengajarkan Anda untuk beroperasi layaknya mesin—menghilangkan keraguan, ketakutan (FOMO), dan sifat serakah. Fokus utama kami adalah membentuk disiplin eksekusi tanpa terpengaruh <i>noise</i> dan volatilitas market harian.</p>
    </div>
    <div class="card">
      <h3>💼 Proteksi Ekuitas (Money Management)</h3>
      <p>Sistem pengelolaan modal yang dirancang untuk memastikan akun Anda mustahil terkena Margin Call. Mulai dari transisi akun <i>Cent</i> untuk melatih mentalitas pemula, hingga pengaturan rasio <i>Lot Size</i> yang proporsional terhadap ketahanan dana di pasar ekstrem.</p>
    </div>
    <div class="card">
      <h3>🛡️ Manajemen Risiko Defensif</h3>
      <p>Kami menanamkan prinsip bahwa modal adalah "nyawa" bisnis Anda. Penerapan <i>Stop Loss</i> terukur yang tidak bisa diganggu gugat, serta manajemen <i>Drawdown</i> harian untuk menjaga karir trading Anda bertahan selama berpuluh-puluh tahun di industri ini.</p>
    </div>
    <div class="card">
      <h3>⚙️ Penguasaan Teknologi (MT5 & EA)</h3>
      <p>Di era modern, kecepatan dan presisi adalah segalanya. Kami membekali pemahaman operasional tingkat lanjut menggunakan platform MetaTrader 5 (MT5), termasuk optimalisasi dan tata kelola <i>Expert Advisor</i> (EA/Robot Trading) berbasis algoritma yang kami rancang.</p>
    </div>
  </div>
</section>

<section id="program">
  <div class="section-title">
    <span>Kurikulum Akademi</span>
    <h2>Pilih Jalur Spesialisasi Anda</h2>
    <p>Dari pemahaman fundamental struktur pasar hingga penguasaan algoritma tingkat lanjut.</p>
  </div>
  <div class="accordion-wrapper">
    <div>
      <button class="accordion-btn">📉 Level 1: Market Structure & Foundation <span>+</span></button>
      <div class="accordion-content">
        <p>Kelas fondasi wajib bagi pemula. Modul ini membongkar ilusi market dan memberikan pemahaman logis tentang mengapa harga bergerak. Anda akan belajar:</p>
        <ul>
          <li>Anatomi Candlestick dan Price Action murni.</li>
          <li>Pemetaan Support, Resistance, serta Supply & Demand (SND).</li>
          <li>Menentukan tren primer, sekunder, dan minor (Market Structure).</li>
          <li>Transisi ke akun real menggunakan Akun Cent (USC) untuk melatih psikologi rasio.</li>
        </ul>
      </div>
    </div>
    <div>
      <button class="accordion-btn premium-acc">👑 Level 2: Smart Money Concept (SMC) & XAUUSD Mastery <span>+</span></button>
      <div class="accordion-content">
        <p>Program eksklusif terlaris kami. Anda tidak lagi bertrading seperti "Retail", melainkan mengikuti jejak institusi besar (Bank/Hedge Funds). Sangat direkomendasikan untuk trader yang menyukai pair dengan volatilitas tinggi seperti XAUUSD (Gold).</p>
        <ul>
          <li>Membaca jejak likuiditas: Mengidentifikasi area di mana Stop Loss ritel akan disapu oleh Market Maker.</li>
          <li>Pemahaman mendalam tentang Fair Value Gap (FVG), Imbalance, Order Block, dan Break of Structure (BOS / CHoCH).</li>
          <li>Spesialisasi pergerakan fundamental dan teknikal pada market Gold (XAUUSD) di berbagai Timeframe (Multi-Timeframe Analysis).</li>
          <li>Mencari setup presisi (Sniper Entry) dengan rasio Risk:Reward (RR) 1:3 hingga 1:10.</li>
        </ul>
      </div>
    </div>
    <div>
      <button class="accordion-btn">⚙️ Level 3: Algorithmic & EA Configuration <span>+</span></button>
      <div class="accordion-content">
        <p>Otomatisasi adalah kunci efisiensi waktu. Program teknis ini dirancang bagi trader yang ingin memanfaatkan kekuatan sistem otomatis tanpa harus menatap layar 24 jam.</p>
        <ul>
          <li>Pengenalan mendalam arsitektur platform MetaTrader 5 (MT5).</li>
          <li>Manajemen instalasi, kompilasi, dan <i>backtesting Expert Advisor</i> (EA) pada folder data.</li>
          <li>Penyesuaian parameter variabel logika EA agar adaptif terhadap kondisi market berjalan.</li>
          <li>Manajemen risiko terotomatisasi (Auto Lot & Auto Trailing Stop).</li>
        </ul>
      </div>
    </div>
    <div>
      <button class="accordion-btn">🚀 Level 4: Elite Mentorship & Portfolio Management <span>+</span></button>
      <div class="accordion-content">
        <p>Layanan konsultasi dan pendampingan 1-on-1 (Eksklusif) yang fokus pada pembentukan Anda menjadi pengelola dana mandiri berpenghasilan tetap.</p>
        <ul>
          <li>Audit portofolio dan pembedahan "Trading Journal" secara berkala bersama mentor.</li>
          <li>Perbaikan kesalahan eksekusi psikologis secara real-time.</li>
          <li>Strategi <i>compounding</i> tingkat lanjut dan target pertumbuhan dana (Healthy Growth).</li>
          <li>Akses prioritas ke pembaruan ekosistem riset RHN CAPITAL FINANCE.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="rules">
  <div class="section-title">
    <span>Standard Operating Procedure (SOP)</span>
    <h2>Hukum Mutlak Kesuksesan</h2>
    <p>Kami tidak menoleransi pelanggaran terhadap aturan dasar keselamatan finansial berikut ini.</p>
  </div>
  <div class="rules">
    <div class="rule">
      <h4>📜 Pasal 1: Pembatasan Risiko Tetap (Max 1-2%)</h4>
      <p>Pasar tidak bisa diprediksi secara absolut, hanya probabilitas. Merisikokan lebih dari 2% dari total ekuitas dalam satu transaksi adalah bentuk dari perjudian. Hitung <i>Lot Size</i> Anda berdasarkan jarak <i>Stop Loss</i>, bukan berdasarkan <i>feeling</i>.</p>
    </div>
    <div class="rule">
      <h4>📜 Pasal 2: Kewajiban Penggunaan Stop Loss (SL)</h4>
      <p>Beroperasi tanpa SL berarti Anda membiarkan pasar memutuskan kapan akun Anda akan hancur. SL adalah asuransi yang melindungi bisnis Anda dari "Black Swan Event" atau rilis berita fundamental yang memicu lonjakan ratusan pips dalam hitungan detik.</p>
    </div>
    <div class="rule">
      <h4>📜 Pasal 3: Kualitas Mengalahkan Kuantitas (No Overtrading)</h4>
      <p>Tugas utama Anda bukanlah terus-menerus menekan tombol <i>Buy</i> atau <i>Sell</i>. Tugas Anda adalah mengintai, menunggu konfirmasi, dan mengeksekusi HANYA jika pergerakan pasar memenuhi 100% dari kriteria sistem perdagangan Anda. Jika tidak ada setup, jangan memaksakan diri.</p>
    </div>
    <div class="rule">
      <h4>📜 Pasal 4: Audit & Jurnal Mandiri</h4>
      <p>Trader yang tidak melakukan pencatatan adalah trader buta. Setiap <i>entry</i> wajib dicatat: alasan masuk, target, rasio risiko, hingga emosi saat itu. Evaluasi mingguan adalah satu-satunya cara mengidentifikasi kelemahan sistem Anda.</p>
    </div>
  </div>
</section>

<section id="materi" style="background: white;">
  <div class="section-title">
    <span>Silabus Pengetahuan Dasar</span>
    <h2>Modul Edukasi Terbuka</h2>
    <p>Pelajari terminologi dan mekanisme dasar pasar finansial global secara komprehensif.</p>
  </div>
  <div id="kontainer-materi" class="rules"></div>
</section>

<section id="contact">
  <div class="section-title">
    <span>Layanan Anggota & Pendaftaran</span>
    <h2>Bergabung Bersama Kami</h2>
    <p>Lakukan pendaftaran kelas atau konsultasikan tantangan trading Anda langsung dengan divisi pendampingan kami.</p>
  </div>
  
  <div class="contact-wrapper">
    <div class="contact-box">
      <h2>TANYA JAWAB <span>DI WHATSAPP</span></h2>
      <p>Layanan konsultasi langsung cepat tanggap (Fast Response). Bahas strategi, review setup MT5, hingga pemilihan program yang tepat dengan kapasitas Anda.</p>
      <h3>0857-1742-6626</h3>
      
      <div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap; margin-top:35px;">
        <a href="https://wa.me/6285717426626" class="btn btn-primary">📱 Chat via WhatsApp Sekarang</a>
      </div>

      <div class="payment-methods">
        <p>Sistem Pembayaran Pendaftaran Kelas Resmi Didukung Oleh:</p>
        <div class="payment-badges">
          <div class="payment-badge">GOPAY</div>
          <div class="payment-badge">DANA</div>
          <div class="payment-badge">SHOPEEPAY</div>
          <div class="payment-badge">TRANSFER BANK</div>
        </div>
      </div>
    </div>
  </div>
</section>

<footer>
  <h2>Institute Trading</h2>
  <p>Dikembangkan secara profesional dan terafiliasi dengan RHN CAPITAL FINANCE.</p>
  <p style="margin-top: 15px; font-size: 0.85rem; opacity: 0.6;">© 2026 Institute Trading. Hak Cipta Dilindungi Undang-Undang.</p>
</footer>

<script>
// 1. EFEK BAYANGAN NAVBAR
window.addEventListener('scroll', () => {
  const header = document.querySelector('header');
  if(window.scrollY > 50){ 
    header.style.boxShadow = '0 10px 30px rgba(0, 177, 64, 0.08)'; 
    header.style.padding = '12px 7%';
  } else { 
    header.style.boxShadow = 'none'; 
    header.style.padding = '18px 7%';
  }
});

// 2. ACCORDION BUTTERY SMOOTH
const accordions = document.querySelectorAll('.accordion-btn');
accordions.forEach(acc => {
  acc.addEventListener('click', function() {
    const content = this.nextElementSibling;
    const span = this.querySelector('span');
    
    // Auto-close others for cleaner UX
    accordions.forEach(otherAcc => {
      if (otherAcc !== this) {
        otherAcc.classList.remove('active');
        otherAcc.querySelector('span').innerHTML = '+';
        otherAcc.nextElementSibling.style.maxHeight = null;
        otherAcc.nextElementSibling.style.padding = "0 45px";
      }
    });

    this.classList.toggle('active');
    
    if (content.style.maxHeight) {
      content.style.maxHeight = null;
      content.style.padding = "0 45px";
      span.innerHTML = "+";
    } else {
      content.style.maxHeight = content.scrollHeight + 120 + "px"; 
      content.style.padding = "0 45px 35px 45px";
      span.innerHTML = "+"; 
    }
  });
});

// 3. GENERATOR MATERI EDUKASI (Diperpanjang & Lebih Profesional)
const dataMateri = [
  { judul: "Mekanika Pasar Finansial Global", isi: "Trading adalah partisipasi aktif dalam likuiditas pasar aset finansial (seperti pasangan mata uang mayor, indeks saham, hingga logam mulia). Keuntungan didapatkan dengan memprediksi arah pergerakan aset berdasarkan analisis historis harga, volume, serta rilis data makroekonomi yang memengaruhi kekuatan sebuah mata uang." },
  { judul: "Anatomi Candlestick Lanjutan", isi: "Candlestick bukan sekadar warna merah atau hijau, melainkan visualisasi psikologi pelaku pasar dalam waktu tertentu. Volume bodi (Body) merepresentasikan komitmen pembeli/penjual, sementara sumbu (Wick/Shadow) merepresentasikan penolakan harga (Rejection) atau pengambilan likuiditas sebelum harga berbalik arah." },
  { judul: "Zonasi Supply & Demand (SND)", isi: "Pasar tidak bergerak secara acak. Harga bergerak dari satu zona likuiditas ke zona likuiditas lainnya. Zona Supply merepresentasikan dominasi tekanan jual historis (pesanan tertunda institusi), sedangkan Demand merepresentasikan area minat beli agregat. Mengidentifikasi zona ini adalah kunci utama untuk mendapatkan presisi tinggi." },
  { judul: "Hukum Probabilitas & Risk to Reward (RR)", isi: "Anda tidak perlu selalu benar untuk bisa mencetak profit konsisten. Dengan penerapan rasio Risk:Reward yang logis (misalnya 1:3), Anda merisikokan 1 bagian untuk mendapatkan 3 bagian. Melalui rasio ini, win-rate sebesar 35-40% dari total transaksi bulanan sudah cukup untuk membuat nilai portofolio Anda bertumbuh secara eksponensial." },
  { judul: "Konsep Dasar Smart Money (SMC)", isi: "Trader ritel cenderung bertransaksi menggunakan pola klasik yang sangat mudah diantisipasi oleh algoritma institusi besar (Smart Money). SMC mengajarkan Anda untuk melihat pasar dari sudut pandang pembuat pasar (Market Maker), memahami bagaimana mereka mengumpulkan posisi (Accumulation), menjebak ritel (Manipulation), lalu mendistribusikan harga (Distribution)." },
  { judul: "Pentingnya Manajemen Multi-Timeframe", isi: "Analisis yang valid tidak pernah bersumber hanya dari satu Timeframe (TF). Analis profesional menggunakan TF besar (Daily/H4) untuk menentukan bias arah tren utama dan mencari Order Block kuat, TF menengah (H1/M15) untuk memantau struktur pasar terkini, dan TF kecil (M5/M1) untuk masuk pasar (Entry) demi meminimalisasi jarak Stop Loss." },
  { judul: "Psikologi: Menghancurkan Bias FOMO", isi: "Fear of Missing Out (FOMO) adalah penyebab utama hancurnya akun trading. Trader profesional memiliki kesabaran tak terbatas. Mereka membiarkan harga yang mendatangi area zona setup mereka (Limit Order), bukan secara emosional mengejar harga yang sedang melesat kencang akibat berita mendadak." },
  { judul: "Navigasi Drawdown Portofolio", isi: "Drawdown (penurunan beruntun) adalah fase alami dari sistem trading mana pun. Kunci melewati fase ini bukan dengan meningkatkan ukuran lot untuk 'balas dendam' kepada pasar (Revenge Trading), melainkan menurunkan eksposur risiko dan mengevaluasi kembali penyesuaian strategi dengan kondisi pasar yang mungkin sedang tidak ideal (Sideways/Konsolidasi)." },
  { judul: "Pemanfaatan Indikator vs Price Action", isi: "Meskipun indikator (Moving Average, RSI, MACD) dapat membantu, mereka selalu bersifat terlambat (Lagging) karena dihitung dari data harga masa lalu. Institute Trading menekankan pentingnya penguasaan Price Action murni (Membaca harga telanjang), karena harga itu sendiri adalah indikator tercepat dan paling jujur di pasar." },
  { judul: "Komitmen Pertumbuhan (Compounding)", isi: "Berfokuslah pada persentase pertumbuhan bulanan yang serealistis mungkin (5% - 10%), bukan melipatgandakan akun dalam semalam. Keajaiban efek bunga majemuk (Compounding) akan mengubah pertumbuhan kecil yang persisten menjadi akumulasi kekayaan yang luar biasa hebat dalam rentang waktu bertahun-tahun." }
];

const kontainer = document.getElementById("kontainer-materi");
let htmlMateri = "";

dataMateri.forEach((item, index) => {
  htmlMateri += `
  <div class="rule">
    <h4>Modul ${index + 1}: ${item.judul}</h4>
    <p>${item.isi}</p>
  </div>
  `;
});

kontainer.innerHTML = htmlMateri;
</script>

</body>
</html>
