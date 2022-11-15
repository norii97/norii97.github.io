---
title:  "Art box) 2. GALLERY 개요"
excerpt: "담당 파트) GALLERY 페이지 개요"
categories: 
    - Art box
tag: 
  - [Node.js, Front-end, EJS, JS, JQ, SweetAlert2]
toc: true
toc_sticky : true
author_profile: true
sidebar:
    nav: "docs"
date: 2022-10-18
last_modified_at: 2022-10-19
---

**💡 Link :** [Art box - Gallery](http://118.67.142.110:8000/show_data "Art box - Gallery"){:target="_blank"}  

![gallery](/videos/gallery.gif)

---

### 🛠 사용 기술  

---

||설명|
|:---:|:---:|  
|**Node.js - Express**|라우터 설정|
|**EJS**|작품 출력|
|**Bootstrap**|scroolspy ( 사이드바 )|
|**JavaScript**|요소 이벤트 추가|
|**JQuery**|요소 속성 값 확인 후 이벤트 컨트롤|
|**SweetAlert2**|alert 통해 데이터 출력|
|**Naver Cloud Platform**|클라우드 컴퓨팅 플랫폼|

---

### 🤔 고려 사항

---

1. **작품 배치**
- 작품 크기에 따른 공백 처리
 
2. **EJS 템플릿을 통한 자동화**
- 연대, 시대에 맞춰 작품 자동 출력
- 작품 추가/제거 시 관련 데이터 처리

---

### 💿 데이터

---

#### 🎲 배치 순서

---

- 연대
  - 시대
    - 작품 + 작가&작품명  


<details markdown="1">
 <summary>🌌 IMG</summary>
 
<img src = "/images/sequence.png" alt="sequence" width = "65%">  

</details>

---

<br />

#### 🆘 데이터 구조

---

##### ⏰ 시간순

|고대   |중세    |근세   |근대    |현대        |
|:---: |:---:  |:---:|:---:  |:---:      |
|로마미술|비잔틴미술|르네상스|사실주의 |포스트 모더니즘|
|      |고딕    |매너리즘|인상주의 |추상표현주의  |
|      |       |바로크 |야수파   |팝아트      |
|      |       |로코코 |다다이즘 |           |
|      |       |로코코 |초현실주의|           |

---

##### 🗂 분류

```python
# 연대 - 대분류
연대 리스트 = [ "고대", "중세", "근세", "근대", "현대" ];

# 시대 - 소분류
중세 = 
{
   르네상스: [ "작가&작품명1", "작가&작품명2", "작가&작품명3"],
   매너리즘: [ "작가&작품명4", "작가&작품명5" ],
   ...
};
-----------------------------------

# 작품 설명
작품 딕셔너리 =
{
  "작가&작품명1": "작품 설명", "작가&작품명2": "작품 설명", 
  "작가&작품명3": "작품 설명", ...
};
```

---

<br />

**💡 Link :** [Art box - Gallery](http://118.67.142.110:8000/show_data "Art box - Gallery"){:target="_blank"}  