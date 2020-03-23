# Report 2-1
## 안동대학교 20141264 정혜성
프로세싱으로 "Graphics"라는 배너를 만드시오.
1. 배너가 왼쪽 오른쪽으로 왔다 갔다 한다.
2. 키보드 0~9를 입력하면 속도가 조절이 된다.
3. 배경과 글자색을 본인이 좋아하는 색상으로 하시오.

```
void setup(){
size(800,300);
textSize(128);
}
int i ,a=1;
void draw(){
background(0);
if(keyPressed)
a= key-'0';
text("Graphics",i=i+a, 200);
if(i>800) i=0;
}
```

* 실행결과
![2주차 배너만들기 과제 실행결과](https://user-images.githubusercontent.com/54826844/77274733-ea31a500-6cf9-11ea-81b5-2d5ea913a1df.PNG)
