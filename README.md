# bucket-list

## 분반101 프론트엔드 5주차 팀 과제 버킷리스트

이번 주 **수요일 18:00까지** 파일을 업로드하면 감사하겠습니다 !

시간 이후에 제출해도 상관은 없지만 최종 수정을 고려해 빨리 제출하면 좋아요

---

## **여**기서 P*a8e*를 확인**하세**요

[우리 조 버킷릐ㅣㅣㅣ스트 아트 월](https://parkjongbin0520-spec.github.io/bucket-list/)

---

### 개인 할 일

카드 HTML만 **입맛에 맞게 수정**하면 되는 간단한 과제

1. `card.html` 을 개인 노트북이나 PC에 다운로드하고 **파일명을 바꿔주세요** !
  
2. **버킷리스트** 내용을 채우고 `style` 속성을 추가해보세요 !
  
3. upload file로 `이름_card.html` 형태로 깃허브에 업로드 해주세요 !
  
  (초록색 `<>code` 왼 쪽에 `add file` 메뉴에서 `upload files`에서 올릴 수 있습니다)
  

> **2가지 필수 구현**
> 
> 1. 배지
>   
>   `position: absolute`로 모서리에 스티커(Hot🔥 등) 띄우기 (부모는 relative!)
>   
> 2. 메모
>   
>   카드 맨 아래에 `visibility: hidden`으로 TMI 메모를 숨기고 hover 시 나타나게 하기
>   

4. 작성한 버킷리스트 카드 `이름_card.html` 코드를 마크다운에 Copy&Prass !
  
5. 스크린샷 2장 (카드 띄운거 캡처 + hover 메모 캡처) 도 마크다운 !
  
  개인 컴퓨터에 `Live Server`에서 그냥 띄운거랑 비밀 메모 `:Hover` 로 띄운거
  
6. 마크다운 작성 후 PDF로 내보내기 !
  

---

### 참고하는 CSS 디자인 필수 가이드

- 카드 나란히 배치: `float: left;` 와 `margin`을 이용해 배치합니다.
  
- 부모 높이 붕괴 방지: 팀장 코드의 `<main>` 에 있는 `clearfix` 가 에러를 막아줍니다.
  
- 힙한 포스트잇 느낌: `transform: rotate(-3deg);` 로 살짝 삐뚤게 붙인 효과를 주었습니다.
  

---

### 예시 코드 CSS에 5주차 핵심 이론은 어떤게 들어갔을까?

```
body {
  background-attachment: fixed;
}
```

보드 이미지를 스크롤해도 화면 고정되서 입체적 효과

```
header {
  position: sticky;
  top: 20px;
}
```

`fixed` 처럼 따라온다

```
.card { float: left; }
.clearfix::after { clear: both; }
```

카드를 `float` 로 가로 나열하고 부모 높이가 0이 되는 것을 `clearfix` 로 방어

```
.card:hover {
  transform: scale(1.05) rotate(0deg);
  z-index: 10;
}
```

마우스를 올리면 포스트잇이 확대하고 `z-index` 로 레이어 우선 순위를 높임

---

## 변경 사항

### 04.05. 팀장용 뼈대 코드에 클래스 추가

> `.imgbadge:hover` //뱃지 호버 확대 및 기울기
> 
> transform: scale(1.1) rotate(5deg);
> 
> `.card:active .secret-memo` //카드 클릭 비밀 메모
> 
> visibility: visible !important;
>
> <body> 배경 이미지 변경 및 <header> 어미 영역 추가 및 sticky 속성 추가
