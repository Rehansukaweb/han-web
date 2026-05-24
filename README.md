<!DOCTYPE html>
<html lang="id" translate="no">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<meta name="google" content="notranslate">
<title>IT - Institute Trading</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
scroll-behavior:smooth;
}

body{
font-family:'Poppins',sans-serif;
background:#080a0f;
overflow-x:hidden;
color:#f1f5f9;
}

/* NAVBAR */
header{
position:fixed;
top:0;
left:0;
width:100%;
padding:20px 7%;
display:flex;
justify-content:space-between;
align-items:center;
background:rgba(8, 10, 15, 0.85);
backdrop-filter:blur(14px);
z-index:1000;
border-bottom:1px solid rgba(255,255,255,0.05);
transition:0.3s;
}

.logo{
display:flex;
align-items:center;
gap:16px;
}

.logo-img{
width:55px;
height:55px;
object-fit:cover;
border-radius:12px;
border:1px solid rgba(255,255,255,0.1);
box-shadow:0 0 20px rgba(0, 210, 255, 0.2);
}

.logo h2{
font-size:1.6rem;
color:#ffffff;
font-weight:700;
}

.logo h2 span{
color:#00b140;
}

nav{
display:flex;
gap:35px;
}

nav a{
text-decoration:none;
color:#cbd5e1;
font-weight:600;
transition:0.3s;
font-size:1.1rem;
}

nav a:hover{
color:#00d2ff;
}

/* HERO */
.hero{
min-height:100vh;
padding:180px 7% 100px;
display:grid;
grid-template-columns:1.2fr 1fr;
align-items:center;
gap:60px;
background:
radial-gradient(circle at top left, rgba(0, 210, 255, 0.1) 0%, transparent 40%),
radial-gradient(circle at bottom right, rgba(0, 177, 64, 0.1) 0%, transparent 35%);
}

.badge{
display:inline-block;
padding:12px 24px;
background:rgba(0, 210, 255, 0.1);
color:#00d2ff;
font-weight:700;
border-radius:50px;
margin-bottom:25px;
border:1px solid rgba(0, 210, 255, 0.2);
font-size:1rem;
}

.hero h1{
font-size:4.5rem;
line-height:1.15;
margin-bottom:25px;
font-weight:800;
color:#ffffff;
}

.hero h1 span{
background: linear-gradient(135deg, #00b140, #00d2ff);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
}

.hero p{
font-size:1.2rem;
line-height:1.8;
color:#94a3b8;
max-width:700px;
margin-bottom:40px;
}

.hero-buttons{
display:flex;
gap:20px;
flex-wrap:wrap;
}

.btn{
padding:18px 38px;
border-radius:16px;
text-decoration:none;
font-weight:700;
transition:0.3s;
display: inline-block;
font-size:1.1rem;
}

.btn-primary{
background:linear-gradient(135deg,#00b140,#00ff88);
color:#080a0f;
box-shadow:0 10px 30px rgba(0,177,64,0.3);
}

.btn-primary:hover{
transform:translateY(-5px);
box-shadow:0 15px 40px rgba(0,177,64,0.4);
}

.btn-secondary{
border:2px solid rgba(255,255,255,0.2);
color:#ffffff;
background:rgba(255,255,255,0.05);
}

.btn-secondary:hover{
background:rgba(255,255,255,0.1);
transform:translateY(-5px);
}

.btn-tiktok{
background:linear-gradient(135deg,#111,#222);
color:white;
border:1px solid rgba(255,255,255,0.1);
box-shadow:0 10px 30px rgba(0,0,0,0.5);
}
.btn-tiktok:hover{
transform:translateY(-5px);
color:#00ff88;
border-color:#00b140;
}

/* HERO RIGHT */
.hero-card{
background:rgba(18, 22, 32, 0.7);
backdrop-filter:blur(20px);
padding:45px;
border-radius:35px;
box-shadow:0 20px 60px rgba(0,0,0,0.4);
border:1px solid rgba(255,255,255,0.05);
position:relative;
overflow:hidden;
animation:floating 4s ease-in-out infinite;
}

.hero-card::before{
content:'';
position:absolute;
width:250px;
height:250px;
background:linear-gradient(135deg,#00d2ff,#00b140);
top:-100px;
right:-100px;
border-radius:50%;
opacity:0.15;
}

.hero-card h2{
font-size:2rem;
margin-bottom:30px;
color:#ffffff;
}

.stat-box{
background:rgba(255,255,255,0.03);
padding:25px;
border-radius:20px;
margin-bottom:20px;
border:1px solid rgba(255,255,255,0.05);
}

.stat-box h3{
font-size:2.2rem;
color:#00ff88;
}

.stat-box p{
font-size:1.1rem;
color:#cbd5e1;
}

.progress{
width:100%;
height:16px;
background:rgba(255,255,255,0.05);
border-radius:50px;
overflow:hidden;
margin-top:20px;
}

.progress-fill{
height:100%;
width:90%;
background:linear-gradient(90deg,#00b140,#00d2ff);
border-radius:50px;
animation:grow 4s infinite alternate;
}

.progress-text{
margin-top:15px;
font-weight:600;
color:#00d2ff;
font-size:1.1rem;
}

/* SECTION */
section{
padding:120px 7%;
}

.section-title{
text-align:center;
margin-bottom:70px;
}

.section-title span{
color:#00d2ff;
font-weight:700;
letter-spacing:2px;
font-size:1.1rem;
text-transform:uppercase;
}

.section-title h2{
font-size:3.2rem;
margin-top:15px;
color:#ffffff;
}

/* GRID */
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(320px,1fr));
gap:40px;
}

/* CARD */
.card{
background:#111520;
padding:45px;
border-radius:30px;
border:1px solid rgba(255,255,255,0.05);
box-shadow:0 10px 40px rgba(0,0,0,0.2);
transition:0.4s;
position:relative;
overflow:hidden;
}

.card:hover{
transform:translateY(-10px);
border-color:rgba(0, 210, 255, 0.3);
}

.card h3{
margin-bottom:20px;
font-size:1.8rem;
color:#ffffff;
}

.card p{
color:#94a3b8;
line-height:1.8;
font-size:1.1rem;
}

/* ACCORDION PROGRAM */
.accordion-wrapper {
max-width: 1000px;
margin: 0 auto;
display: flex;
flex-direction: column;
gap: 25px;
}

.accordion-btn {
background: #111520;
padding: 35px 40px;
border-radius: 25px;
border: 1px solid rgba(255,255,255,0.05);
box-shadow: 0 10px 40px rgba(0,0,0,0.2);
width: 100%;
text-align: left;
font-size: 1.6rem;
font-weight: 700;
font-family: 'Poppins', sans-serif;
cursor: pointer;
transition: 0.4s;
color: #ffffff;
display: flex;
justify-content: space-between;
align-items: center;
}

.accordion-btn:hover {
transform: translateY(-5px);
border-color: rgba(255,255,255,0.1);
}

.accordion-btn.premium-acc {
background: linear-gradient(135deg,#161e2e,#111520);
border: 1px solid rgba(0, 210, 255, 0.3);
}

.accordion-btn.premium-acc span {
color: #e5a93c;
}

.accordion-content {
padding: 0 40px;
background: #0d1017;
border-radius: 0 0 25px 25px;
max-height: 0;
overflow: hidden;
transition: max-height 0.3s ease-out, padding 0.3s ease-out;
margin-top: -25px;
border: 1px solid rgba(255,255,255,0.02);
border-top: none;
}

.accordion-content p {
color: #94a3b8;
line-height: 1.8;
padding: 45px 0 25px 0;
font-size: 1.15rem;
}

/* RULE (MATERI EDUKASI) */
.rules{
display:grid;
gap:25px;
max-width:1000px;
margin:auto;
}

.rule{
background:#111520;
padding:35px 40px;
border-radius:20px;
box-shadow:0 10px 40px rgba(0,0,0,0.2);
transition:0.3s;
border: 1px solid rgba(255,255,255,0.05);
border-left: 6px solid #00b140;
}

.rule:hover{
transform:translateY(-5px);
border-color: rgba(255,255,255,0.1);
border-left-color: #00d2ff;
}

.rule h4 {
color: #ffffff;
font-size: 1.5rem;
margin-bottom: 15px;
font-weight: 700;
}

.rule p {
color: #94a3b8;
line-height: 1.8;
font-size: 1.15rem;
}

/* CONTACT */
.contact-box{
max-width:800px;
margin:auto;
background:#111520;
padding:60px;
border-radius:35px;
text-align:center;
box-shadow:0 15px 50px rgba(0,0,0,0.4);
border: 3px dashed rgba(0, 210, 255, 0.3);
}

.contact-box h3{
font-size:3rem;
margin:20px 0;
color:#00ff88;
}

/* FOOTER */
footer{
background:#06080c;
padding:60px 20px;
text-align:center;
color:#94a3b8;
border-top:1px solid rgba(255,255,255,0.05);
}

footer h2{
margin-bottom:10px;
color:#ffffff;
font-size:1.8rem;
}

footer p {
font-size:1.1rem;
}

/* ANIMATION */
@keyframes floating{
0%,100%{ transform:translateY(0); }
50%{ transform:translateY(-15px); }
}

@keyframes grow{
from{ width:60%; }
to{ width:90%; }
}

/* RESPONSIVE UNTUK HP DAN TABLET */
@media(max-width:1100px){
.hero{grid-template-columns:1fr; padding-top:150px; gap:50px;}
.hero h1{font-size:3.8rem;}
nav{display:none;}
}

@media(max-width:600px){
section {padding: 80px 5%;}
.hero{padding-top: 130px;}
.hero h1{font-size: 2.8rem;}
.hero p {font-size: 1.05rem;}
.section-title h2{font-size:2.2rem;}
.btn{width:100%; text-align:center; padding: 15px 20px;}
.hero-card {padding: 30px;}
.card, .rule {padding: 25px 25px;}
.rule h4 {font-size: 1.3rem;}
.rule p {font-size: 1rem;}
.accordion-btn {font-size: 1.2rem; padding: 25px;}
.contact-box{padding:40px 20px;}
.contact-box h3 {font-size: 2.2rem;}
}
</style>
</head>

<body>

<header>
<div class="logo">
<img src="LOGO INTITUTE TRADING.jpeg" alt="Institute Trading Logo" class="logo-img">
<h2>Institute <span>Trading</span></h2>
</div>
<nav>
<a href="#home">Home</a>
<a href="#about">Tentang</a>
<a href="#program">Program</a>
<a href="#materi">Edukasi</a>
<a href="#rules">Rules</a>
<a href="#contact">Kontak</a>
</nav>
</header>

<section class="hero" id="home">
<div>
<div class="badge">#1 Trading Education Platform</div>
<h1>Menciptakan <span>Trader Muda</span> Yang Disiplin, Sehat & Sukses</h1>
<p>Institute Trading hadir untuk membangun trader muda profesional dengan mindset kuat, money management sehat, dan risk management yang disiplin agar mampu menjadi trader sukses dan financial freedom.</p>
<div class="hero-buttons">
<a href="https://wa.me/6285717426626" class="btn btn-primary">Gabung Sekarang</a>
<a href="#program" class="btn btn-secondary">Lihat Program</a>
</div>
</div>
<div class="hero-card">
<h2>TRADER SUCCESS SYSTEM</h2>
<div class="stat-box"><h3>90%</h3><p>Risk Management & Psikologi</p></div>
<div class="stat-box"><h3>10%</h3><p>Entry Strategy</p></div>
<div class="progress"><div class="progress-fill"></div></div>
<div class="progress-text">Healthy Growth & Consistency</div>
</div>
</section>

<section id="about">
<div class="section-title">
<span>TENTANG KAMI</span>
<h2>Institute Trading Modern</h2>
</div>
<div class="grid">
<div class="card"><h3>Mindset Trader</h3><p>Melatih trader muda agar memiliki mental disiplin, tidak emosional, dan fokus pada konsistensi.</p></div>
<div class="card"><h3>Money Management</h3><p>Mengajarkan pengelolaan modal profesional agar akun tetap sehat dan berkembang stabil.</p></div>
<div class="card"><h3>Risk Management</h3><p>Strategi pembatasan kerugian untuk menjaga longevity dalam dunia trading.</p></div>
</div>
</section>

<section id="program">
<div class="section-title">
<span>PROGRAM</span>
<h2>Program Unggulan</h2>
<p style="margin-top: 10px; color: #94a3b8; font-size: 1.1rem;">Klik pada program untuk melihat detailnya 👇</p>
</div>
<div class="accordion-wrapper">
    <div>
        <button class="accordion-btn">📉 Basic Trading <span>+</span></button>
        <div class="accordion-content">
            <p>Belajar market structure, candlestick, support resistance, dan dasar analisis market. Sangat cocok untuk pemula yang ingin belajar dari nol dengan pondasi yang benar.</p>
        </div>
    </div>
    <div>
        <button class="accordion-btn premium-acc">👑 Professional Trading (BEST) <span>+</span></button>
        <div class="accordion-content">
            <p>Belajar Smart Money Concept (SMC), institutional trading, psychology, dan risk management profesional. Setup entry yang lebih tajam layaknya institusi besar.</p>
        </div>
    </div>
    <div>
        <button class="accordion-btn">🚀 Millionaire Trader <span>+</span></button>
        <div class="accordion-content">
            <p>Mentoring elite untuk membangun trader sukses dan financial freedom jangka panjang. Pendampingan eksklusif untuk menjaga konsistensi profit Anda.</p>
        </div>
    </div>
</div>
</section>

<section id="materi">
<div class="section-title">
<span>EDUKASI</span>
<h2>Perpustakaan Ilmu Trading</h2>
<p style="margin-top: 10px; color: #94a3b8; font-size: 1.1rem;">Pelajari dasar-dasar trading gratis dari Institute Trading.</p>
</div>
<div id="kontainer-materi" class="rules"></div>
</section>

<section id="rules">
<div class="section-title">
<span>RULES</span>
<h2>Trader Sehat & Disiplin</h2>
</div>
<div class="rules">
<div class="rule" style="font-weight:bold; border-left-color: #00ff88;">✅ Maksimal Risk 1-2% Per Entry</div>
<div class="rule" style="font-weight:bold; border-left-color: #00ff88;">✅ Selalu Gunakan Stop Loss</div>
<div class="rule" style="font-weight:bold; border-left-color: #00ff88;">✅ Hindari Overtrading</div>
<div class="rule" style="font-weight:bold; border-left-color: #00ff88;">✅ Fokus Pada Konsistensi</div>
<div class="rule" style="font-weight:bold; border-left-color: #00ff88;">✅ Utamakan Psikologi Trading</div>
</div>
</section>

<section id="contact">
<div class="section-title">
<span>KONTAK</span>
<h2>Hubungi Kami</h2>
</div>
<div class="contact-box">
<h2 style="font-size: 2.5rem; color:#ffffff; margin-bottom: 10px;">TANYA JAWAB <span style="color:#00ff88;">DI WA</span></h2>
<p style="color:#94a3b8; font-size:1.2rem;">Konsultasi langsung dengan mentor kami sekarang juga!</p>
<h3>085717426626</h3>
<div style="display:flex; justify-content:center; gap:20px; flex-wrap:wrap; margin-top:40px;">
    <a href="https://wa.me/6285717426626" class="btn btn-primary">📱 Chat WhatsApp</a>
    <a href="https://www.tiktok.com/@itrading.com?_r=1&_t=ZS-96cThJJNePC" target="_blank" class="btn btn-tiktok">🎵 TikTok: @itrading.com</a>
</div>
</div>
</section>

<footer>
<h2>IT - Institute Trading</h2>
<p>Healthy Trader • Discipline • Financial Freedom</p>
</footer>

<script>
// 1. EFEK NAVBAR SAAT SCROLL
window.addEventListener('scroll',()=>{
    const header=document.querySelector('header');
    if(window.scrollY > 50){ 
        header.style.background='rgba(8, 10, 15, 0.95)';
        header.style.boxShadow='0 10px 30px rgba(0,0,0,0.5)'; 
    }
    else{ 
        header.style.background='rgba(8, 10, 15, 0.85)';
        header.style.boxShadow='none'; 
    }
});

// 2. ACCORDION FUNGSI
var acc = document.getElementsByClassName("accordion-btn");
for (var i = 0; i < acc.length; i++) {
  acc[i].addEventListener("click", function() {
    var content = this.nextElementSibling;
    var span = this.querySelector('span');
    
    if (content.style.maxHeight) {
      content.style.maxHeight = null;
      content.style.padding = "0 40px";
      span.innerHTML = "+";
    } else {
      content.style.maxHeight = content.scrollHeight + 80 + "px";
      content.style.padding = "0 40px 30px 40px";
      span.innerHTML = "−";
    }
  });
}

// 3. DATA MATERI EDUKASI (Spasi invisible sudah dibersihkan)
const dataMateri = [
    {
        judul: "1. Apa itu Trading Forex & Saham?",
        isi: "Trading adalah kegiatan jual beli aset keuangan seperti mata uang (forex), saham, atau kripto di pasar finansial. Tujuannya adalah mendapatkan keuntungan dari selisih harga beli dan harga jual. Berbeda dengan investasi jangka panjang, trading berfokus pada pergerakan harga dalam jangka pendek atau menengah."
    },
    {
        judul: "2. Membaca Candlestick Dasar",
        isi: "Candlestick adalah visualisasi pergerakan harga. Candle hijau (Bullish) menunjukkan harga penutupan lebih tinggi dari pembukaan, artinya pembeli mendominasi. Candle merah (Bearish) menunjukkan harga penutupan lebih rendah, artinya penjual mendominasi. Sumbu (wick) menunjukkan harga tertinggi dan terendah pada periode waktu tersebut."
    },
    {
        judul: "3. Support dan Resistance (SNR)",
        isi: "Support adalah area 'lantai' di mana harga sering memantul naik karena banyaknya minat beli. Resistance adalah area 'atap' di mana harga sering memantul turun karena tingginya minat jual. Mengetahui SNR membantu trader menentukan area entry dan exit yang logis."
    },
    {
        judul: "4. Trend is Your Friend (Uptrend & Downtrend)",
        isi: "Uptrend ditandai dengan terbentuknya pola Higher High (HH) dan Higher Low (HL). Downtrend ditandai dengan Lower High (LH) dan Lower Low (LL). Kesalahan terbesar pemula adalah melawan arah tren besar. Selalu cari peluang Buy di saat Uptrend dan Sell di saat Downtrend."
    },
    {
        judul: "5. Risk Management (Sangat Penting!)",
        isi: "Risk management adalah tameng pelindung akun Anda. Rule nomor satu di Institute Trading: Jangan pernah merisikokan lebih dari 1% hingga 2% modal Anda dalam satu transaksi. Jika Anda punya $1000, maksimal kerugian per transaksi hanyalah $10-$20."
    },
    {
        judul: "6. Selalu Gunakan Stop Loss (SL)",
        isi: "Stop Loss adalah pembatas kerugian otomatis. Trading tanpa Stop Loss sama seperti mengendarai mobil berkecepatan tinggi tanpa rem. SL melindungi modal Anda dari pergerakan pasar yang ekstrem atau berita fundamental yang tak terduga."
    },
    {
        judul: "7. Risk to Reward Ratio (RRR)",
        isi: "RRR membandingkan potensi kerugian dengan potensi keuntungan. RRR minimal yang sehat adalah 1:2. Artinya, jika Anda merisikokan $10 (SL), target keuntungan Anda harus $20 (TP). Dengan RRR 1:2, win rate 40% saja sudah bisa membuat akun Anda profit."
    },
    {
        judul: "8. Supply and Demand (SND)",
        isi: "Hukum ekonomi dasar berlaku di market. Area Supply adalah titik di mana penjual (institusi) meninggalkan pesanan besar yang menyebabkan harga drop drastis (Drop-Base-Drop). Area Demand adalah tempat harga rally naik secara agresif (Rally-Base-Rally). Ini adalah strategi andalan trader pro."
    },
    {
        judul: "9. Market Structure (BOS & CHoCH)",
        isi: "BOS (Break of Structure) terjadi saat tren berlanjut menembus High/Low sebelumnya. CHoCH (Change of Character) adalah sinyal awal bahwa tren mungkin akan berbalik arah. Memahami struktur pasar menghindarkan Anda dari entry di waktu yang salah."
    },
    {
        judul: "10. Pengenalan Smart Money Concept (SMC)",
        isi: "SMC mengajarkan kita untuk mengikuti jejak Institusi Besar (Bank/Hedge Fund). Institusi membutuhkan Likuiditas besar untuk masuk market. Oleh karena itu, harga sering kali menyentuh Stop Loss trader ritel (Liquidity Sweep) sebelum akhirnya terbang sesuai analisa awal."
    },
    {
        judul: "11. Imbalance / Fair Value Gap (FVG)",
        isi: "Ketika ada pergerakan harga yang sangat cepat dan kuat (biasanya dari institusi), pasar sering meninggalkan area 'kosong' atau tidak seimbang (Imbalance). Harga cenderung akan kembali ke area ini di masa depan untuk menyeimbangkan pesanan sebelum melanjutkan trennya."
    },
    {
        judul: "12. Psikologi Trading: Bahaya FOMO",
        isi: "FOMO (Fear of Missing Out) adalah perasaan takut tertinggal peluang. Ini membuat trader entry tergesa-gesa tanpa konfirmasi, membeli di pucuk atau menjual di lembah. Trader sukses sabar menunggu harga datang ke area setup-nya, bukan mengejar harga yang sedang lari."
    },
    {
        judul: "13. Overtrading: Penyakit Utama Pemula",
        isi: "Overtrading adalah kondisi di mana Anda membuka terlalu banyak posisi dalam sehari, seringkali dipicu oleh emosi setelah Loss (Revenge Trading). Di Institute Trading, kami menyarankan maksimal 2-3 kali entry per hari. Jika sudah loss batas harian, tutup chart dan istirahat."
    },
    {
        judul: "14. Pentingnya Trading Journal",
        isi: "Bisnis tanpa pembukuan pasti akan hancur. Trading journal berfungsi untuk mencatat alasan Anda entry, screenshot setup chart, emosi yang dirasakan, dan hasil akhir (Profit/Loss). Dari jurnal inilah Anda bisa mengevaluasi strategi mana yang paling efektif."
    },
    {
        judul: "15. Memahami Multi-Timeframe Analysis",
        isi: "Jangan hanya melihat satu timeframe. Gunakan Timeframe Besar (H4/Daily) untuk melihat arah tren utama. Gunakan Timeframe Sedang (H1/M15) untuk melihat struktur pasar. Lalu gunakan Timeframe Kecil (M5/M1) untuk mencari konfirmasi entry yang presisi dengan risiko sekecil mungkin."
    },
    {
        judul: "16. Likuiditas: Menjadi Mangsa atau Pemangsa?",
        isi: "Di market, jika Anda tidak bisa melihat di mana letak likuiditas (kumpulan Stop Loss trader lain), kemungkinan besar Andalah likuiditas tersebut. Hindari entry di area Support/Resistance yang terlalu jelas (Equal Highs/Equal Lows) sebelum area tersebut di-sweep (dibersihkan) oleh market maker."
    },
    {
        judul: "17. Mengelola Emosi Saat Floating Minus",
        isi: "Melihat angka merah di akun bisa memicu kepanikan. Jika Anda sudah menggunakan Lot yang sesuai (Risk 1%) dan sudah memasang Stop Loss, biarkan sistem yang bekerja. Jangan pernah menggeser-geser SL untuk memperlebar kerugian dengan harapan harga akan berbalik."
    },
    {
        judul: "18. Konsistensi Jauh Lebih Penting dari Profit Besar",
        isi: "Mendapatkan profit 100% dalam sehari itu mudah, itu namanya judi. Mempertahankan profit 5-10% setiap bulan selama bertahun-tahun itulah yang dinamakan trader profesional. Fokuslah pada persentase pertumbuhan, bukan nominal uang di awal karir."
    },
    {
        judul: "19. Menghadapi Drawdown (Masa Rugi Beruntun)",
        isi: "Semua trader, bahkan yang profesional sekalipun, pasti akan mengalami Drawdown (rentetan Loss). Cara bertahan dari masa ini adalah dengan mengurangi ukuran Lot Anda sementara waktu sampai Anda kembali selaras dengan ritme pergerakan pasar (kembali profit)."
    },
    {
        judul: "20. Langkah Selanjutnya: Belajar Bersama Mentor",
        isi: "Belajar otodidak itu bagus, namun belajar bersama mentor akan memangkas waktu trial & error Anda bertahun-tahun. Kami di Institute Trading siap membimbing Anda dari nol hingga bisa menganalisa market secara mandiri. Punya pertanyaan? Langsung TANYA JAWAB DI WA!"
    }
];

const kontainer = document.getElementById("kontainer-materi");
let htmlMateri = "";

dataMateri.forEach(item => {
    htmlMateri += `
    <div class="rule">
        <h4>📚 ${item.judul}</h4>
        <p>${item.isi}</p>
    </div>
    `;
});

kontainer.innerHTML = htmlMateri;
</script>

</body>
</html>
