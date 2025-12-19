# l
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sana Yazılmış Bir Aşk</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;1,600&family=Montserrat:wght@300;600&display=swap" rel="stylesheet">

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  background: radial-gradient(circle at top, #3a0b5e, #120018);
  color: #fff;
  font-family: 'Montserrat', sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.container {
  max-width: 420px;
  padding: 32px;
  text-align: center;
  background: rgba(255,255,255,0.08);
  border-radius: 25px;
  backdrop-filter: blur(12px);
  box-shadow: 0 0 40px rgba(255,0,150,0.25);
  animation: fadeIn 2s ease;
}

h1 {
  font-family: 'Playfair Display', serif;
  font-size: 30px;
  margin-bottom: 25px;
}

.poem {
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 18px;
  line-height: 1.8;
  margin-bottom: 28px;
}

button {
  background: linear-gradient(135deg, #ff4fd8, #b400ff);
  border: none;
  padding: 14px 30px;
  border-radius: 30px;
  color: #fff;
  font-size: 16px;
  cursor: pointer;
  transition: transform .3s, box-shadow .3s;
  box-shadow: 0 10px 25px rgba(255,0,200,.4);
}

button:hover {
  transform: scale(1.08);
  box-shadow: 0 15px 30px rgba(255,0,200,.6);
}

.hidden {
  display: none;
}

@keyframes fadeIn {
  from {opacity: 0; transform: scale(0.95);}
  to {opacity: 1; transform: scale(1);}
}

/* Kalpler */
.heart {
  position: absolute;
  color: #ff5fd2;
  font-size: 20px;
  animation: float 6s linear infinite;
  opacity: 0.7;
}

@keyframes float {
  from {transform: translateY(100vh) scale(1); opacity: 1;}
  to {transform: translateY(-10vh) scale(1.5); opacity: 0;}
}
</style>
</head>

<body>

<div class="container">
  <h1>Sana Yazılmış Bir Aşk</h1>

  <div class="poem">
    Göğsüne yaslanınca susar dünya,<br>
    Kalbim adını ezbere biliyor.<br>
    Zaman durur sen gülünce,<br>
    Ben her halinle seni seviyorum.
  </div>

  <button onclick="showMessage()">Kalbimden Sana</button>

  <div class="poem hidden" id="secret">
    Eğer bir gün kaybolursan,<br>
    Bil ki seni bekleyen bir kalp var.<br><br>
    Ne zaman yorulursan,<br>
    O kalp hep aynı yerde olacak.<br><br>
    <b>Ben.</b>
  </div>
</div>

<script>
function showMessage() {
  document.getElementById("secret").classList.remove("hidden");
}

// Kalp animasyonu
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerText = "❤";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = Math.random() * 15 + 15 + "px";
  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 6000);
}, 300);
</script>

</body>
</html>
