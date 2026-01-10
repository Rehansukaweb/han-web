<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Farhan Store</title>
<style>
body{margin:0;font-family:Arial;background:#0f172a;color:#fff}
header{padding:14px;text-align:center;font-size:22px;background:#020617}
input,button{padding:10px;border-radius:10px;border:none}
button{background:#22c55e;font-weight:bold;cursor:pointer}
.hidden{display:none}
.card{background:#020617;padding:14px;border-radius:14px;margin:10px 0}
nav button{margin:4px}
</style>
</head>

<body>

<header>🛒 FARHAN STORE</header>

<!-- LOGIN -->
<div id="login" class="card">
<h3>Login</h3>
<input id="user" placeholder="Username"><br><br>
<input id="pass" type="password" placeholder="Password"><br><br>
<button onclick="login()">Masuk</button>
<p>Admin: admin / admin</p>
</div>

<!-- USER SHOP -->
<div id="shop" class="hidden">
<nav>
<button onclick="showShop()">Toko</button>
<button onclick="showCart()">Keranjang</button>
<button onclick="logout()">Logout</button>
</nav>

<div id="products">
<div class="card">
<h4>Joki FF</h4>
<p>Rp25.000</p>
<button onclick="add(25000)">Tambah</button>
</div>
<div class="card">
<h4>Joki ML</h4>
<p>Rp30.000</p>
<button onclick="add(30000)">Tambah</button>
</div>
<div class="card">
<h4>Room Wangi</h4>
<p>Rp20.000</p>
<button onclick="add(20000)">Tambah</button>
</div>
</div>

<div id="cart" class="hidden card">
<h3>Keranjang</h3>
<p>Total: Rp <span id="total">0</span></p>
<button onclick="pay()">Bayar via QRIS</button>
</div>
</div>

<!-- ADMIN PANEL -->
<div id="admin" class="hidden card">
<h3>Admin Panel</h3>
<p>Total Transaksi: <span id="orders">0</span></p>
<button onclick="logout()">Logout</button>
</div>

<script>
let total=0;
let orders=localStorage.getItem("orders")||0;

function login(){
let u=user.value,p=pass.value;
if(u==="admin"&&p==="admin"){
loginDiv(false);admin.classList.remove("hidden");
}else{
loginDiv(false);shop.classList.remove("hidden");
}
}

function loginDiv(x){login.classList.toggle("hidden",!x)}

function logout(){location.reload()}

function add(h){total+=h;document.getElementById("total").innerText=total}

function showCart(){cart.classList.remove("hidden");products.classList.add("hidden")}
function showShop(){products.classList.remove("hidden");cart.classList.add("hidden")}

function pay(){
if(total===0){alert("Keranjang kosong");return}
orders++;localStorage.setItem("orders",orders);
window.open("https://wa.me/6285717426626?text=Halo%20Farhan%20Store,%20saya%20bayar%20Rp"+total);
}

document.getElementById("orders").innerText=orders;
</script>

</body>
</html>
