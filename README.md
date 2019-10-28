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

3-6. 포지션
모든 박스는 디폴트로 포지션이 static이지. 스크롤을 내리면 안보이게 되는데 position:static; 

만약 포지션이 position:fixed; 라면 스크롤 해도 사라지지가 않는다.
position:fixed; bottom:30px; right:30px; 라면

absolute 는 fixed와 비슷한데 스크롤를 내리면 달라진다.
position:absolute; right:0; top:10px;
이는 본문body에 맞추어 위치를 잡는다. 다른요소와 관계를 만들어주면, 그 요소 기준으로 포지션을 잡는다.
position:relative;

포지션 absolute는 포지션 relative에 상대적으로 포지션을 잡는다. 없으면 body를 기준!

3-7 flex box 퍼킹 어메이징 한것.
flexbox의 필요성 - 인라인 블럭으로만 만들려고 하면, 매우 귀찮은 일임. 박스가 개행할때의 margin값도 좌우가 다르고, 인라인 블럭들의 정렬도 필요할때 하나하나 조정해야됨.
그래서 box들의 부모 div를 flex라고 설정해서 부모의 설정만 건드리면 아래 박스들을 한번에 다룰 수 있다.!

display:flex;

justify-content: (수평)
flex-start;처음부터 나란히 정렬
flex-end;뒤에서부터 나란히 정렬
center; 아이템들이 중앙으로 이동한다. 
space-between; 박스들이 일정하게 벌려짐
space-around; 박스들과 간격이 일정하게 벌려짐

align-items: (수직)
flex-start; 위에서 부터 시작한다.
center;
flex-end; 바닥부터 시작한다.
baseline; 요소들을 
stretch;

flex-direction:
row; 이거는 수평으로 차곡차곡 쌓는다.
column; flex박스들이 수직으로 내려간다.
row-reverse; flex컨테이너의 자식들이 flex컨테이너일 경우, 정렬하는 방식을 거꾸로 한다. 
column-reverse;

eg)오른쪽에 네비게이션을 주고 싶어 아래로 목차들이 있는.
그럼 direction 은 column 주고,  flex-end주고 center주면됨
즉, direction에 따라 수평 수직 옵션이 바뀐다...~!

flex-wrap:
no-wrap; 기본값.
wrap; 원래는 flex컨테이너 안에서 박스들이 쭈구러드는데, 이거는 밑으로 떨어뜨린다.
wrap-reverse;
no-wrap-reverse;

## X. 참고 사이트
[분석하고 싶은 웹사이트의 사이즈를 볼때](https://chrome.google.com/webstore/detail/page-ruler/emliamioobfffbgcfdchabfibonehkme?hl=en)
[분석하고 싶은 웹사이트의 색깔을 추출](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp?hl=en)


