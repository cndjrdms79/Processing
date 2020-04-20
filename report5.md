## 과제5 - 각 장별 1개씩 소스코드 예제를 작성 
## 안동대학교 20141264 정혜성
### 1주차 프로세싱으로 Pen 만들기 예제
1. 창 크기 500,500 설정
2. pen 색상 파란색 설정
3. pen 굵기 16 설정
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
* 실행결과

![6주차 pen 실행결과](https://user-images.githubusercontent.com/54826844/79756509-b0ce7280-8355-11ea-8cba-380887d02da2.PNG)


### 2주차 프로세싱으로 배너만들기 예제

1. 창 크기 800,300 설정
2. 글자크기 128 설정
3. 배경색 검은색, 글자색 흰색으로 설정
4. "Graphics" 문자가 왼쪽, 오른쪽으로 반복해서 이동
5. 키보드 입력시 이동속도 증가
```
void setup(){
size(800, 300);
textSize(128);
}
int i, dir=1, sp=1;
void draw(){
background(0);
fill(255);
text("Graphics", i ,200);
if(i>width-128/2*8.5) dir = -1;
if(i<0) dir= 1;
i = i+dir*sp;
if(keyPressed) sp =key-'0';
}
```
* 실행결과

![6주차 배너만들기 실행결과](https://user-images.githubusercontent.com/54826844/79757239-c8f2c180-8356-11ea-8366-9f4cef49372d.PNG)

### 3주차 프로세싱으로 이미지 투명도 예제
1. 창 크기 1200,800 설정
2. 이미지를 불러옴
3. 원본이미지를 고정하고 투명도를 조정한 이미지는 위아래로 움직이도록 설정

```
PImage img;
float offset = 0;
float easing = 1.0;

void setup() {
  size(1200, 800);
  img = loadImage("anu.jpg");  // Load an image into the program 
}

void draw() { 
  image(img, 0, 0);  // Display at full opacity
  float dx = (mouseY-img.height/2) - offset;
  offset += dx * easing; 
  tint(255, 127);  // Display at half opacity
  image(img, 0, offset);
}
```

* 실행결과

![3주차 3-1 Transparency Examples 변경 실행결과](https://user-images.githubusercontent.com/54826844/79758559-816d3500-8358-11ea-8a11-acb6186bbbff.PNG)

### 4주차 프로세싱으로 캐릭터 만들기 예제
1. 창 크기 300,300 설정
2. 위치에 맞게 몸 얼굴 귀 눈동자 입 오른손 왼손 오른발 왼발 설정
3. 토끼 캐릭터 완성
```
size(300,300);
translate(150,100);
rect(-25,0,50,100); //몸
fill(255);
ellipse(0, 0, 100, 60); //얼굴
ellipse(-25, -50, 25, 50); //귀
ellipse(+25, -50, 25, 50); //귀
fill(0);
ellipse(-20, -10, 5, 5); //눈동자
ellipse(+20, -10, 5, 5); //눈동자
fill(255,0,0);
arc(0, 5, 10, 30, 0, PI); //입 
line(25,25,60,60); //오른손
line(-25,25,-60,60); //왼손
line(25,100,50,140); //오른발
line(-25,100,-50,140); //왼발
```
* 실행결과

![4주차 나만의 도형 만들기 MyCharacter](https://user-images.githubusercontent.com/54826844/79758949-035d5e00-8359-11ea-9e48-64ba8e6d646e.PNG)


### 5주차 프로세싱으로 Pshape 변형 예제
1. 창 크기 640,360 설정
2. PShape star 설정
3. 색상은 노란색, 선표시는 없음으로 설정
4. 별모양 도형을 좌표에 맞게 설정
5. 움직이는 마우스에 따라서 도형이동
```
PShape star;
void setup() {
  size(640, 360, P2D);

  // First create the shape
  star = createShape();
  star.beginShape();
  // You can set fill and stroke
  star.fill(255,255,0);
  star.noStroke();
  
  // Here, we are hardcoding a series of vertices
  star.vertex(0, -50);
  star.vertex(14, -20);
  star.vertex(47, -15);
  star.vertex(23, 7);
  star.vertex(29, 40);
  star.vertex(0, 25);
  star.vertex(-29, 40);
  star.vertex(-23, 7);
  star.vertex(-47, -15);
  star.vertex(-14, -20);
  star.endShape(CLOSE);
}
void draw() {
  background(0);
  // We can use translate to move the PShape
  translate(mouseX, mouseY);
  // Display the shape
  shape(star);
}
```

* 실행결과

![5주차 Pshape 실습](https://user-images.githubusercontent.com/54826844/79759638-e5442d80-8359-11ea-85cf-be9892f65d3a.PNG)
