---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: "100% 완벽한 데이터 수집이 어려운 이유"
subtitle: 
description: 데이터 수집을 방해하는 요소에 대해 알아봅니다.
permalink: /ga/difficult-to-collect-perfect-data/
date: 2023-02-20 13:00:00 +0900
video_id: xFYehFUO9sw
---

GA가 데이터를 수집하려면 웹/앱에서 GA가 정상적으로 실행되어 수집 액션을 수행해야 합니다. 하지만 언제나 그렇듯 예상치 못한 문제가 생기기 마련입니다.

## 인터넷 통신 문제

인터넷 통신 상황이 좋지 못해 느려지거나 끊기는 상황이 발생해 웹/앱 로딩에 문제가 생긴다면 GA는 실행되지 않을 수 있습니다.

## 스크립트 오류/로드되지 않는 문제

- GA를 실행하는 gtag.js 혹은 SDK가 제대로 로드되지 않는 경우 GA는 실행되지 않아 데이터를 수집할 수 없습니다.
- GA가 제대로 로드되었더라도 이벤트 스크립트 등에 오류가 생긴다면 데이터 수집이 어려울 수 있습니다.

## 광고/트래커 차단

- 광고와 트래커를 차단하는 플러그인을 사용하는 사용자는 점점 늘어나고 있습니다.
- 차단 기능이 기본적으로 내장된 브라우저도 존재합니다.
- 이 경우 트래커 차단으로 인해 GA를 실행할 수 없어 데이터는 수집되지 않습니다.

이처럼 여러 요인으로 인해 데이터 수집이 누락되는 상황이 흔하게 발생할 수 있습니다. 그러므로 이런 제약으로 인해 완벽한 데이터 수집이 어렵다는 것을 인지하고 구글 애널리틱스를 어떻게 활용할지 방향을 잡아야 합니다.