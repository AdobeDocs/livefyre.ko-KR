---
description: 선별된 소셜 항목의 수를 카운트합니다.
title: 소셜 카운터
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 10%

---

# 소셜 카운터{#social-counter}

선별된 소셜 항목의 수를 카운트합니다. 사용 가능한 끝점의 전체 목록을 보려면 Livefyre [API 참조](https://api.livefyre.com/docs) 섹션을 참조하십시오.

Social 카운터 API는 일정 기간 동안 특정 컬렉션의 일치하는 조정 규칙에 대한 카운트를 반환합니다.

>[!NOTE]
>
>이 API는 Twitter 해시 태그에만 사용할 수 있습니다.

소셜 카운터 API:

* 리소스
* 규칙 유형
* 응답

## 리소스 {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** Livefyre가 네트워크 이름을 제공했습니다. 예:`labs.fyre.co`의 *labs*
* **쿼리:** 모든 사이트, 아티클 ID, 카운트 정보를 가져오는 규칙 유형 튜플의 url-safe base64 인코딩 해시(사전 인코딩)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >쿼리는 10개 사이트, 아티클 ID, 규칙 유형 튜플로 제한됩니다. 이전 예에는 3개의 튜브가 포함됩니다.

* **** `(optional)` fromtime to graph;에서 는 생략하면 시작 및 기본값을 24시간 전에 지정합니다.
* **** `(optional)` untilly는 그래프의 상대 또는 절대 기간을 지정합니다.until은 생략할 경우 시작 및 기본값을 현재 시간(현재 시간)으로 지정합니다.

### 상대 시간

| 약자 | 단위 |
|---|---|
| s | 초 |
| min | 분 |
| h | 시간 |
| d | 일 |
| w | 주 |
| mon | 30일(월) |
| y | 365일(년) |

예:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## 절대 시간 {#section_xqr_jgc_11b}

형식:HH:MM_YYYMMDD

| 약자 | 의미 |
|---|---|
| HH | 시간(24시간 형식) |
| MM | 분 |
| YYYY | 4자리 연도 |
| MM | 월 |
| DD | 일 |

예:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## 규칙 유형 {#section_v53_xqb_11b}

| 값 | 유형 |
|---|---|
| 2 | Twitter |

예:

사이트 `123456` 및 아티클 ID `some-article-id` 및 규칙 유형 `2`에 대한 마지막 분 동안 카운트를 가져오려면 다음을 수행하십시오.`123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

응답 예:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
