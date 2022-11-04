---
title:  "Art box - 2. GALLERY 개요"
excerpt: "담당 파트 GALLERY 페이지 개요"
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

### 🪧 계획
---

#### 🛠 기술 스택  

||설명|
|:---:|:---:|  
|**EJS**|연대/시대에 맟춰 작품 출력 자동화|
|**Bootstrap**|scroolspy ( 사이드바 )|
|**JavaScript**|요소 이벤트 추가|
|**JQuery**|요소 속성 값 확인 후 이벤트 컨트롤|
|**SweetAlert2**|클릭 시 alert를 통해 데이터 출력|


---

#### 🤔 고려 사항

1. **작품 배치**
- 작품 크기 별 공백 처리
 
2. **EJS 템플릿을 통한 자동화**
- 연대, 시대에 맞춰 작품 자동 출력
- 작품 추가/제거 시 관련 데이터 처리

---

### 💿 데이터
---

#### 🎲 순서

> 연대
>> 시대
>>> 작품 + 작품명  

<br />

<img src = "/images/sequence.png" alt="sequence">  

<br />

### 🆘 데이터 구조

<details markdown="1">
 <summary>상세 설명</summary>

#### ⏰ 시간순

|고대   |중세    |근세   |근대    |현대        |
|:---: |:---:  |:---:|:---:  |:---:      |
|로마미술|비잔틴미술|르네상스|사실주의 |포스트 모더니즘|
|      |고딕    |매너리즘|인상주의 |추상표현주의  |
|      |       |바로크 |야수파   |팝아트      |
|      |       |로코코 |다다이즘 |           |
|      |       |로코코 |초현실주의|           |

---

#### 🗂 분류

```python
# 연대 - 대분류
연대 리스트 = [ 고대, 중세, 근세, 근대, 현대 ]

# 시대 - 소분류
중세 = 
{
   르네상스: [ 작품명1, 작품명2, 작품명3],
   매너리즘: [ 작품명4, 작품명5 ],
   ...
}

# 작품설명
작품 딕셔너리 =
{
  작품명1: 설명, 작품명2: 설명, 작품명3: 설명, ...
}

```

---

#### ⚙️ 설계

> **연대 리스트**  [ 고대, 중세, 근세, 근대, 현대 ]  
>> **연대** {key: 시대 - value: **작품 리스트**} <br />  
>>> **작품 리스트** [ **작품명1**, 작품명2, ... ]   
>>>> **- OUTPUT :** <br /> **작품명** & 작품 설명 ( 작품 딕셔너리[**작품명**] )



 
</details>

<br />


**💡 Link :** [Art box - Gallery](http://118.67.142.110:8000/show_data "Art box - Gallery"){:target="_blank"}  