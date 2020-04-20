# Report 5
## 안동대학교 20141264 정혜성

```
void setup(){
  size(500,500); //screen size 
  stroke(0,0,255);// pen color
  strokeWeight(16); // pen size
}
void draw(){
  if(mousePressed) // draw mouse
  line(pmouseX,pmouseY,mouseX,mouseY); // mouse move
}
```
