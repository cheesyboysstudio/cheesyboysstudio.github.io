# cheesyboysstudio.github.io
onze coole game
 </div>
    </section>

    <section>
      <h2>👾 De vijanden</h2>
      <div class="worlds">
        <article><h3>🐱 Catianen</h3><p>Blauwe helpers van de Ender Cat.</p></article>
        <article><h3>💜 Ender Cat</h3><p>De eindbaas met lila manen. Verschijnt in wave 5!</p></article>
      </div>
    </section>

    <section id="about">
      <h2>🐶 Onze mascotte</h2>
      <p>Maak kennis met Pasta, de hond van Cheesy Boys Studios!</p>
      <h2>Gemaakt door Cheesy Boys Studios</h2>
    </section>
  </main>

  <footer>© 2026 Cheesy Boys Studios - NOVABLOX</footer>
  <script src="script.js"></script>
</body>
</html>
{
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  background: #101025;
  color: white;
  font-family: Arial, sans-serif;
}

header {
  background: #211443;
  padding: 18px;
  text-align: center;
  border-bottom: 3px solid #a855f7;
}

header h1 {
  color: #e5b8ff;
}

nav {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  color: #d8a5ff;
}

section {
  padding: 45px 20px;
  text-align: center;
}

.hero {
  min-height: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: linear-gradient(135deg, #32145b, #101025);
}

.hero h2 {
  font-size: clamp(40px, 8vw, 75px);
  color: #d9a5ff;
  margin-bottom: 5px;
}

.play-button {
  display: inline-block;
  align-self: center;
  background: #a855f7;
  color: white;
  padding: 15px 35px;
  border-radius: 12px;
  text-decoration: none;
  font-weight: bold;
  margin-top: 20px;
}

iframe {
  width: 100%;
  max-width: 1000px;
  height: 650px;
  border: 3px solid #a855f7;
  border-radius: 15px;
  background: black;
}

.worlds {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.worlds article {
  background: #211443;
  border: 2px solid #7136a8;
  border-radius: 15px;
  padding: 20px;
  width: 260px;
}

footer {
  background: #211443;
  text-align: center;
  padding: 25px;
}

@media (max-width: 600px) {
  iframe {
    height: 600px;
  }

  nav {
    gap: 12px;
  }
}
document.querySelectorAll('nav a').forEach(link => {
  link.addEventListener('click', () => {
    document.querySelectorAll('nav a').forEach(item => {
      item.style.color = 'white';
    });

    link.style.color = '#d8a5ff';
  });
});
<!DOCTYPE html>
<html lang="nl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NOVABLOX Game</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>🌌 NOVABLOX</h1>
  <p>Bestuur Pasta en versla de Catianen!</p>

  <div class="controls">
    <button id="start">Start</button>
    <button id="restart">Opnieuw</button>
    <button id="fullscreen">Volledig scherm</button>
  </div>

  <p id="status">Druk op Start om te beginnen.</p>
  <canvas id="game" width="800" height="450"></canvas>

  <div class="touch-controls">
    <button data-key="ArrowUp">⬆️</button>
    <div>
      <button data-key="ArrowLeft">⬅️</button>
      <button data-key="ArrowDown">⬇️</button>
      <button data-key="ArrowRight">➡️</button>
    </div>
  </div>

  <script src="game.js"></script>
</body>
</html>
{
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 15px;
  text-align: center;
  background: #101025;
  color: white;
  font-family: Arial, sans-serif;
}

canvas {
  display: block;
  width: 100%;
  max-width: 800px;
  height: auto;
  margin: 15px auto;
  border: 3px solid #a855f7;
  border-radius: 10px;
  background: #182c36;
}

button {
  background: #813bd0;
  color: white;
  border: 0;
  border-radius: 8px;
  padding: 12px 18px;
  margin: 5px;
  font-weight: bold;
  cursor: pointer;
  touch-action: none;
}

button:hover {
  background: #a855f7;
}

.touch-controls {
  margin-top: 15px;
}

.touch-controls button {
  min-width: 55px;
  font-size: 20px;
}

#status {
  color: #e5b8ff;
  font-weight: bold;
}

@media (min-width: 900px) {
  .touch-controls {
    display: none;
  }
}
document.getElementById("restart").onclick = reset;

document.getElementById("fullscreen").onclick = () => {
  if (canvas.requestFullscreen) canvas.requestFullscreen();
};

document.querySelectorAll("[data-key]").forEach(button => {
  const key = button.dataset.key;

  button.addEventListener("pointerdown", e => {
    e.preventDefault();
    keys[key] = true;
  });

  ["pointerup", "pointerleave", "pointercancel"].forEach(event => {
    button.addEventListener(event, () => keys[key] = false);
  });
});

reset();
loop();




Zo moet jullie GitHub-project eruitzien

NOVABLOX/
│
├── index.html
├── style.css
├── script.js
│
└── game/
    ├── index.html
    ├── style.css
    └── game.js
