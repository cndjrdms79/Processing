# Report2-2
## 안동대학교 컴퓨터공학과 20141264 정혜성

* 한글 배너를 제작하시오.
1. "안동대 컴공 사랑합니다"
2. 위에서 아래로 내려오도록 배너를 만드시오.
3. 키보드로 속도를 0~9배까지 조절하도록 하시오.
```
PFont f;
void setup(){
size(800,800);
textSize(72);
f = createFont("굴림",64);
textFont(f);
}
int i ,a=1;
void draw(){
  fill(0);
background(255);
if(keyPressed)
a= key-'0';
text("안동대컴공 사랑합니다",70, i=i+a);
if(i>800) i=0;
}
```

* 실행결과

![2주차 2-2 과제 배너 위에서아래로 출력](https://user-images.githubusercontent.com/54826844/77389948-e1170580-6dd7-11ea-8ab5-67df7ef0635f.PNG)
