---
description: Livefyre의 규칙 및 Livefyre의 콘텐츠 구성에 대해 학습합니다.
seo-description: Livefyre의 규칙 및 Livefyre의 콘텐츠 구성에 대해 학습합니다.
seo-title: 아키텍처
solution: Experience Manager
title: 아키텍처
uuid: 94358 E 6 C -954 A -4 A 52-9 BB 2-D 800 B 2933130
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 아키텍처{#architecture}

Livefyre의 규칙 및 Livefyre의 콘텐츠 구성에 대해 학습합니다.

이 섹션에서는 Livefyre 네트워크 아키텍처에 대한 개요를 제공합니다.

## 네트워크 및 사이트 개요

Livefyre는 네트워크와 사이트별로 사용자와 컨텐츠를 구성합니다. 모든 네트워크에는 하나 이상의 사용자 계정이 연결되어 있을 수 있으며, 각 네트워크는 하나 이상의 Livefyre 사이트를 포함할 수 있습니다. Livefyre 사이트는 컬렉션의 임의 그룹입니다. 하나의 컬렉션은 CMS에서 하나의 아티클 ID로 매핑됩니다.

## 네트워크 이해 {#section_hqt_4m4_xz}

여러 도메인이 있는 고객은 단일 Livefyre 네트워크를 사용하여 모든 도메인에 걸쳐 사용자 계정을 공유할 수 있습니다. 서로 다른 도메인에 대해 별도의 사용자 계정을 유지하려면 별도의 Livefyre 네트워크가 필요합니다.

구성 설정은 사이트, 네트워크 및 컬렉션에 적용할 수 있습니다 (위 그림에서 대화라고 함).

>[!NOTE]
>
>일부 설정은 네트워크 수준 (이메일 알림 환경 설정, 이메일 주소, 이메일 사용자 정의 로고 등) 에서만 사용할 수 있습니다. 이러한 설정이 도메인마다 달라지도록 하려면 여러 네트워크를 사용해야 합니다.

## 사이트 이해 {#section_vjw_nm4_xz}

사이트는 임의의 아티클 그룹입니다. 그룹화는 여러 컨텐츠 그룹에 서로 다른 중재자를 할당할 수 있으므로 유용합니다. 중재자와 소유자는 컨텐츠를 중재하고 네트워크 또는 사이트 수준에서 관리자 설정을 구성할 수 있도록 설정할 수 있습니다. 일부 중재자가 특정 컬렉션만 보도록 하려는 경우 이러한 컬렉션은 별도의 Livefyre 사이트로 설정할 수 있습니다.

>[!NOTE]
>
>사용자 정의 네트워크에 있는 사이트 수에는 제한이 없습니다.

## 앱 시퀀스 다이어그램 {#section_mw2_lm4_xz}

Livefyre가 제공하는 사용자 정의 기능을 구현하려는 경우 또는 간단히 문제를 디버깅해야 하는 경우 Livefyre 앱 요청/응답 흐름이 작동하는 방식을 이해하는 것이 도움이 됩니다.

![](assets/appsequencediagram.png)

1. 클라이언트가 사이트를 히트하면 Livefyre 앱을 사이트 ID 및 아티클 ID로 인스턴스화합니다.
1. 사용자를 인증하고 (트래픽 평가 및 사이트 보호 시 중요한 경우) Livefyre를 사이트 정보와 사용자 프로필 토큰으로 보내십시오.
1. Livefyre를 사이트 ID와 아티클 ID로 전송하여 앱을 초기화합니다.

   Livefyre는 초기 컨텐츠를 반환합니다.

   이 컨텐츠를 페이지로 보내고 앱을 표시합니다.

1. 페이지에 표시되는 컨텐츠를 업데이트하려면 페이지에서 최신 이벤트 ID를 livefyre로 전송합니다. 새로운 콘텐츠를 사용할 수 있는 경우 이 컨텐츠가 반환됩니다.

   새 컨텐츠로 페이지를 다시 로드하고 프로세스를 무기한으로 반복합니다.

1. 사용자가 새 컨텐츠를 게시할 수 있도록 허용하는 경우, 새 컨텐츠가 사이트에 게시되면 이벤트를 트리거하여 Livefyre에 게시합니다. Livefyre는 사이트를 업데이트하는 데 사용할 수 있는 업데이트된 스트림을 반환합니다.