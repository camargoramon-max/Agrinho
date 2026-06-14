# Agrinho
let windmillAngle = 0;

function setup() {
  createCanvas(900, 600);
}

function draw() {
  background(135, 206, 250);

  // Sun
  fill(255, 204, 0);
  noStroke();
  circle(780, 80, 90);

  // Grass
  fill(90, 180, 80);
  rect(0, 300, width, 300);

  // River
  fill(70, 170, 255);
  rect(0, 450, width, 60);

  // House
  fill(240, 220, 180);
  rect(100, 220, 140, 120);

  fill(170, 60, 40);
  triangle(80, 220, 170, 150, 260, 220);

  fill(120, 70, 30);
  rect(155, 270, 30, 70);

  fill(180, 220, 255);
  rect(115, 245, 25, 25);
  rect(200, 245, 25, 25);

  // Windmill
  push();
  translate(450, 250);

  fill(180);
  rect(-8, 0, 16, 120);

  translate(0, 10);
  rotate(windmillAngle);

  stroke(80);
  strokeWeight(4);
  line(0, 0, 60, 0);
  line(0, 0, -60, 0);
  line(0, 0, 0, 60);
  line(0, 0, 0, -60);

  fill(220);
  circle(0, 0, 15);

  pop();

  windmillAngle += 0.03;

  // Solar Panels
  fill(40, 80, 200);
  rect(650, 260, 90, 40);

  stroke(255);
  line(680,260,680,300);
  line(710,260,710,300);
  line(650,280,740,280);

  // Trees
  drawTree(320,250);
  drawTree(760,240);

  // Flowers
  for(let i=0;i<10;i++){
    fill(255,0,150);
    circle(50+i*70,390,10);
    fill(255,255,0);
    circle(50+i*70,390,4);
  }

  // Title
  noStroke();
  fill(0);
  textAlign(CENTER);
  textSize(28);
  text("STRONG AGRICULTURE", width/2,40);

  textSize(22);
  text("SUSTAINABLE FUTURE", width/2,70);

  textSize(18);
  text("Clean energy and nature make farming stronger.", width/2,560);
}

function drawTree(x,y){
  fill(120,70,30);
  rect(x-8,y,16,50);

  fill(40,160,50);
  circle(x,y-10,50);
  circle(x-18,y+8,40);
  circle(x+18,y+8,40);
}
