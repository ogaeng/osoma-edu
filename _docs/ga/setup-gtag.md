---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 설치 실습(gtag.js)
subtitle: 
description: GA4에서 제공하는 기본 설치 방식을 실습합니다.
permalink: /ga/setup-gtag/
date: 2023-02-20 13:00:00 +0900
video_id: exN0kubP0Kg
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
- [여기](https://drive.google.com/file/d/1oC8DWzRLAgDEc2ORnY5EgHVK8CxguRpO/view?usp=sharing){:target="_blank"}를 눌러 웹사이트 파일을 다운로드합니다.
- 다운로드한 파일의 압축을 풀고 원하는 폴더로 이동합니다.

## 테스트를 위한 플러그인 설치

### 구글 애널리틱스 디버거 Chrome 확장 프로그램 추가

- [Google Analytics Debugger 플러그인](https://chrome.google.com/webstore/detail/google-analytics-debugger/jnkmfdileelhofjcijamephohjechhna){:target="_blank"}을 크롬에 추가합니다.

## GA4 설치

- 웹사이트 <head> 영역에 GA4 태그를 추가하여 설치합니다.

![gtag](/images/docs/ga/setup-gtag/01.png)