<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vegas Cafe Bar | Desayunos y Brunch en Granada</title>

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800&display=swap" rel="stylesheet">

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
  font-family:'Montserrat',system-ui,sans-serif;
}

body{
  background:#f5f5f5;
  color:#333;
  padding-top:70px;
}

/* HEADER */
header{
  position:fixed;
  top:0;
  width:100%;
  background:#141010;
  z-index:100;
  padding:.8rem;
  text-align:center;
}

nav button{
  background:#1f1717;
  color:#fff;
  border:1px solid #c47a4a;
  padding:.5rem 1.2rem;
  margin:.2rem;
  border-radius:25px;
  cursor:pointer;
  font-weight:600;
}

nav button:hover,
nav button.active{
  background:#c47a4a;
}

/* SECTIONS */
section{
  display:none;
  padding:5rem 1rem;
  max-width:1200px;
  margin:auto;
}

/* HERO */
#hero{
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  min-height:100vh;
  background:
    linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
    url("https://images.unsplash.com/photo-1509042239860-f550ce710b93?auto=format&fit=crop&w=1600&q=80");
  background-size:cover;
  background-position:center;
  color:#fff;
  text-align:center;
}

/* LOGO */
.logo{
  background:rgba(0,0,0,.65);
  padding:3rem 3.8rem;
  border-radius:26px;
}

.logo h1{
  font-size:3.8rem;
  font-weight:800;
  letter-spacing:.15em;
}

.logo span{
  display:block;
  margin-top:.8rem;
  font-size:1rem;
  letter-spacing:.25em;
  color:#f2c27d;
}

@media(max-width:600px){
  .logo h1{font-size:2.6rem;}
  .logo{padding:2rem;}
}

/* QR BUTTON */
.hero-qr{
  margin-top:2rem;
  background:linear-gradient(45deg,#c47a4a,#e6b17a);
  color:#fff;
  border:none;
  padding:1rem 3rem;
  border-radius:45px;
  font-size:1.1rem;
  font-weight:700;
  cursor:pointer;
  box-shadow:0 14px 35px rgba(0,0,0,.45);
}

.hero-qr:hover{
  transform:scale(1.05);
}

/* TITLES */
h2{
  text-align:center;
  font-size:2.4rem;
  margin-bottom:1.5rem;
}

/* NOSOTROS */
#info p{
  max-width:820px;
  margin:auto;
  text-align:center;
  font-size:1.05rem;
  color:#555;
  line-height:1.6;
}

/* MENU */
.menu-category{
  margin-bottom:4.5rem;
}

.menu-category h3{
  text-align:center;
  font-size:2rem;
  margin-bottom:2.2rem;
  color:#5a3a27;
}

.menu-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
  gap:1.8rem;
}

.menu-item{
  background:#fff;
  border-radius:20px;
  padding:1.2rem;
  text-align:center;
  box-shadow:0 8px 22px rgba(0,0,0,.1);
}

.menu-item img{
  width:100%;
  height:170px;
  object-fit:cover;
  border-radius:14px;
}

.menu-item h4{
  margin:.8rem 0 .3rem;
  font-size:1.15rem;
}

.menu-item p{
  font-size:.95rem;
  color:#666;
}

.price{
  margin-top:.5rem;
  font-weight:800;
  color:#c47a4a;
}

/* CONTACT */
#contact{
  text-align:center;
}

.instagram-btn{
  display:inline-block;
  margin-top:1.2rem;
  background:linear-gradient(45deg,#f09433,#dc2743,#bc1888);
  color:#fff;
  padding:.85rem 2rem;
  border-radius:35px;
  text-decoration:none;
  font-weight:700;
}

/* QR */
#qrBox{
  display:none;
  margin-top:2.2rem;
}

#qrBox img{
  background:#fff;
  padding:16px;
  border-radius:18px;
  box-shadow:0 12px 30px rgba(0,0,0,.35);
}

/* FOOTER */
footer{
  background:#141010;
  color:#fff;
  text-align:center;
  padding:1.5rem;
}
</style>
</head>

<body>

<header>
<nav>
<button onclick="showSection('hero',this)">Inicio</button>
<button onclick="showSection('info',this)">Nosotros</button>
<button onclick="showSection('menu',this)">Menu</button>
<button onclick="showSection('contact',this)">Contacto</button>
</nav>
</header>

<section id="hero">
  <div class="logo">
    <h1>VEGAS CAFE BAR</h1>
    <span>DESAYUNOS BRUNCH CAFE</span>
  </div>

  <button class="hero-qr" onclick="openQR()">ESCANEAR MENU QR</button>
</section>

<section id="info">
<h2>Nuestra esencia</h2>
<p>
En Vegas Cafe Bar apostamos por el cafe de calidad, los ingredientes frescos
y un ambiente acogedor que invita a quedarse. Ofrecemos desayunos y brunch
cuidadosamente elaborados en pleno centro de Granada.
</p>
</section>

<section id="menu">

<div class="menu-category">
<h3>Cafes</h3>
<div class="menu-grid">
<div class="menu-item"><img src="https://www.baque.com/wp-content/uploads/2020/06/variedad-taza-de-caf%C3%A9.jpg" alt="Espresso"><h4>Espresso</h4><p>Cafe intenso y aromatico</p><div class="price">1.80 EUR</div></div>
<div class="menu-item"><img src="https://cafesmoreno.com/wp-content/uploads/2024/06/Cafe-con-leche.png" alt="Cafe con leche"><h4>Cafe con Leche</h4><p>Equilibrio perfecto entre cafe y leche</p><div class="price">2.20 EUR</div></div>
<div class="menu-item"><img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93" alt="Cappuccino"><h4>Cappuccino</h4><p>Espuma cremosa y sabor suave</p><div class="price">2.80 EUR</div></div>
<div class="menu-item"><img src="https://www.coopeldos.com/wp-content/uploads/2020/06/cafeLatteConSabor.jpg.webp" alt="Latte"><h4>Latte</h4><p>Cremoso y equilibrado</p><div class="price">2.50 EUR</div></div>
</div>
</div>

<div class="menu-category">
<h3>Desayunos</h3>
<div class="menu-grid">
<div class="menu-item"><img src="https://images.unsplash.com/photo-1551183053-bf91a1d81141" alt="Tostada de aguacate"><h4>Tostada de Aguacate</h4><p>Pan artesanal con aguacate y semillas</p><div class="price">4.50 EUR</div></div>
<div class="menu-item"><img src="https://images.unsplash.com/photo-1617191519105-d07b98d82fda" alt="Tostada de salmon"><h4>Tostada de Salmon</h4><p>Queso crema y salmon ahumado</p><div class="price">6.50 EUR</div></div>
<div class="menu-item"><img src="https://images.unsplash.com/photo-1493770348161-369560ae357d" alt="Tostada clasica"><h4>Tostada Clasica</h4><p>Aceite de oliva y tomate natural</p><div class="price">2.80 EUR</div></div>
</div>
</div>

<div class="menu-category">
<h3>Brunch</h3>
<div class="menu-grid">
<div class="menu-item"><img src="https://images.unsplash.com/photo-1525351484163-7529414344d8" alt="Huevos benedict"><h4>Huevos Benedict</h4><p>Huevos pochados con salsa holandesa</p><div class="price">7.90 EUR</div></div>
<div class="menu-item"><img src="https://images.unsplash.com/photo-1490645935967-10de6ba17061" alt="Pancakes"><h4>Pancakes</h4><p>Con fruta fresca y sirope</p><div class="price">6.90 EUR</div></div>
</div>
</div>

</section>

<section id="contact">
<h2>Visitanos</h2>
<p>
Calle Gracia 32, Granada<br>
Telefono 697245373<br>
Horario de 09:00 a 14:00
</p>

<a class="instagram-btn" href="https://www.instagram.com/cafe.vegas.granada" target="_blank">
Instagram
</a>

<div id="qrBox">
<img src="https://api.qrserver.com/v1/create-qr-code/?size=260x260&data=https://www.instagram.com/cafe.vegas.granada">
<p style="margin-top:10px;color:#555;">Escanea para ver el menu</p>
</div>
</section>

<footer>
2026 Vegas Cafe Bar Granada
</footer>

<script>
function showSection(id,btn){
  document.querySelectorAll("section").forEach(s=>s.style.display="none");
  document.getElementById(id).style.display="block";
  document.getElementById("qrBox").style.display="none";
  document.querySelectorAll("nav button").forEach(b=>b.classList.remove("active"));
  if(btn) btn.classList.add("active");
  window.scrollTo({top:0,behavior:"smooth"});
}

function openQR(){
  showSection("contact");
  setTimeout(function(){
    document.getElementById("qrBox").style.display="block";
  },300);
}

showSection("hero");
</script>

</body>
</html>
