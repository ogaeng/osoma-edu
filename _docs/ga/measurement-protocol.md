---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 이벤트 설정(측정 프로토콜, Measurement Protocol)
subtitle: 
description: GA4의 측정 프로토콜(Measurement Protocol)을 이용해 이벤트를 전송하는 방법에 대해 안내합니다.
permalink: /ga/measurement-protocol/
date: 2023-08-17 10:00:00 +0900
video_id: rfSSjajHDNQ
---

## 1. 측정 프로토콜(Measurement Protocol)이란?

측정 프로토콜은 HTTP 요청을 통해 구글 애널리틱스 4 서버로 직접 이벤트를 전송할 수 있는 프로토콜입니다.

### 사용 사례

- 서버에서 직접 GA4 서버로 데이터를 전송하고 싶을 때
- 정기 구독 서비스의 정기 결제에 대한 이벤트를 GA4로 전송하고 싶을 때
- 오프라인에서 발생한 전환을 GA4로 전송하고 싶을 때

### 참고 사항

- 측정 프로토콜은 기본적으로 이벤트와 사용자 속성 정보만 전송이 가능하며 사용자의 지역, 기기 정보 등을 자동으로 수집하지 않습니다.

## 2. 측정 프로토콜을 이용한 이벤트 전송

### API 비밀번호 발급

GA4 관리 → 속성 → 데이터 스트림 → 측정 프로토콜 API 비밀번호로 접속해 API 비밀번호를 만듭니다.

### URL endpoint

아래 URL로 POST 요청을 보냅니다.

{% highlight plain %}
{% raw %}

HOST: https://www.google-analytics.com/mp/collect?measurement_id={측정 ID}&api_secret={API 비밀번호}
Content-Type: application/json

{% endraw %}
{% endhighlight %}

### Payload

{% highlight json %}
{% raw %}

{
	"client_id": "<사용자 Client ID 값>",
	"timestamp_micros": "<이벤트 실행 시간 타임스탬프 값(마이크로초 단위)>",
	"events": [{
		"name": "<이벤트 이름>",
		"params": {
			"<이벤트 매개변수 이름 1>": "<이벤트 매개변수 값 1>",
			"<이벤트 매개변수 이름 2>": "<이벤트 매개변수 값 2>"
		}
	}]
}

{% endraw %}
{% endhighlight %}

## 3. 유효성 검사

### URL endpoint

유효성 검사를 위해 아래 URL로 POST 요청을 보냅니다.

{% highlight plain %}
{% raw %}

HOST: https://www.google-analytics.com/debug/mp/collect?measurement_id={측정 ID}&api_secret={API 비밀번호}
Content-Type: application/json

{% endraw %}
{% endhighlight %}

## 4. 세션 ID 정보를 추가하여 세션 연결하기

### Payload

{% highlight json %}
{% raw %}

{
	"client_id": "<사용자 Client ID 값>",
	"timestamp_micros": "<이벤트 실행 시간 타임스탬프 값(마이크로초 단위)>",
	"events": [{
		"name": "<이벤트 이름>",
		"params": {
			"session_id": "<연결할 세션의 세션 ID>",
			"<이벤트 매개변수 이름 1>": "<이벤트 매개변수 값 1>",
			"<이벤트 매개변수 이름 2>": "<이벤트 매개변수 값 2>"
		}
	}]
}

{% endraw %}
{% endhighlight %}

- session_id 매개변수에 연결할 세션 ID 값을 입력합니다.(client_id와 session_id가 모두 일치해야 세션이 연결됩니다.)
- 세션 시작 후 72시간이 지나면 연결이 불가능합니다.

## 5. 관련 문서 링크

- 📄 [POSTMAN](https://www.postman.com/){:target="blank"}
- 📄 [측정 프로토콜 개요](https://developers.google.com/analytics/devguides/collection/protocol/ga4){:target="blank"}
- 📄 [Event Builder](https://ga-dev-tools.google/ga4/event-builder/){:target="blank"}