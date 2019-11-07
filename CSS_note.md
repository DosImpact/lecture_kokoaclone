# CSS 강의 노트

```cs
display:flex; 부모의 div에 적용한다.
```

```css
justify-content: (수평)
flex-start; 처음부터 나란히 정렬
flex-end; 뒤에서부터 나란히 정렬
center; 아이템들이 중앙으로 이동한다.
space-between;  박스들이 일정하게 벌려짐
space-around; 박스들과 간격이 일정하게 벌려짐
```

```css
align-items: (수직)
flex-start; 위에서 부터 시작한다.
center;
flex-end; 바닥부터 시작한다.
baseline; 요소들을
stretch;
```

```css
flex-direction:
row; 이거는 수평으로 차곡차곡 쌓는다.
column; flex박스들이 수직으로 내려간다.
row-reverse; flex컨테이너의 자식들이 flex컨테이너일 경우, 정렬하는 방식을 거꾸로 한다.
column-reverse;
```

eg)오른쪽에 네비게이션을 주고 싶어 아래로 목차들이 있는.
그럼 direction 은 column 주고, flex-end주고 center주면됨
즉, direction에 따라 수평 수직 옵션이 바뀐다...~!

```css
flex-wrap:
no-wrap; 기본값.
wrap; 원래는 flex컨테이너 안에서 박스들이 쭈구러드는데, 이거는 밑으로 떨어뜨린다.
wrap-reverse;
no-wrap-reverse;

flex-flow: 보통 flex-direction과 flex-wrap은 같이 쓰이기 때문에
column wrap;
row wrap; 등으로 같이 쓴다.
```

- 자식에서도 개별적으로 설정을 디테일 하게 줄수있다.!!

```
order:
0; 기본값
1; flex컨테이너의 각 요소에 직접 이 설정을 해준다. 그러면 order순서가 낮은 요소들 먼저 flex박스에서 배치되게 한다.
-1; 개별 요소에 -1 , -2 등을 주면 개별 순서를 지정 가능!@

align-self: 이역시도 컨테이너의 개별요소들에게 적용시킬수 있다.
flex-end;
center;....
```

## 3-8 css설렉터,가상 선택자

- 가상 설렉터란(pseudo-selector) :  
  태그이름,class,id를 쓰지않고 선택하는 방법이 있다는것!!속성을 선택

```css
input[type="submit"] {
  background-color: red;
}
input[type="password"] {
  background-color: blue;
}
input {
  border: 1px solid yellow;
}
```

- 자식선택,직계선택,형제선택

```css
box들이 여럿있을때 그중에서 선택하는 방법

.box{
background-color:greend; display:block; height:100px; border:1px solid black;
}
.box:last-child{
background-color:pink;
}
.box:first-child{} 첫번째 요소를 선택
.box:nth-child(2){} 두번째 요소를 선택
.box:nth-child(2n){} 짝수의 요소들을 선택

box들이 여럿있을떄 그중에서 다른 요소를 선택하는 방법
input + .box{} 형제 선택자
input > .box{} direct child 직계 자식
```

- 3-9 CSS states

```css
.box{ background-color:red; font-size:40px;}
.box:hover{} 마우스를 올리면~
.box:active{} 마으스로 클릭하면
.box:focuse{} tab을 얹거나 input에 타이핑시
.box:visited{} 클릭했을시
```

## [Module #4] Advanced CSS

- 4-2 트렌지션
  box클래스에 마우스를 올리면 1초에 걸처 색깔이 서서히 바뀐다.

```css
from: 배경만 바뀌게 만든다.
.box {
  background-color: blue;
  color: white;
  transition: background-color 0.9s ease-in-out;
}
from: 모든 속성이 바뀐다.
.box {
  background-color: blue;
  color: white;
  transition: all 0.9s ease-in-out;
}
to: hover
.box:hover {
  background-color: green;
}
```

- 4-3 트렌스포메이션
  html 문서의 요소들의 모습이 바뀌는것, 회전,이동,skew 등등

```css
.box {
  width: 500px;
  height: 500px;
  background: red;
  transform: rotate(20deg);
}
```

트렌지션이랑 트렌스포메이션이랑 합치면 대단한 효과.

```css
.box{ width:100px; height:100px; background: red; transition: transform .5s ease-in-out;}
.box:hover{ transform: rotate(1turn); scale(.5, .5);}
```

- 박스에 마우스를 올렸을때 트렌지션 효과두기
  [example 3-8](/3.CSS3/3-7.html)
- 4-4 애니메이션
  계속해서 트렌지션 및 트렌스폼 효과를 주고 싶다면 애니메이션을 주면 됨.

```css
.box {
  width: 100px;
  height: 100px;
  background: red;
  animation: 1.5s scaleAndRotateSquare ease-in-out;
}
@keyframes scaleAndRotateSquare {
  from {
    transform: none;
  }
  to {
    transform: rotate(1turn) scale(0.5, 0.5);
  }
}
-

계속해서 애니메이션을 반복하고 싶다면: keyframe과 무한히 애니메이션을 바꿔!
.box {
  width: 100px;
  height: 100px;
  background: red;
  animation: 1.5s scaleAndRotateSquare infinite ease-in-out;
}
@keyframes scaleAndRotateSquare {
  0% {
    transform: none;
  }
  50% {
    transform: rotate(1turn) scale(0.5, 0.5);
  }
  100% {
    transform: none;
  }
}
```

- 무한 애니메이션 예제
  [example 3-9](/3.CSS3/3-9.html)
  [example 3-10](/3.CSS3/3-10.html)

- 4-5 Medai Queries

```css
@media screen and (min-width: 320px) and (max-width: 640px) {
  body {
    background-color: blue;
  }
}
```
