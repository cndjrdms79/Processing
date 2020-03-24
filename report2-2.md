# Report2-2
## 안동대학교 컴퓨터공학과 20141264 정혜성

프로세싱으로 "Graphics"라는 배너를 만드시오.
1. 배너가 왼쪽 오른쪽으로 왔다 갔다 한다.
2. 키보드 0~9를 입력하면 속도가 조절이 된다.
3. 배경과 글자색을 본인이 좋아하는 색상으로 하시오.
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

실행결과
![2주차 2-2 과제 배너 위에서아래로 출력](https://user-images.githubusercontent.com/54826844/77389948-e1170580-6dd7-11ea-8ab5-67df7ef0635f.PNG)
