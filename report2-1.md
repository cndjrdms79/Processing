# Report 2-1
## 안동대학교 20141264 정혜성
* 프로세싱으로 "Graphics"라는 배너를 만드시오.
1. 배너가 왼쪽 오른쪽으로 왔다 갔다 한다.
2. 키보드 0~9를 입력하면 속도가 조절이 된다.
3. 배경과 글자색을 본인이 좋아하는 색상으로 하시오.

```
void setup(){
size(800, 300);
textSize(128);
}
int i, dir=1, sp=1;
void draw(){
fill(0);
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

![2주차 배너만들기 과제 실행결과](https://user-images.githubusercontent.com/54826844/77274733-ea31a500-6cf9-11ea-81b5-2d5ea913a1df.PNG)
