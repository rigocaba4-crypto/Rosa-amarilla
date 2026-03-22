<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Güerita 🌼💛</title>

<style>
body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  background: linear-gradient(#ffd54f, #fff176);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Arial;
}

/* Carta */
.carta {
  background: #fff8dc;
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  width: 80%;
  max-width: 400px;
  z-index: 2;
}

h1 {
  font-size: 2rem;
}

button {
  margin-top: 15px;
  padding: 10px 20px;
  border: none;
  background: #ffca28;
  border-radius: 10px;
  cursor: pointer;
}

.mensaje {
  display: none;
  margin-top: 15px;
  font-size: 1.2rem;
}

/* Flores cayendo */
.flor {
  position: absolute;
  top: -50px;
  font-size: 24px;
  animation: caer linear infinite;
}

@keyframes caer {
  to {
    transform: translateY(110vh);
  }
}
</style>
</head>

<body>

<audio id="musica" loop>
  <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mpeg">
</audio>

<div class="carta">
  <h1>🌼 Para Güerita 💛</h1>
  <p>Eres como las flores amarillas… iluminas todo 🌼✨</p>

  <button onclick="mostrar()">Abrir mensaje 💌</button>

  <div class="mensaje" id="msg">
    Te quiero mucho ❤️  
    Nunca olvides lo especial que eres 💛
  </div>
</div>

<script>
function mostrar() {
  document.getElementById("msg").style.display = "block";
  document.getElementById("musica").play();
}

/* Crear flores animadas */
for (let i = 0; i < 20; i++) {
  let flor = document.createElement("div");
  flor.className = "flor";
  flor.innerHTML = "🌼";
  flor.style.left = Math.random() * 100 + "vw";
  flor.style.animationDuration = (3 + Math.random() * 5) + "s";
  document.body.appendChild(flor);
}
</script>

</body>
</html>
