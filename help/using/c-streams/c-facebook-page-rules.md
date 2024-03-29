---
description: facebook 페이지에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.
title: Facebook 페이지 규칙
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Facebook 페이지 규칙{#facebook-page-rules}

facebook 페이지에서 컨텐츠를 가져오는 스트림 규칙을 만들 수 있습니다.

facebook 페이지 규칙을 사용하여 Facebook 페이지에서 공개적으로 게시된 컨텐츠를 스트리밍할 수 있습니다. 컨텐츠는 Facebook 페이지 및 게시물 트래픽 패턴에 따라 변경되는 SocialSync와 동일한 빈도로 앱 또는 폴더로 가져올 수 있습니다. facebook 페이지 내의 링크도 지원되며, 스트림에 표시됩니다.

facebook 페이지 규칙을 만들어 Facebook 페이지의 콘텐츠를 앱 또는 폴더로 가져오려면 다음을 기준으로 필터링할 수 있습니다.

* **[!UICONTROL Facebook Page]**

   * 페이지의 **[!UICONTROL Name]**&#x200B;을 입력합니다. URL에 대해 후행 텍스트만 입력합니다. **예:** 다음 필드에서 컨텐츠를 추가하려면  `https://facebook.com/KellysSuperFunFanPage`필드에  ** KelysSuperFunFanPagein을  **[!UICONTROL Name]** 입력합니다.

   * 페이지 게시물에 사용자 댓글을 포함하려면 **[!UICONTROL Include Facebook Comments for each post]**&#x200B;을(를) 전환하십시오.
   * 다른 사용자로부터 게시물을 제외하려면 **[!UICONTROL Only Show Author Posts]**&#x200B;을(를) 전환합니다.

모든 스트림 규칙에 대한 추가 스트림 규칙 옵션은 모든 스트림 규칙에 대한 [스트림 규칙 옵션](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)을 참조하십시오.

>[!NOTE]
>
>Livefyre는 Facebook에서 수신한 컨텐트로 제한되므로 Facebook 페이지의 모든 게시물이 스트림에 포함될 것이라고 보장할 수 없습니다.

>[!NOTE]
>
>facebook SocialSync와 Facebook 페이지 규칙이 모두 특정 Facebook 페이지에 대해 활성화되어 있고 사용자 주석이 Facebook 페이지 규칙에 대해 활성화된 경우 스트림 규칙이 SocialSync를 재정의합니다. 컨텐츠는 SocialSync를 사용하지 않고 Facebook 페이지 조정 규칙만을 기반으로 앱으로 스트리밍됩니다.

facebook 페이지 조정에서 지원하는 컨텐츠 유형은 다음과 같습니다.

* 페이지 소유자 또는 관리자

   * 상태
   * 사진
   * 비디오를 링크로

* 표준 Facebook 사용자

   * 상태
   * 사진
   * 비디오를 링크로

* 제3자

   * 상태
