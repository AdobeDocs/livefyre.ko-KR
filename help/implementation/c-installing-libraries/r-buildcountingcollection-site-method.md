---
description: 카운팅 유형으로 인스턴스화된 Collection 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.
title: buildCountingCollection 사이트 메서드
exl-id: 02186eff-1f2f-41e5-8232-033b646ef224
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# buildCountingCollection 사이트 메서드{#buildcountingcollection-site-method}

카운팅 유형으로 인스턴스화된 Collection 개체를 반환합니다. 컬렉션 개체에서 create_or_update()를 실행하여 빌드 프로세스를 완료합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| title | 문자열 | 컬렉션의 제목입니다. |
| articleId | 문자열 | 사이트 내 컬렉션을 식별하기 위해 선택한 고유한 아티클 ID. |
| url | 문자열 | 이 컬렉션에 대한 기본 절대 URL. |

## Java 예 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## NodeJS 예 {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## PHP 예 {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Python 예 {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## 루비의 예 {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```
