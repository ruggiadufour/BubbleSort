const w = 400, h = 400, n = 20;
function setup() {
  createCanvas(w + 4, h + 4);
  frameRate(20);
}
let numbers = fillArray();
let i = n-1;
let j = 0;

function draw() {
  background(220);
  show(); 
  if (i >= 1) {
    if (j < i) {
      fill(0, 255, 0);
      rect(2 + (w/n) * j, 0, (w/n), numbers[j]);
      fill(0, 255, 0);
      rect(2 + (w/n) * (j+1), 0, (w/n), numbers[j+1]);
      fill(255, 255, 255);
      
      if (numbers[j] > numbers[j + 1]) {
        let aux = numbers[j + 1];
        numbers[j + 1] = numbers[j];
        numbers[j] = aux;
      }
      j++;
    }else{
      j = 0;
      i--;
    }    
  }else{
    noLoop();
  }
   
}

function show(){
  for (let j = 0; j < n; j++) {
    rect(2 + (w/n) * j, 0, (w/n), numbers[j]);
  }
}
function fillArray() {
  let array = [];
  for(let a = 0; a < n; a++){
    array.push(Math.random() * (h - 0) + 0);
  }
  return array;
}
