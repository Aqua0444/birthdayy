<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Ultimate Birthday Surprise 🎂💗</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

/* Full-screen gradient background animation */
body {
  margin: 0;
  padding: 0;
  height: 100vh;
  overflow: hidden;
  font-family: "Poppins", sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #ffb3d9, #ffe6f2, #ffe6cc);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
}

@keyframes gradientBG {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* Card */
.card {
  background: rgba(255, 255, 255, 0.95);
  padding: 40px;
  border-radius: 20px;
  width: 80%;
  max-width: 450px;
  text-align: center;
  box-shadow: 0 8px 35px rgba(0,0,0,0.2);
  position: relative;
  z-index: 5;
}

/* Birthday message words */
.message span {
  display: inline-block;
  font-size: 28px;
  font-weight: 600;
  margin: 0 2px;
  background: linear-gradient(90deg, #ff80bf, #ff4da6, #ffc0cb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: pulseWords 2s ease-in-out infinite, sparkleWords 3s linear infinite;
}

@keyframes pulseWords {
  0%,100% { transform: scale(1); }
  50% { transform: scale(1.3); }
}

@keyframes sparkleWords {
  0%,100% { text-shadow: 0 0 5px #ff80bf, 0 0 10px #ffc0cb; }
  50% { text-shadow: 0 0 15px #ff4da6, 0 0 25px #ff80bf; }
}

/* Shou sparkling text */
#shou {
  font-size: 36px;
  font-weight: bold;
  margin: 15px 0;
  background: linear-gradient(90deg, #ff80bf, #ff4da6, #ffc0cb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: sparkle 2s infinite linear, glow 2s infinite alternate;
}

@keyframes sparkle {
  0% { filter: brightness(1); }
  25% { filter: brightness(1.5); }
  50% { filter: brightness(1); }
  75% { filter: brightness(1.3); }
  100% { filter: brightness(1); }
}

@keyframes glow {
  0% { text-shadow: 0 0 5px #ff80bf; }
  50% { text-shadow: 0 0 20px #ff4da6, 0 0 30px #ffc0cb; }
  100% { text-shadow: 0 0 5px #ff80bf; }
}

/* Button */
button {
  padding: 12px 25px;
  background: #ff80bf;
  border: none;
  border-radius: 12px;
  color: white;
  font-size: 18px;
  cursor: pointer;
  margin-top: 10px;
  transition: transform 0.2s, background 0.3s;
}
button:hover {
  background: #ff4da6;
  transform: scale(1.05);
}

/* Floating hearts */
.heart {
  position: fixed;
  bottom: -10px;
  animation: floatUp linear forwards;
  color: #ff4da6;
  opacity: 0;
  z-index: 3;
}

@keyframes floatUp {
  0% { transform: translateY(0) rotate(0deg); opacity: 0; }
  10% { opacity: 0.7; }
  100% { transform: translateY(-120vh) rotate(360deg); opacity: 0; }
}

/* Floating sparkles around */
.sparkle {
  position: fixed;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  opacity: 0.8;
  animation: sparkleFloat linear forwards;
  z-index: 3;
}

@keyframes sparkleFloat {
  0% { transform: translate(0,0) scale(0.5); opacity: 1; }
  100% { transform: translate(0,-100vh) scale(1); opacity: 0; }
}

/* Confetti */
.confetti {
  position: fixed;
  width: 10px;
  height: 10px;
  opacity: 0.9;
  z-index: 4;
  pointer-events: none;
  animation: confettiFall linear forwards;
}

@keyframes confettiFall {
  0% { transform: translateY(0) rotate(0deg); opacity: 1; }
  100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
}

/* Twinkling stars */
.star {
  position: fixed;
  background: white;
  border-radius: 50%;
  opacity: 0.8;
  animation: twinkle 2s infinite alternate;
  z-index: 0;
}

/* ILY corner styles */
.ily-corner {
  position: fixed;
  font-size: 48px;
  font-weight: bold;
  color: #ff4da6;
  z-index: 4;
  user-select: none;
}
.ily-tl { top: 20px; left: 20px; animation: floatTL 4s ease-in-out infinite alternate, pulseTL 2s infinite; }
.ily-tr { top: 20px; right: 20px; animation: floatTR 3s ease-in-out infinite alternate, pulseTR 2s infinite; }
.ily-bl { bottom: 20px; left: 20px; animation: floatBL 5s ease-in-out infinite alternate, pulseBL 2s infinite; }
.ily-br { bottom: 20px; right: 20px; animation: floatBR 4s ease-in-out infinite alternate, pulseBR 2s infinite; }

/* Float animations */
@keyframes floatTL { 0% { transform: translate(0,0); } 100% { transform: translate(15px,15px); } }
@keyframes floatTR { 0% { transform: translate(0,0); } 100% { transform: translate(-15px,15px); } }
@keyframes floatBL { 0% { transform: translate(0,0); } 100% { transform: translate(15px,-15px); } }
@keyframes floatBR { 0% { transform: translate(0,0); } 100% { transform: translate(-15px,-15px); } }

/* Pulse animations */
@keyframes pulseTL { 0%,100% { transform: scale(1);} 50% { transform: scale(1.2);} }
@keyframes pulseTR { 0%,100% { transform: scale(1);} 50% { transform: scale(1.3);} }
@keyframes pulseBL { 0%,100% { transform: scale(1);} 50% { transform: scale(1.25);} }
@keyframes pulseBR { 0%,100% { transform: scale(1);} 50% { transform: scale(1.2);} }
</style>
</head>
<body>

<div class="card">
  <div id="msg" class="message">Happy Birthday! 🎉</div>
  <div id="shou">Shou ✨</div>
  <button id="nextBtn">Next 🎈</button>
</div>

<!-- ILY in all corners -->
<div class="ily-corner ily-tl">ILY ❤️</div>
<div class="ily-corner ily-tr">ILY 💖</div>
<div class="ily-corner ily-bl">ILY 💗</div>
<div class="ily-corner ily-br">ILY 💝</div>

<script>
// Split words into spans for animation
function animateMessage(text) {
  const container = document.getElementById("msg");
  container.innerHTML = "";
  text.split(" ").forEach(word => {
    const span = document.createElement("span");
    span.textContent = word;
    container.appendChild(span);
    container.appendChild(document.createTextNode(" "));
  });
}

// Messages
const msgs = [
  "Happy Birthday! 🎉",
  "Wishing you a day filled with love and laughter ❤️",
  "May all your wishes come true 🌟",
  "Here’s to good times and great memories 🥳",
  "Enjoy your special day! 🎂"
];
let idx = 0;
animateMessage(msgs[idx]);

// Button click effect + confetti
document.getElementById("nextBtn").onclick = () => {
  idx = (idx + 1) % msgs.length;
  animateMessage(msgs[idx]);

  // Confetti burst
  for (let i = 0; i < 50; i++) {
    const confetti = document.createElement("div");
    confetti.className = "confetti";
    confetti.style.left = Math.random() * 100 + "vw";
    confetti.style.backgroundColor = `hsl(${Math.random()*360}, 80%, 60%)`;
    confetti.style.width = confetti.style.height = (5 + Math.random() * 10) + "px";
    confetti.style.animationDuration = (2 + Math.random()*2) + "s";
    document.body.appendChild(confetti);
    setTimeout(() => confetti.remove(), 4000);
  }
};

// Floating hearts continuously
setInterval(() => {
  const heart = document.createElement("div");
  heart.textContent = "💗";
  heart.className = "heart";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (20 + Math.random() * 30) + "px";
  heart.style.animationDuration = (3 + Math.random() * 4) + "s";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 7000);
}, 200);

// Twinkling stars
for(let i=0; i<200; i++){
  const star = document.createElement("div");
  star.className = "star";
  star.style.width = star.style.height = (1 + Math.random()*3) + "px";
  star.style.top = Math.random() * 100 + "vh";
  star.style.left = Math.random() * 100 + "vw";
  star.style.animationDuration = (1 + Math.random()*3) + "s";
  document.body.appendChild(star);
}

// Floating sparkles randomly
setInterval(() => {
  const sparkle = document.createElement("div");
  sparkle.className = "sparkle";
  sparkle.style.left = Math.random() * window.innerWidth + "px";
  sparkle.style.top = Math.random() * window.innerHeight + "px";
  sparkle.style.width = sparkle.style.height = (3 + Math.random()*6) + "px";
  sparkle.style.backgroundColor = `hsl(${Math.random()*360}, 80%, 70%)`;
  sparkle.style.animationDuration = (2 + Math.random()*3) + "s";
  document.body.appendChild(sparkle);
  setTimeout(() => sparkle.remove(), 3000);
}, 150);

// Floating bubbles
setInterval(() => {
  const bubble = document.createElement("div");
  bubble.style.position = "fixed";
  bubble.style.width = bubble.style.height = (5 + Math.random()*20) + "px";
  bubble.style.borderRadius = "50%";
  bubble.style.background = `hsla(${Math.random()*360}, 70%, 80%, 0.4)`;
  bubble.style.left = Math.random() * window.innerWidth + "px";
  bubble.style.bottom = "-20px";
  bubble.style.zIndex = 2;
  const duration = 4 + Math.random()*4;
  bubble.style.transition = `transform ${duration}s linear, opacity ${duration}s linear`;
  document.body.appendChild(bubble);
  setTimeout(() => { bubble.style.transform = `translateY(-${window.innerHeight + 50}px)`; bubble.style.opacity=0; }, 50);
  setTimeout(() => bubble.remove(), duration*1000);
}, 300);
</script>

</body>
</html>
