---
description: 이전에 설정한 사용자 동기화 URL에서 사용자 정보를 가져오도록 Livefyre에 알려줍니다. 부울 값을 반환합니다.
title: syncUser 네트워크 메서드
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# syncUser 네트워크 메서드{#syncuser-network-method}

이전에 설정한 사용자 동기화 URL에서 사용자 정보를 가져오도록 Livefyre에 알려줍니다. 부울 값을 반환합니다.

| 변수 | 유형 | 설명 |
|--- |--- |--- |
| userId | 문자열 | Livefyre와 동기화할 사용자 ID입니다. 이 메서드를 호출하려면 먼저 Livefyre와 사용자 동기화 URL이 설정되어 있어야 합니다. |

## Java 예 {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

샘플 출력:

```
true
```

## NodeJS 예 {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

샘플 출력:

```
true
```

## PHP 예 {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

샘플 출력:

```
true
```

## Python 예 {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

샘플 출력:

```
True
```

## 루비의 예 {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

샘플 출력:

```
True
```
