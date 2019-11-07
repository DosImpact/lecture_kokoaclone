# BEM 이란??

## HTML class에 대한 명명 규칙이다.

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

---
