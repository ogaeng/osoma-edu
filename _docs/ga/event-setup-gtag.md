---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 이벤트 설정(gtag.js)
subtitle: 
description: gtag 방식으로 GA4 이벤트 설정하는 방법을 실습합니다.
permalink: /ga/event-setup-gtag/
date: 2023-04-03 00:00:00 +0900
video_id: -F7hZ5_kW1k
---

## [GA4]이벤트 설정 문서
📄 [https://developers.google.com/analytics/devguides/collection/ga4/events](https://developers.google.com/analytics/devguides/collection/ga4/events){:target="_blank"}

## 이벤트 작동 스크립트 양식

{% highlight javascript %}
{% raw %}

gtag('event', '이벤트 이름', {
    '이벤트 매개변수 키': '이벤트 매개변수 값'
});

{% endraw %}
{% endhighlight %}

## 버거 메뉴 다운로드 이벤트

{% highlight html %}
{% raw %}

<script>
	document.querySelector('#buger-menu').addEventListener('click', function(){
		gtag('event', 'click_button', {
			'name': '버거 메뉴 다운로드'
		});
	});
</script>

{% endraw %}
{% endhighlight %}