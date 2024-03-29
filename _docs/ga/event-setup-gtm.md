---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 이벤트 설정(GTM)
subtitle: 
description: GTM 방식으로 GA4 이벤트 설정하는 방법을 실습합니다.
permalink: /ga/event-setup-gtm/
date: 2023-04-03 00:00:00 +0900
video_id: aZPllIQ40FI
---

## 1. 변수 만들기

- 변수 메뉴에 접속합니다.
- 기본 제공 변수의 [구성] 버튼을 누릅니다.
- **Click ID**를 체크합니다.

## 2. 트리거 만들기

- 트리거 메뉴에 접속합니다.
- [새로 만들기] 버튼을 누릅니다.
- 트리거 구성을 눌러 **링크만**을 선택합니다.
- **일부 링크 클릭**을 체크합니다.
- 아래 이미지와 같이 조건을 설정합니다.

![트리거 설정](/images/docs/ga/event-setup-gtm/01.png)

## 3. 태그 만들기

- 태그 메뉴에 접속합니다.
- [새로 만들기] 버튼을 누릅니다.
- 태그 구성을 눌러 **Google 애널리틱스: GA4 이벤트**를 선택합니다.
- 이전에 만든 구성 태그를 선택합니다.
- 이벤트 이름과 매개변수를 아래 이미지와 같이 설정합니다.

![태그 설정](/images/docs/ga/event-setup-gtm/02.png)

- 위에서 만든 링크 클릭 트리거를 선택합니다.