---
title:  "Art box) 3. GALLERY 구현"
excerpt: "담당 파트) GALLERY 페이지 구현"
categories: 
    - Art box
tag: 
    - [Node.js, Front-end, EJS, JS, JQ, SweetAlert2 ]
toc: true
toc_sticky : true
author_profile: true
sidebar:
    nav: "docs"
date: 2022-10-19
last_modified_at: 2022-10-21
---

**💡 Link :** [Art box - Gallery](http://118.67.142.110:8000/show_data "Art box - Gallery"){:target="_blank"}  

### 🛟 페이지 구조

- 작품 출력  
    - 3열 종대
        - 작품
        - 작가명 & 작품명

- 사이드 바  
    - 연대  
    - 시대  

![print3](/videos/frame.gif)

---

### ⚽️ 구현

---
#### ✔️ 작품 출력


---

##### - 3열 종대

&nbsp; 모든 작품이 출력 될 때 까지 한 행에 3개씩 작품을 출력했습니다.

- 작품 - 중앙 정렬  
- 작가&작품명 - 하단 고정   

<br>

![print3](/videos/div3.gif)

---

#### ✔️ onclick 이벤트

---

##### - SweetAlert2 를 통해 작품 확대 및 설명 출력

&nbsp; onclick 이벤트를 통해 함수 호출 후  
SweetAlert2 를 사용하여 작품 확대 및 설명 출력하였습니다.

---

##### - 네브바 fadein/fadeout  

&nbsp; SweetAlert2 실행 시 swal2-container 라는 클래스가 추가되는 것을 확인하였습니다.  

&nbsp; JQuery hasclass 함수를 통해 swal2-container 클래스 유/무를 확인 후 네브바를 fadeout/fadein 해 주었습니다.

&nbsp; SweetAlert2 가 꺼진 후 이벤트리스너가 onclick 에만 걸려있어 클릭을 하지 않을 경우 네브바가 복구되지 않는 예외 상황이 발생하였습니다.

&nbsp; 이벤트리스너에 onscroll 을 추가하여 예외 상황에 대처 해 주었습니다.

<br/>

![print3](/videos/sweetalert2.gif)

---

####  ✔️ 사이드 바 ( Bootstrap - scrollspy )

---

##### - 작품과 연대/시대 매칭
##### - 연대/시대 클릭 시 해당 작품으로 이동

<br/>

&nbsp; 위 두 개는 Bootstrap 프레임워크의 scrollspy 를 사용하였습니다.

<br/>

![print3](/videos/scrollspy1.gif)

---

##### - 해당 시대에 맞게 스크롤 바 상하 이동

&nbsp; 화면 스크롤 시 현재 작품의 시대에 맞춰 사이드 바의 시대는 변하지만, 사이드 바의 스크롤이 이에 맞춰 따라가는 기능은 지원되지 않음을 파악하였습니다.

&nbsp; 이를 해결하기 위해 스크롤 시 **현재 화면의 높이/전체화면의 높이** 퍼센테이지를 구하여 사이드바의 스크롤 위치를 퍼센테이지에 맞춰 주면 해결이 될 거라 생각했습니다.

&nbsp; 하지만 scroll 이벤트 중복 발생과 동기처리 때문에 인지 버벅거리면 오작동을 일으켰습니다.

&nbsp; 이를 해결하기 위해 사이드바 내부의 컨텐츠 양이 많지 않으니 **현재 화면의 높이/전체화면의 높이** 50% 를 기점으로 사이드바의 스크롤을 최하단 최상단으로 옮겨주는 것으로 해결 하였습니다.

<br/>

![print3](/videos/scrollspy2.gif)

---

**💡 Link :** [Art box - Gallery](http://118.67.142.110:8000/show_data "Art box - Gallery"){:target="_blank"}  