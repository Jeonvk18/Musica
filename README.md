<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Músicos Argentinos</title>

<style>

/* =========================
   FONDO GENERAL
========================= */

body{
margin:0;
font-family:Arial;
background:linear-gradient(180deg,#050816,#0b1220);
color:white;
text-align:center;
}

/* =========================
   HEADER
========================= */

header{
background:linear-gradient(90deg,#2563eb,#3b82f6);
padding:20px;
box-shadow:0 10px 30px rgba(0,0,0,0.4);
}

header h1{
margin:0;
font-size:24px;
}

/* =========================
   BUSCADOR
========================= */

input{
margin:20px;
padding:12px;
width:80%;
max-width:300px;
border-radius:25px;
border:none;
outline:none;
text-align:center;
background:#111827;
color:white;
border:1px solid #2563eb;
}

/* =========================
   CARDS
========================= */

.container{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:20px;
padding:20px;
}

.card{
background:#111827;
border:1px solid #2563eb;
border-radius:15px;
width:200px;
padding:15px;
transition:0.3s;
}

.card:hover{
transform:scale(1.05);
box-shadow:0 10px 25px rgba(37,99,235,0.4);
}

.card img{
width:100%;
height:180px;
object-fit:cover;
border-radius:10px;
}

.card h3{
margin:10px 0 5px;
color:#60a5fa;
}

.card p{
margin:0;
color:#cbd5e1;
font-size:14px;
}

    .card a{
    display:inline-block;
    margin-top:12px;
    padding:8px 14px;
    background:#2563eb;
    color:white;
    text-decoration:none;
    border-radius:999px;
    font-size:14px;
    transition:0.2s;
    }

    .card a:hover{
    background:#1d4ed8;
    }

    </style>

    </head>

    <body>

<header>
<h1>Músicos Argentinos 🎵</h1>
</header>

<input type="text" id="search" placeholder="Buscar artista...">

<div class="container">

<div class="card" data-name="cerati">
<img src="https://akamai.sscdn.co/uploadfile/letras/fotos/4/2/d/2/42d2e803ba0bf47c4061b596700b113b.jpg" alt="Gustavo Cerati">
<h3>Gustavo Cerati</h3>
<p>Rock Nacional</p>
<a href="https://es.wikipedia.org/wiki/Gustavo_Cerati">Más info</a>
</div>

<div class="card" data-name="charly">
<img src="https://indiehoy.com/wp-content/uploads/2025/03/charly-garcia-1.jpg" alt="Charly García">
<h3>Charly García</h3>
<p>Rock Nacional</p>
<a href="https://es.wikipedia.org/wiki/Charly_Garc%C3%ADa">Más info</a>
</div>

<div class="card" data-name="mercedes">
<img src="https://akamai.sscdn.co/uploadfile/letras/fotos/d/b/d/9/dbd905a617d240a26cfab196d3267b0e.jpg" alt="Mercedes Sosa">
<h3>Mercedes Sosa</h3>
<p>Folklore</p>
<a href="https://es.wikipedia.org/wiki/Mercedes_Sosa">Más info</a>
</div>

<div class="card" data-name="fito">
<img src="https://depor.com/resizer/QAVTZDMPATYbEZ2gqWEuhkmDsMQ=/1200x799/smart/filters:format(jpeg):quality(90)/cloudfront-us-east-1.images.arcpublishing.com/elcomercio/J55LW2NGMZHUBMXS3SZJ6EPZCI.jpg" alt="Fito Páez">
<h3>Fito Páez</h3>
<p>Rock Nacional</p>
<a href="https://es.wikipedia.org/wiki/Fito_P%C3%A1ez">Más info</a>
</div>

</div>

<script>

/* =========================
   BUSCADOR
========================= */

const search = document.getElementById("search");
const cards = document.querySelectorAll(".card");

search.addEventListener("input", () => {

const value = search.value.toLowerCase();

cards.forEach(card => {

const name = card.dataset.name;

if(name.includes(value)){
card.style.display = "block";
}else{
card.style.display = "none";
}

});

});

</script>

</body>
</html>
