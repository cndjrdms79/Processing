## 과제5 - 각 장별 1개씩 소스코드를 예제를 작성 
## 안동대학교 20141264 정혜성
### 1주차 프로세싱으로 Pen 만들기
1. 가로세로 크기 500,500 화면설정
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


### 2주차 프로세싱으로 배너만들기

1. 창 크기 800,300 지정
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
