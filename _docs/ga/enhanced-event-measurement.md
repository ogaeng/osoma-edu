---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 향상된 측정
subtitle: 
description: GA4의 새로운 기능인 향상된 이벤트 측정에 대해 알아봅니다.
permalink: /ga/enhanced-event-measurement/
date: 2023-04-04 00:00:00 +0900
video_id: 8b8cK6jWUeY
---

## Omnibug - Chrome 확장 프로그램

- [Omnibug 플러그인](https://chrome.google.com/webstore/detail/omnibug/bknpehncffejahipecakbfkomebjmokl){:target="_blank"}

## [GA4]향상된 이벤트 측정 문서
📄 [https://support.google.com/analytics/answer/9216061](https://support.google.com/analytics/answer/9216061){:target="_blank"}

## gtag에서 GA4 page_view 이벤트 전송 차단

- 아래와 같이 gtag 구성 태그에 send_page_view 옵션을 추가합니다.

{% highlight javascript %}
{% raw %}

gtag('config', '측정 ID', {
    'send_page_view': false
});

{% endraw %}
{% endhighlight %}

## GTM에서 GA4 page_view 이벤트 전송 차단

- 태그 메뉴에 접속합니다.
- 기존에 생성한 GA4 구성 태그를 엽니다.
- **이 구성이 로드될 때 페이지 조회 이벤트 전송**의 체크를 해제합니다.

![트리거 설정](/images/docs/ga/enhanced-event-measurement/01.png)