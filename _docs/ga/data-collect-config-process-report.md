---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 데이터 수집, 처리, 보고 구조 이해하기
subtitle: 
description: GA4에서 데이터가 어떻게 수집되고 처리되어 보고서로 출력되는지 그 과정을 알아봅니다.
permalink: /ga/data-collect-config-process-report/
date: 2023-02-20 13:00:00 +0900
video_id: 6CIXzQkh2to
---

## GA4의 데이터 전송, 처리, 보고 구조

수집(Collection) ➝ 구성(Configuration) ➝ 처리(Processing) ➝ 보고(Reporting)

![데이터 구조](/images/docs/ga/data-collect-config-process-report/01.jpg)

## 수집(Collection)

### gtag.js

구글 애널리틱스 4는 gtag를 로드하고 GA4 구성이 이루어지는 순서로 실행됩니다.

![gtag](/images/docs/ga/data-collect-config-process-report/02.jpg)

### 이벤트 전송

사용자의 행동을 수집하기 위해선 이벤트를 구글 애널리틱스 서버로 전송해야 합니다.

![이벤트](/images/docs/ga/data-collect-config-process-report/03.jpg)

이벤트가 전송될 때 측정 ID, OS, 브라우저 정보, 페이지 정보 등이 함께 전송됩니다.

![이벤트 전송](/images/docs/ga/data-collect-config-process-report/04.jpg)

## 구성(Configuration)

구성 단계에서는 웹 인터페이스 혹은 [Admin API](https://developers.google.com/analytics/devguides/config/admin/v1){:target="_blank"}를 통해 설정한 GA4 속성의 사용자 권한, 데이터 수집/보관 설정, 내부 트래픽, 맞춤 측정기준 등의 설정이 적용되는 단계입니다.

## 처리(Processing)

구성 단계에서 적용된 내용을 바탕으로 데이터를 처리합니다.

## 보고(Reporting)

처리된 데이터를 웹 인터페이스 혹은 [Data API](https://developers.google.com/analytics/devguides/reporting/data/v1){:target="_blank"}를 이용해 출력하고 확인할 수 있습니다.