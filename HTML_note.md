#HTML_note

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

```
position : static| fiexd| absolute| relative;
top|bottom|right|left :100px;
```

## 3-7 flex box 퍼킹 어메이징 한것.

flexbox의 필요성 - 인라인 블럭으로만 만들려고 하면, 매우 귀찮은 일임. 박스가 개행할때의 margin값도 좌우가 다르고, 인라인 블럭들의 정렬도 필요할때 하나하나 조정해야됨.
그래서 box들의 부모 div를 flex라고 설정해서 부모의 설정만 건드리면 아래 박스들을 한번에 다룰 수 있다.!
