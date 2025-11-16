# La-Panera-Verde
Emprendimiento de pastelería libre de gluten
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>La Panera Verde - Pastelería Sin TACC</title>

<style>
/* -------------------------------- */
/*          ESTILOS GLOBALES        */
/* -------------------------------- */
body {
    margin: 0;
    font-family: "Poppins", sans-serif;
    background: linear-gradient(to bottom right, #ffe6f2, #e8ffe8);
    animation: fadeIn 1s ease-in-out;
    color: #333;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

/* -------------------------------- */
/*            HEADER                 */
/* -------------------------------- */
header {
    background: linear-gradient(45deg, #A3D39C, #7fbf73);
    text-align: center;
    padding: 40px 20px;
    color: white;
    box-shadow: 0 4px 15px #00000040;
}

header h1 {
    margin: 0;
    font-size: 3em;
}

.slogan {
    font-size: 1.3em;
    font-style: italic;
    color: #ffe0ff;
}

/* -------------------------------- */
/*             CARRUSEL              */
/* -------------------------------- */
.carousel-container {
    width: 100%;
    max-width: 900px;
    margin: 35px auto;
    overflow: hidden;
    border-radius: 20px;
    box-shadow: 0 4px 20px #00000030;
}

.carousel {
    display: flex;
    animation: slide 15s infinite;
}

.carousel img {
    width: 100%;
    height: 360px;
    object-fit: cover;
}

@keyframes slide {
    0% { transform: translateX(0); }
    33% { transform: translateX(-100%); }
    66% { transform: translateX(-200%); }
    100% { transform: translateX(0); }
}

/* -------------------------------- */
/*        BOTÓN PEDIDOS YA          */
/* -------------------------------- */
.py-btn {
    background: #ff0033;
    color: white;
    padding: 14px 25px;
    display: block;
    width: 280px;
    margin: 20px auto;
    text-align: center;
    border-radius: 10px;
    font-size: 1.3em;
    text-decoration: none;
    box-shadow: 0 4px 10px #00000030;
    transition: 0.3s;
}

.py-btn:hover {
    background: #cc0028;
    transform: scale(1.05);
}

/* -------------------------------- */
/*            PRODUCTOS              */
/* -------------------------------- */
section.products {
    padding: 20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.product {
    background: rgba(255,255,255,0.7);
    backdrop-filter: blur(8px);
    width: 300px;
    margin: 15px;
    border-radius: 15px;
    box-shadow: 0 4px 15px #00000025;
    padding: 15px;
    text-align: center;
    transition: 0.3s;
}

.product:hover {
    transform: translateY(-5px);
}

.product img {
    width: 100%;
    height: 190px;
    border-radius: 10px;
    object-fit: cover;
}

.price {
    font-size: 1.5em;
    color: #ff3e91;
    margin-top: 10px;
}

.qty-box input {
    width: 60px;
    padding: 5px;
    margin-top: 8px;
}

.add-btn {
    margin-top: 10px;
    background-color: #ff66b3;
    color: white;
    border: none;
    padding: 10px 14px;
    border-radius: 7px;
    cursor: pointer;
    transition: 0.25s;
}

.add-btn:hover {
    background-color: #ff2a88;
}

/* -------------------------------- */
/*       CARRITO FLOTANTE           */
/* -------------------------------- */
.cart-btn {
    position: fixed;
    right: 20px;
    bottom: 20px;
    background: #ff66b3;
    color: white;
    padding: 12px;
    border-radius: 50px;
    text-decoration: none;
    font-size: 1.1em;
    box-shadow: 0 4px 10px #00000040;
    cursor: pointer;
}

#cart-modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #00000060;
    display: none;
    justify-content: center;
    align-items: center;
}

#cart-box {
    width: 90%;
    max-width: 450px;
    background: white;
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 4px 20px #00000060;
}

#cart-items p {
    border-bottom: 1px solid #ddd;
    padding: 8px 0;
}

/* -------------------------------- */
/*           WHATSAPP               */
/* -------------------------------- */
.whatsapp {
    position: fixed;
    left: 20px;
    bottom: 20px;
    background: #25D366;
    color: white;
    padding: 12px 15px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: bold;
}

/* -------------------------------- */
/*     PEDIDOS PERSONALIZADOS       */
/* -------------------------------- */
.custom-order-section {
    background: rgba(255,255,255,0.6);
    margin: 40px auto;
    padding: 25px;
    max-width: 900px;
    border-radius: 20px;
    box-shadow: 0 4px 20px #00000025;
    backdrop-filter: blur(6px);
    animation: fadeIn 1.2s ease;
}

.custom-order-section h2 {
    text-align: center;
    color: #ff3e91;
    margin-bottom: 5px;
}

.custom-desc {
    text-align: center;
    margin-bottom: 25px;
}

.custom-order-box {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.custom-order-box input,
.custom-order-box select,
.custom-order-box textarea {
    padding: 12px;
    border: 2px solid #ff9acc;
    border-radius: 10px;
    background: #fff;
    transition: 0.3s;
}

.custom-order-box input:focus,
.custom-order-box select:focus,
.custom-order-box textarea:focus {
    border-color: #ff3e91;
    box-shadow: 0 0 6px #ff3e9150;
}

.custom-btn {
    padding: 12px;
    background: #ff66b3;
    color: white;
    border-radius: 10px;
    border: none;
    font-size: 1.2em;
    cursor: pointer;
    transition: 0.3s;
}

.custom-btn:hover {
    background: #ff2a88;
    transform: scale(1.05);
}

/* -------------------------------- */
/*            FOOTER                */
/* -------------------------------- */
footer {
    margin-top: 30px;
    text-align: center;
    padding: 20px;
    background: #A3D39C;
    color: white;
}

/* Responsive */
@media (max-width: 600px){
    header h1 { font-size: 2.1em; }
    .product { width: 90%; }
    .carousel img { height: 250px; }
}
</style>
</head>
<body>

<header>
    <h1>La Panera Verde</h1>
    <p class="slogan">“Dulces momentos, sin gluten y con amor.”</p>
</header>

<!-- CARRUSEL -->
<div class="carousel-container">
    <div class="carousel">
        <!-- REEMPLAZÁ ESTAS IMÁGENES POR LAS TUYAS -->
        <img src="macarrones.png">
        <img src="croissant.png">
        <img src="roll.png">
        <img src="panera verde.jpg"
    </div>
</div>

<!-- PEDIR POR PEDIDOS YA -->
<a class="py-btn" href="https://www.pedidosya.com.ar" target="_blank">
    Pedir por PedidosYa
</a>

<!-- ----------------- PEDIDOS PERSONALIZADOS ----------------- -->
<section class="custom-order-section">
    <h2>✨ Pedidos Personalizados ✨</h2>
    <p class="custom-desc">Creá tu torta o postre sin TACC a tu gusto. Completá el formulario y nos pondremos en contacto.</p>

    <div class="custom-order-box">

        <label>Nombre completo:</label>
        <input type="text" id="custom-name">

        <label>Producto deseado:</label>
        <select id="custom-product">
            <option>Torta personalizada</option>
            <option>Box dulce</option>
            <option>Cookies decoradas</option>
            <option>Postre especial</option>
            <option>Otro</option>
        </select>

        <label>Tamaño:</label>
        <select id="custom-size">
            <option>Pequeño (8 porciones)</option>
            <option>Mediano (12 porciones)</option>
            <option>Grande (20 porciones)</option>
            <option>Gigante (30 porciones)</option>
        </select>

        <label>Sabores:</label>
        <input type="text" id="custom-flavors">

        <label>Relleno:</label>
        <input type="text" id="custom-filling">

        <label>Descripción del diseño:</label>
        <textarea id="custom-details" rows="4"></textarea>

        <label>Fecha del evento:</label>
        <input type="date" id="custom-date">

        <button class="custom-btn" onclick="sendCustomOrder()">Enviar pedido personalizado</button>
    </div>
</section>

<!-- -------------------- PRODUCTOS --------------------- -->
<section class="products" id="product-list">
</section>

<!-- CARRITO FLOTANTE -->
<div class="cart-btn" onclick="openCart()">🛒 Carrito</div>

<!-- MODAL CARRITO -->
<div id="cart-modal">
    <div id="cart-box">
        <h2>Carrito</h2>
        <div id="cart-items"></div>
        <h3>Total: $<span id="cart-total">0</span></h3>
        <button onclick="closeCart()">Cerrar</button>
    </div>
</div>

<!-- WHATSAPP -->
<a class="whatsapp" target="_blank" href="https://wa.me/1123456789">WhatsApp</a>

<footer>
    &copy; 2025 La Panera Verde - Pastelería Sin TACC
</footer>


<!-- -------------------------------- -->
<!--         JAVASCRIPT               -->
<!-- -------------------------------- -->
<script>
// PRODUCTOS
const productos = [
    { nombre: "Brownies", precio: 1200, img:"brownie.png" },
    { nombre: "Alfajor de Maicena", precio: 950, img:"alfajor de maicena.png" },
    { nombre: "Tarta Frutal", precio: 2800, img:"tarta frutal.png" },
    { nombre: "Pancakes", precio: 1500, img:"pancakes.png" },
    { nombre: "Cookies", precio: 700, img:"cookies.png" },
    { nombre: "Tortas", precio: 6500, img:"tortas.png" }
];

// Render productos
productos.forEach((p, i) => {
    document.getElementById("product-list").innerHTML += `
        <div class="product">
            <img src="${p.img}">
            <h3>${p.nombre}</h3>
            <p class="price">$${p.precio}</p>
            <div class="qty-box">
                <label>Cantidad: </label>
                <input id="qty-${i}" type="number" min="1" value="1">
            </div>
            <button class="add-btn" onclick="agregar(${i})">Agregar al carrito</button>
        </div>
    `;
});

// Carrito
let carrito = [];

function agregar(i){
    const cantidad = parseInt(document.getElementById(`qty-${i}`).value);
    const prod = productos[i];

    carrito.push({ nombre: prod.nombre, precio: prod.precio, cantidad });

    alert(`${cantidad} ${prod.nombre} agregado al carrito`);
    actualizarCarrito();
}

function actualizarCarrito(){
    const cont = document.getElementById("cart-items");
    cont.innerHTML = "";

    let total = 0;

    carrito.forEach(item => {
        cont.innerHTML += `<p>${item.cantidad} x ${item.nombre} - $${item.precio * item.cantidad}</p>`;
        total += item.precio * item.cantidad;
    });

    document.getElementById("cart-total").innerText = total;
}

function openCart(){
    document.getElementById("cart-modal").style.display = "flex";
}
function closeCart(){
    document.getElementById("cart-modal").style.display = "none";
}

// PEDIDOS PERSONALIZADOS
function sendCustomOrder() {
    const name = document.getElementById("custom-name").value;
    const product = document.getElementById("custom-product").value;
    const size = document.getElementById("custom-size").value;
    const flavors = document.getElementById("custom-flavors").value;
    const filling = document.getElementById("custom-filling").value;
    const details = document.getElementById("custom-details").value;
    const date = document.getElementById("custom-date").value;

    if (!name || !product || !size || !flavors || !filling || !details || !date) {
        alert("Por favor completá todos los campos.");
        return;
    }

    const message = 
`¡Hola! Me gustaría hacer un pedido personalizado:

👤 Nombre: ${name}
🍰 Producto: ${product}
📏 Tamaño: ${size}
🍫 Sabores: ${flavors}
🥣 Relleno: ${filling}
🎨 Diseño deseado: ${details}
📅 Fecha del evento: ${date}

¿Podrían confirmarme disponibilidad y precio?`;

    window.open(`https://wa.me/1123456789?text=${encodeURIComponent(message)}`, "_blank");
}
</script>

</body>
</html>
