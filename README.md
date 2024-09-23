<!DOCTYPE html>
<html lang="en">
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.3/p5.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.3/addons/p5.sound.min.js"></script>
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />

  </head>
  <body>
    <main>
    </main>
    <script src="sketch.js"></script>
  </body>
</html>

let cor;
let circuloX;
let circuloY;

function setup() {
  createCanvas(400, 400);
  background(color(100, 0, 0));
  cor = "color(random(0, 255), random(0, 255), random(0,255))";
  circuloX = [0, 0, 0, 0, 0];
  circuloY = [random(height), random(height), random(height),random(height),random(height)];
}
function draw() {
  fill(cor);

  // console.log(circuloX length);
  for (let contador in circuloX) {
    console.log(contador);
    circle(circuloX[contador], circuloY[contador], 50);
    circuloX[contador] += random(0, 3);
    circuloY[contador] += random(-3, 3);

    if (circuloX[contador] >= width) {
      circuloX[contador] = 0;
      circuloY[contador] = random(height);
    }
  }

html, body {
  margin: 0;
  padding: 0;
}
canvas {
  display: block;
}
