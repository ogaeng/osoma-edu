---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 설치 실습(GTM)
subtitle: 
description: 구글 태그 매니저를 이용해 GA4 설치하는 방법을 알아봅니다.
permalink: /ga/setup-gtm/
date: 2023-02-20 13:00:00 +0900
video_id: 9v43kAol0nw
---

## 실습 준비 안내

### 1. netlify 회원가입

- 우리 강의에서는 실습 파일을 웹에 배포하여 테스트하기 위해 netlify를 사용합니다.
- [netlify 웹사이트](https://www.netlify.com/){:target="_blank"}에 접속해 회원 가입을 합니다.

### 2. VSCode 설치

- 우리 강의에서는 코드 편집을 위해 VSCode를 사용합니다.
- 만약, 이미 사용 중인 다른 편집 도구가 있다면 그 도구를 사용해도 무방합니다.
- [VSCode 웹사이트](https://code.visualstudio.com/){:target="_blank"}에 접속해 VSCode를 다운로드하고 설치합니다.

### 3. 실습 웹사이트 다운로드

- 실습에 활용할 웹사이트를 제공합니다.
- [여기](https://drive.google.com/file/d/16qtvbSIN2ev4cx6Ms1HkoRu625x2yWpV/view?usp=sharing){:target="_blank"}를 눌러 웹사이트 파일을 다운로드합니다.
- 다운로드한 파일의 압축을 풀고 원하는 폴더로 이동합니다.

## 작업을 위한 플러그인 설치

### Tag Assistant Companion Chrome 확장 프로그램 추가

- [Tag Assistant Companion 플러그인](https://chrome.google.com/webstore/detail/tag-assistant-companion/jmekfmbnaedfebfnmakmokmlfpblbfdm){:target="_blank"}을 크롬에 추가합니다.

## Google Tag Manager 컨테이너 생성

- [Google Tag Manager 웹사이트](https://tagmanager.google.com/){:target="_blank"}에 접속합니다.
- 계정 만들기를 눌러 계정과 컨테이너를 생성합니다.(타겟 플랫폼: 웹 선택)

## Google Tag Manager 설치

- 웹사이트에 GTM 스니펫을 추가하여 설치합니다.

![GTM 설치](/images/docs/ga/setup-gtm/00.png)

## GA4 태그 생성

- 태그 메뉴에서 새로 만들기 버튼을 누릅니다.
- 태그 유형에서 Google 애널리틱스: GA4 구성을 선택합니다.
- 측정 ID 항목에 GA4 데이터 스트림의 측정 ID를 입력합니다.(예: G-XXXXXXXXXX)
- 트리거를 눌러 All Pages를 선택합니다.
- 태그의 이름을 입력하고 저장합니다.

![GTM 태그](/images/docs/ga/setup-gtm/01.png)

## 미리보기

- 태그 생성을 완료한 뒤 미리보기 버튼을 눌러 Tag Assistant를 실행합니다.
- 미리보기 창이 뜨면 테스트할 웹사이트 주소를 입력하고 Connect를 누릅니다.
![GTM 미리보기](/images/docs/ga/setup-gtm/02.png)
- Tag Assistant에서 태그가 Fired 되어있는지 확인합니다.
![GTM 태그 Fired](/images/docs/ga/setup-gtm/03.png)