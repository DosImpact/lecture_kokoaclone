# 노마드 코더 카카오 클론 강의 레파지토리 및 내용 정리

[카카오 클론](kakaoV2/index.html)

## [Module #1] The tools of a Web Developer

### 개발 환경 : vs code + (Material Theme + Material Icon + prettier) + git/github

- 깃 = 커밋 + 푸시 + 브랜치 기능
- 깃허브는 깃을 클라우드 상에서 관리할 수 있는 웹서비스 , 깃 데스크탑도 있음

- HTML = hyper text markup language
- CSS = cascading style sheet
- 둘다 프로그래밍 언어가 아님.!

## [Module #2] HTML5

```html
<!DOCTYPE html>
```

self-contained Tag: 혼자 스스로 열고 닫는 태그이다. 이 자체로 정보를 제공하기 떄문!!

### semantic tag VS Non semantic tag

1. Non semantic tag : 아무 의미가 없는 테그, div span태그 등, div는 컨테이너 같은것, span은 텍스트를 위한 컨테이너,
2. semantic tag : header,article,section 과 같은 태그들은 의미가 있다.

## [Module #3] CSS3

### - css의 적용 1,외부(external방식)) 2, head부분(inline방식) 3, 각 tag에 직접 지정 방식

```css
<link href="styles.css" rel="stylesheet">
```

### - Box model

content -> padding -> border -> margin

cf)파일을 html 로 저장을 하고 html:5를 치면 기본적인 html 구조가 나온다.

### 3-4.

- 패딩을 주는 여러가지 방법

```css
padding: 20px;
padding: 20px 10px;
padding: 20px 10px 30px 10px;
padding-top: 50px;
```

- 마진도 마찬가지

```
margin: 50px;
```

- 보더도 폭 색상 스타일

```css
border-style: dashed;
border-color: red;
border-width: 5px;
border: 5px solid red;
```

## 3-5. 블록요소 vs 인라인 블록 vs 인라인 요소

블록 요소는 크키에 상관없이 다른 요소가 오른쪽에 있는것을 허용하지 않는다.  
인라인 블록은 옆에 다른 요소가 오는것을 허용, display:inline-block; 그리고 박스 모델이 적용이 된다.  
인라인은 박스의 모든 프로퍼티들을 지울거임. 박스의 폭이나 너비등이 적용이 안됨. 인라인은 텍스트야, 텍스트의 배경색 글자색 등만 적용시킬 수 있을뿐.

## 3-6. 포지션

모든 박스는 디폴트로 포지션이 static이지. 스크롤을 내리면 안보이게 되는데 position:static;

만약 포지션이 position:fixed; 라면 스크롤 해도 사라지지가 않는다.  
position:fixed; bottom:30px; right:30px; 라면

absolute 는 fixed와 비슷한데 스크롤를 내리면 달라진다.  
position:absolute; right:0; top:10px;
이는 본문body에 맞추어 위치를 잡는다. 다른요소와 관계를 만들어주면, 그 요소 기준으로 포지션을 잡는다.
position:relative;

포지션 absolute는 포지션 relative에 상대적으로 포지션을 잡는다. 없으면 body를 기준!

## 3-7 flex box 퍼킹 어메이징 한것.

flexbox의 필요성 - 인라인 블럭으로만 만들려고 하면, 매우 귀찮은 일임. 박스가 개행할때의 margin값도 좌우가 다르고, 인라인 블럭들의 정렬도 필요할때 하나하나 조정해야됨.
그래서 box들의 부모 div를 flex라고 설정해서 부모의 설정만 건드리면 아래 박스들을 한번에 다룰 수 있다.!

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
.box {
  background-color: blue;
  color: white;
  transition: background-color 0.9s ease-in-out;
}
배경만 바뀌게 만든다. .box {
  background-color: blue;
  color: white;
  transition: all 0.9s ease-in-out;
}
모든 속성이 바뀐다. .box:hover {
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

## Outro

- study
  공부할 PDF 제공!
- homework
  BEM에 대해서 공부하시요.

Block
Standalone entity that is meaningful on its own.

Examples
header, container, menu, checkbox, input

---

Element
A part of a block that has no standalone meaning and is semantically tied to its block.

Examples
menu item, list item, checkbox caption, header title

---

Modifier
A flag on a block or element. Use them to change appearance or behavior.

Examples
disabled, highlighted, checked, fixed, size big, color yellow

```css
.button {
  display: inline-block;
  border-radius: 3px;
  padding: 7px 12px;
  border: 1px solid #d5d5d5;
  background-image: linear-gradient(#eee, #ddd);
  font: 700 13px/18px Helvetica, arial;
}
.button--state-success {
  color: #fff;
  background: #569e3d linear-gradient(#79d858, #569e3d) repeat-x;
  border-color: #4a993e;
}
.button--state-danger {
  color: #900;
}
```

---

### 또다른 방법론

BEM: 코드를 쉽게 읽기위한 방법론이다. header\_\_form-email. 와 같은 코들르 본다면 BDEM 방법론이 적용된것.
BEM : block element modifier

페이지를 크게 header, siderbar,footer article 등올 나누면 이게 네이밍의 어근이 된다.
여기다가 각 기능을 접두사로 추가하면됨.

1. 규칙 element는 **로 이어쓴다.
   .block**element
   eg)
   .header**logo{}
   .header**tagline{}
   .header**navigation{}
   .header**serachbar{}

2. 규칙 Modifier는 --로 이어쓴다.
   .block\_\_elemnet--sizebig\

# 카카오 클론 코딩 실전편 ~~

## reset CSS

- 기본적으로 큰 파일임. 모든 기본값 margin,padding을 0으로 만들어줌, p태그,h1태그 등등 모든 패딩 마진 다 다름.
  [css 초기화 파일](https://meyerweb.com/eric/tools/css/reset/)

```css
styles.css에서 다음을 임포트 해서 쓰면 된다.
@import "reset.css";
```

- Noramlize css 는 모든 브라우저의 각 태그들의 마진 패딩 등의 값을 동일하게 만들어 준다.
- Google fonts 를 통해서, 원하는 폰트를 고르고, 가볍게 커스터 마이징(원하는 옵션만 골라),해서 import하면 끝!

```css
@import url("https://fonts.googleapis.com/css?family=Open+Sans:400,700&display=swap");
@import "reset.css";
@import "status-bar.css";
body {
  background-color: white;
  padding: 10px 20px;
  color: #020202;
  font-family: "Open Sans", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
```

- 왜이렇게 class를 덕지덕지 붙이나 싶었는데, class를 덕지 덕지 붙였다는 말은 스타일을 일괄적용하고
  js로 일괄적으로 컨트롤 하겠다는 느낌인것 같다. class나 id가 없는 태그는 음... 비행청소년같은 느낌? 어디로 갔는지 모르겠고
  설상 문서상에 딱 나타나도 어떻게 js나 css로 잡아줄수가 없네....~!!!!

- css파일을 자꾸 쪼개는 이유

1. 작은 쪼갠 css파일들은 결국 styles.css로 통합된다.
2. 그렇게 작게 쪼개두면 navbar을 수정할때는 nav.css만 수정하면됨, 구지 길게 파일을 써 내려갈 필요가 없음

- statusbar,header,navbar작업전에는 항상 빨간색을 칠해보고 하드라

- box-sizing: border-box의 이해

```css
* {
  /*이 설정을 안해주면, 박스의 크기는 = 마진+보더+패딩+컨텐츠 쭉쭉 생각했던것보다 커짐*/
  /*이 설정은 border까지의 크기를  height,width로 예상했던것만큼 만들어줌*/
  box-sizing: border-box;
}
```

## X. 참고 사이트

## [분석하고 싶은 웹사이트의 사이즈를 볼때](https://chrome.google.com/webstore/detail/page-ruler/emliamioobfffbgcfdchabfibonehkme?hl=en)

## [분석하고 싶은 웹사이트의 색깔을 추출](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp?hl=en)

[트렌지션 docs](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)
[트렌스포메이션 docs](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)

---

[BEM 소개](http://getbem.com/introduction/)
[BEM 키 컨셉](https://en.bem.info/methodology/key-concepts/)
[BEM 퀵스타트](https://en.bem.info/methodology/quick-start/)
