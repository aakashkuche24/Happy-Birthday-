# Happy-Birthday-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Janhavi 💖</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  text-align: center;
  background: linear-gradient(135deg, #ff4b7d, #ff7eb3);
  color: white;
  overflow: hidden;
}

h1 {
  margin-top: 30px;
  font-size: 40px;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 10px white; }
  to { text-shadow: 0 0 25px pink; }
}

.slideshow {
  width: 260px;
  height: 330px;
  margin: auto;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 0 20px pink;
}

.slideshow img {
  width: 100%;
  height: 100%;
  display: none;
}

button {
  padding: 12px 25px;
  border: none;
  border-radius: 20px;
  background: white;
  color: #ff4b7d;
  font-size: 18px;
  margin-top: 20px;
  cursor: pointer;
}

button:hover {
  background: yellow;
}

.heart {
  position: absolute;
  color: pink;
  animation: float 5s linear infinite;
}

@keyframes float {
  from { transform: translateY(100vh); }
  to { transform: translateY(-10vh); }
}
</style>

</head>

<body>

<h1>🎉 Happy Birthday Janhavi 🎉</h1>

<p>Hey Janhavi 😘💖</p>
<p>Aaj cha divas special aahe... pan tu tar rojach special diste 😏</p>
<p>Tu hasta na... tar seriously majha mood full set hoto 😍</p>

<div class="slideshow">
  <img src="photo1.jpg">
  <img src="photo2.jpg">
  <img src="photo3.jpg">
  <img src="photo4.jpg">
</div>

<button onclick="msg()">Click Me 😏</button>

<p id="text"></p>

<script>
let index = 0;
let images = document.querySelectorAll(".slideshow img");

function showSlides() {
  images.forEach(img => img.style.display = "none");
  index++;
  if(index > images.length) index = 1;
  images[index-1].style.display = "block";
  setTimeout(showSlides, 2000);
}
showSlides();

function msg() {
  document.getElementById("text").innerHTML =
  "Sach bolu? Tu bestie kami ani majhi favorite person jast ahes 😌💖";
}

// hearts animation
setInterval(() => {
  let heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = Math.random() * 20 + 20 + "px";
  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 5000);
}, 300);
</script>

</body>
</html>
