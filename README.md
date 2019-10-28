# 노마드 코더 카카오 클론 강의 레파지토리 및 내용 정리

## [Module #1] The tools of a Web Developer

개발 환경 vs code + Material Theme + Material Icon + prettier 

깃 = 커밋 + 푸시 + 브랜치 기능
깃허브는 깃을 클라우드 상에서 관리할 수 있는 웹서비스 , 깃 데스크탑도 있음

HTML = hyper text markup language
CSS = cascading style sheet
둘다 프로그래밍 언어가 아님.!

## [Module #2] HTML5

<!DOCTYPE html>은 self-contained 태그다. 혼자 스스로 열고 닫느 태그이다. 이 자체로 정보를 제공하기 떄문!!

semantic tag  VS  Non semantic tag

Non semantic tag  : 아무 의미가 없는 테그, div span태그 등  div는 컨테이너 같은것, span은 텍스트를 위한 컨테이너, 
semantic tag : header,article,section 과 같은 태그들은 의미가 있다.

2-7.
여러가지 div가 있을때 뭐가뭔지 구분을 할때 class와 id를 부여해준다.
class 는 여권의 국적같은 
id는 개인여권 번호같은 것
채팅 메시지는 class, sns 아이콘은 하나의 id

## [Module #3] CSS3

css의 적용 1,외부(external방식)) 2, head부분(inline방식) 3, 각 tag에 직접 지정
css를 배울때 많은 요소들이 박스이다. 4개의 박스가 있다.
content - padding - border - margin 

파일을 html 로 저장을 하고 html:5를 치면 기본적인 html 구조가 나온다.

3-4.
background-color주고 , width랑 height 주고

패딩을 주는 여러가지 방법
padding: 20px;
padding: 20px 10px;
padding: 20px 10px 30px 10px;
padding-top: 50px;

마진도 마찬가지
margin: 50px;

보더도 폭 색상 스타일
border-style:dashed; 
border-color:red;
border-width: 5px;
border: 5px solid red;

3-5. 블록요소 vs 인라인 블록 vs 인라인 요소
블록 요소는 크키에 상관없이 다른 요소가 왼쪽에 있는것을 허용하지 않는다.
인라인 블록은 옆에 다른 요소가 오는것을 허용, display:inline-block;
인라인은 박스의 모든 프로퍼티들을 지울거임. 박스의 폭이나 너비등이 적용이 안됨. 인라인은 텍스트야, 텍스트의 배경색 글자색 등만 적용시킬 수 있을뿐.
## X. 참고 사이트
[분석하고 싶은 웹사이트의 사이즈를 볼때](https://chrome.google.com/webstore/detail/page-ruler/emliamioobfffbgcfdchabfibonehkme?hl=en)
[분석하고 싶은 웹사이트의 색깔을 추출](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp?hl=en)


