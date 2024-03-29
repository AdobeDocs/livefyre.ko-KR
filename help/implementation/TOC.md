---
product: livefyre
audience: end-user
user-guide-title: Livefyre 구현 안내서
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Livefyre 구현 안내서 {#implementation}

+ [Livefyre 구현 안내서](home.md)
+ 시작하기 {#getting-started}
   + [Livefyre 통합 시작하기](c-getting-started/c-getting-started.md)
   + 구현 과정 {#implementation-process}
      + [구현 과정](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [앱 통합 유형](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [앱 구현](c-getting-started/designer-app-implementation.md)
      + [제3자 통합을 통해 Livefyre 구현](c-app-integrations/implement-livefyre-3rd-party.md)
      + [아키텍처](c-getting-started/c-implementation-process/c-architecture.md)
      + [앱 포함](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [Livefyre.js를 사용하여 앱에 인증 추가](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [서버 측 토큰 작성](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta 토큰](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [사용자 인증 토큰](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [CollectionMeta 토큰을 사용하여 컬렉션 만들기](t-create-a-collectionmeta-token.md)
      + [체크섬 만들기](c-creating-a-checksum.md)
+ ID 통합 {#identity-integration}
   + [ID 통합](t-about-identity-integration/t-about-identity-integration.md)
   + [인증 패키지](t-about-identity-integration/c-authorization-package.md)
   + [AuthDelegate 개체](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [외부 시스템에 사용자 권한 게시(선택 사항)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + SSO {#implementing-sso} 구현
      + [SSO 구현](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [디버깅 인증 위임](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + Livefyre {#sync-ping-for-pull}과 동기화
      + [Pull용 Ping을 사용하여 Livefyre와 동기화](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [풀 끝점 만들기](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [Studio에 끝점 등록](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [Ping 구축](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [요청 구조 가져오기](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [풀링 응답에 대한 Ping 작성](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Livefyre ID {#livefyre-identity}
   + [Livefyre ID](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [Livefyre ID 활성화](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + Livefyre ID {#use-social-apps-with-livefyre-identity}에서 소셜 앱 사용
      + [소셜 앱 만들기](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [Livefyre ID와 함께 사용할 Facebook 앱 만들기](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [Livefyre ID와 함께 사용할 Twitter 앱 만들기](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [Yahoo! 만들기 Livefyre ID에 사용할 앱](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [Livefyre ID와 함께 사용할 Microsoft Live ID 앱 만들기](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [Livefyre ID와 함께 사용할 LinkedIn 앱 만들기](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [Livefyre ID에서 사용할 GitHub ID 앱 만들기](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [Studio를 사용하여 소셜 앱을 Livefyre 구현에 연결](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [페이지에 Livefyre.js 추가](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [Livefyre ID 초기화](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Livefyre ID에 대한 이메일](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [잔레인 캡처/후면판](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + 설치 {#installation}
      + [라이브러리 설치](c-installing-libraries/c-installing-libraries.md)
      + [클래스 및 메서드](c-installing-libraries/c-methods-livefyre.md)
      + [네트워크 메서드](c-installing-libraries/c-network-methods.md)
      + [setSSL 네트워크 메서드](c-installing-libraries/r-setssl-method.md)
      + [buildLivefyreToken 네트워크 메서드](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [buildUserAuthToken 네트워크 메서드](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken 네트워크 메서드](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl 네트워크 메서드](c-installing-libraries/r-setusersyncurl-method.md)
      + [syncUser 네트워크 메서드](c-installing-libraries/r-syncuser-method.md)
      + [getUrn 네트워크 메서드](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser 네트워크 메서드](c-installing-libraries/r-geturnforuser-method.md)
      + [getNetworkName 네트워크 메서드](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite Network 메서드](c-installing-libraries/r-getsite-method.md)
      + [네트워크 클래스 메서드](c-installing-libraries/c-network-class-methods.md)
      + [컬렉션 클래스 메서드](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate 컬렉션 메서드](c-installing-libraries/r-createorupdate-collection-method.md)
      + [buildCollectionMetaToken 컬렉션 메서드](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [buildChecksum 컬렉션 메서드](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent 컬렉션 메서드](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn 컬렉션 메서드](c-installing-libraries/r-geturn-collection-method.md)
      + [사이트 클래스 메서드](c-installing-libraries/c-site-methods.md)
      + [buildBlogCollection 사이트 메서드](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [buildChatCollection 사이트 메서드](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentsCollection 사이트 메서드](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [buildCountingCollection 사이트 메서드](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [buildRatingsCollection 사이트 메서드](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [buildReviewsCollection 사이트 메서드](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [buildSitenotesCollection 사이트 메서드](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [buildCollection 사이트 메서드](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn 사이트 메서드](c-installing-libraries/r-geturn-site-method.md)
      + [예](c-installing-libraries/c-libraries-examples.md)
   + Mobile SDK {#mobile-sdks}
      + [Mobile SDK](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [Livefyre 토큰 만들기 C#](c-creating-livefyre-tokens-c-.md)
+ 앱 통합 {#app-integrations}
   + [대화](c-app-integrations/c-app-integratios-chat.md)
   + 설명 {#comments}
      + [댓글](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [라이브 블로그](c-app-integrations/c-live-blog-integration.md)
   + [평가](c-app-integrations/c-reviews-integration.md)
   + 사이드노트 {#sidenotes}
      + [사이드노트 통합](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [페이지에 사이드노트 추가](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [사이드노트 앱 이벤트](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [사이드노트 구성 옵션](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [사이드노트 사용자 지정 스타일](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [사이드노트 사용자 지정 문자열](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [사이드노트 구현](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors 메서드](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [맵](c-app-integrations/c-map-integration.md)
   + [미디어 벽](c-app-integrations/c-media-wall-integration.md)
   + [트렌딩](c-app-integrations/c-trending-integration.md)
+ 앱 사용자 지정 {#app-customizations}
   + [앱 맞춤화](c-app-customizations/c-app-customizations.md)
   + [표시 옵션 변경](c-app-customizations/c-change-display-options.md)
   + [CSS 클래스](c-app-customizations/c-css-classes.md)
   + [CSS 클래스 저장](c-app-customizations/c-storify-css-classes.md)
   + [번역 세트](c-app-customizations/c-translation-sets.md)
   + [Livefyre 로고 이동](c-app-customizations/c-move-the-livefyre-logo.md)
   + [미디어 제한](c-app-customizations/c-restrict-media.md)
   + [앱 요소 숨기기](c-app-customizations/c-hide-app-elements.md)
   + [Mention 아이콘 변경](c-app-customizations/c-change-mention-icon.md)
   + [내용 강조 표시](c-app-customizations/c-highlight-content.md)
   + [날짜 및 타임스탬프 사용자 지정](c-app-customizations/c-date-time-stamp.md)
   + 기능 내용 {#feature-content}
      + [기능 컨텐츠](c-app-customizations/t-feature-content.md)
      + [Studio에서 콘텐츠 제공 활성화](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [앱에서 기능할 콘텐츠 선택](c-app-customizations/t-select-content-to-feature.md)
      + [Studio에서 기능할 내용 선택](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [CSS를 사용하여 주요 컨텐츠의 스타일 지정](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [기능 API](c-app-customizations/c-feature-apis.md)
   + [AuthDelegate를 사용하여 Janrain을 Livefyre에 연결](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [주요 API를 사용하여 주요 컨텐츠 취합](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + 내용 스타일 지정 {#style-content}
      + [사용자 그룹 콘텐츠 스타일 지정](c-app-customizations/c-style-user-group-content.md)
      + [그룹에 사용자 추가](c-app-customizations/c-adding-users-to-groups.md)
   + 사용자 지정 스타일 적용 {#apply-custom-styles}
      + [사용자 정의 스타일 적용](c-app-customizations/c-applying-custom-styles-.md)
      + [사용자 정의 단추 추가](c-app-customizations/t-add-custom-buttons.md)
   + Javascript 이벤트 {#javascript-events}
      + [JavaScript 이벤트 정의 및 예](c-app-customizations/c-javascript-events.md)
      + [시각화 앱에 대한 Javascript 이벤트](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [미디어 담벼락에 대한 Javascript 이벤트](c-app-customizations/c-javascript-events-media-wall.md)
      + [대화 앱에 대한 Javascript 이벤트](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [댓글 앱 포함](c-app-customizations/c-embed-a-comments-app.md)
   + [참조 추적](c-app-customizations/c-referral-tracking.md)
   + [장치 및 브라우저 지원](c-app-customizations/c-device-and-browser-support.md)
   + [Twitter 표시 요구 사항](c-app-customizations/c-twitter-display-requirements.md)
+ [스트레스 테스트 정책](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [Adobe Analytics 및 DTM(Dynamic Tag Manager)에서 Livefyre 사용](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [다른 분석 도구에서 Livefyre 사용](livefyre-analytics/c-livefyre-analytics.md)
   + [Livefyre 분석 이벤트](livefyre-analytics/c-livefyre-analytics-events.md)
+ [AEM과 Livefyre 통합](c-livefyre-aem-integration.md)
+ 고급 항목 {#advanced-topics}
   + [주석 수 표시](c-advanced-topics/t-display-comment-count.md)
   + [소셜 공유 활성화](c-advanced-topics/c-enabling-social-sharing.md)
   + [활동 스트림](c-advanced-topics/c-activity-stream.md)
   + [Bootstrap HTML](c-advanced-topics/c-bootstrap-html.md)
   + [컬렉션 변경](c-advanced-topics/c-change-collection.md)
   + [여러 컬렉션](c-advanced-topics/c-multiple-collections.md)
   + [핵심 앱 유형 전환](c-advanced-topics/c-switch-core-app-types.md)
   + [소셜 카운터](c-advanced-topics/c-social-counter.md)
   + [Livefyre 앱과 함께 Bootsrap 및 스트림 API 사용](c-advanced-topics/bootstrap-stream-api.md)
