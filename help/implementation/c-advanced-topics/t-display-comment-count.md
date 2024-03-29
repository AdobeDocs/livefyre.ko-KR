---
description: 색인 페이지에 표시할 특정 컬렉션의 게시물 및 댓글 수를 선택합니다.
title: 주석 수 표시
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# 주석 수 표시{#display-comment-count}

색인 페이지에 표시할 특정 컬렉션의 게시물 및 댓글 수를 선택합니다.

Livefyre `CommentCount.js`을(를) 사용하면 사이트에서 컬렉션에 대한 콘텐츠 수를 가져올 수 있습니다. Apps는 현재 컬렉션에 대한 댓글 수를 표시하지만 사이트 전체에 이러한 카운트를 게시하는 것은 유용할 수 있습니다. 이 기능은 데이터베이스의 콘텐츠를 유지하지 않거나 CMS 데이터베이스가 Livefyre와 동기화되지 않은 경우에 특히 유용합니다.

1. JavaScript를 로드합니다.

   `CommentCount.js`을 사용하려면 먼저 JavaScript 파일을 사용하려는 페이지 또는 템플릿의 `<head>` 섹션에 포함시킵니다.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. HTML 요소를 바인딩합니다.

   스크립트가 로드되면 클래스 이름이 `livefyre-commentcount`인 페이지의 다른 요소를 찾으려고 시도합니다. 이러한 각 요소에 대해 스크립트는 `data-lf-site-id` 및 `data-lf-article-id` HTML 속성을 찾고 이러한 속성을 사용하여 Livefyre에서 컨텐츠를 가져오고 각 요소를 최신 값으로 업데이트합니다.

   예를 들어 다음 요소가 업데이트됩니다.

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >`CommentCount.js` 코드는 실제 수로 업데이트할 숫자 값을 확인합니다. 태그 사이에 숫자 값을 포함해야 합니다.

   **예 1** (URL을 아티클 ID로 사용):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **예 2** (번호가 매겨진 시스템을 아티클 ID로 사용):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 옵션 구성을 참조하십시오.

   내용 개수 대체 방법을 더 잘 제어하려면 `LF.CommentCount()`을 호출하고 구성 옵션이 포함된 개체를 전달합니다. 바꿔야 할 모든 요소가 DOM에 있으면 함수를 호출해야 합니다. 이 메서드를 호출할 수 있는 가장 좋은 위치는 바닥글이므로 DOM이 로드될 때, 문서 및 창 준비 이벤트 전에 발생합니다.

   다음 구성 옵션을 허용합니다.

* **replacer:** Function 또는 Regex를 사용하여 각 컨텐츠 카운트의 텍스트를 대체합니다.

* **함수:** 각 요소에서 대체 작업을 수행하는 데 사용됩니다. 함수의 인수는 다음과 같습니다.

   **요소:** 업데이트 중인 HTML 요소입니다.
   **count:** 이 요소의 컨텐츠 카운트입니다.

* **regex:** 요소 텍스트의 일부를 개수로 대체할 부분을 결정하는 데 사용됩니다.

   **예**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >바꾸기를 사용하여 댓글 수 메시지를 사용자 정의하거나 국제화합니다.
