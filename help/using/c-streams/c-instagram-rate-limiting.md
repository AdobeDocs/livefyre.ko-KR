---
description: Instagram은 Livefyre를 포함하여 Instagram API를 사용하는 모든 회사가 토큰당 시간당 5,000개의 요청에서 토큰당 시간당 200개의 요청으로 수행할 수 있는 요청 수를 변경했습니다. 이를 속도 제한이라고 합니다.
title: Instagram 속도 제한
exl-id: b13db09b-fb5a-4711-a566-d0976172e35e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# 문제 해결:instagram 내용 제한 사항 {#instagram-rate-limiting}

Instagram은 Livefyre를 포함하여 Instagram API를 사용하는 모든 회사가 토큰당 시간당 5,000개의 요청에서 토큰당 시간당 200개의 요청으로 수행할 수 있는 요청 수를 변경했습니다. 이것은 *비율 제한*&#x200B;이라고 합니다.

토큰은 Instagram 계정과 동일합니다.

다음 이유로 Instagram에서 컨텐츠를 검색하거나 가져오는 기능을 제한하는 오류가 발생할 수 있습니다.

* 둘 이상의 스트림에 계정을 하나 사용하고 있습니까?
* 많은 수의 Instagram 스트림 보유
* 대용량 해시 태그를 사용할 수 있습니다(예: `#cats` 또는 `#beach`).

instagram 속도 제한의 영향을 줄이기 위해:

* 여러 Instagram 계정을 네트워크에 연결합니다. 네트워크에 Instagram 계정을 추가하는 방법에 대한 자세한 내용은 [Instagram 계정 정보](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)를 참조하십시오.
사용하지 않는 Instagram 스트림 끄기
스트림이 올바른 키워드로 타깃팅되었는지 확인하고 스마트 태그 필터를 사용하여 쿼리를 보다 정확하게 만들 수 있습니다. 스마트 태그 필터 사용 방법에 대한 자세한 내용은 [스마트 태그](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md)를 참조하십시오.
여러 사람이 동일한 Instagram 계정을 하나의 네트워크에서 사용하여 Instagram 컨텐츠를 조정하는 경우 시간을 최소화할 수 있습니다.
