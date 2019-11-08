# 노마드 코더 카카오 클론 강의 레파지토리 및 내용 정리

[카카오 클론](https://dosimpact.github.io/kokoaclone/kakaoV2/index.html)  
[ Task 09 ](https://dosimpact.github.io/kokoaclone/Task/Day9Task/index.html)  
[ Task 10 ](https://dosimpact.github.io/kokoaclone/Task/Day10Task/index.html)  
[ Task 11 ](https://dosimpact.github.io/kokoaclone/Task/Day11Task/index.html)  
[ Task 12 ](https://dosimpact.github.io/kokoaclone/Task/Day12Task/index.html)

## [Module #1] The tools of a Web Developer

### 개발 환경 : vs code + (Material Theme + Material Icon + prettier) + git/github

- 깃 = 커밋 + 푸시 + 브랜치 기능
- 깃허브는 깃을 클라우드 상에서 관리할 수 있는 웹서비스 , 깃 데스크탑도 있음

- HTML = hyper text markup language
- CSS = cascading style sheet
- 둘다 프로그래밍 언어가 아님.!

## NOTE

[ HTML 강의 노트 ](HTML_note.md)

---

[ CSS 강의 노트 ](CSS_note.md)

---

[ code snippet 노트 ](Code_snippet.md)

[ BEM 란? ](BEM.md)

## Outro

- study
  공부할 PDF 제공!
- homework
  BEM에 대해서 공부하시요.

# 카카오 클론 코딩 실전편 ~~

---

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

- 예쁜 하얀 동그라미 input 만들기

```
.chat__write {
  position: fixed;
  bottom: 50px;
  margin: 0 auto;
  left: 0;
  right: 0;
  /*position이 fixed 된 녀석을 가운데 정렬 하는방법:
    bottom:50px; margin: 0 auto; left: 0; right: 0;*/
  width: 80%;
  display: flex;
  background-color: #fefefe;
  box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
  /*수평방향 수직방향 블러 그림자색깔*/

  padding: 20px 50px;
  border-radius: 40px;
}

```

```
  아래 위 둘다 그림자 주기.
   box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2),0px -8px 20px rgba(0, 0, 0, 0.2);
```

```
  letter-spacing: 0.1px;
  overflow: hidden;
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

---

[CSS 프레임 워크 스토리 북](https://storybook-design-system.netlify.com/?path=/docs/design-system-intro--page)  
[ 드리블 멋진 웹사이트 디자인을 찾을 수 있는곳. ](https://dribbble.com/)
[ 멋진 패경 패턴 ](https://www.toptal.com/designers/subtlepatterns/)
[ 멋진 UI 그래디언트 ](https://uigradients.com/#MegaTron)
