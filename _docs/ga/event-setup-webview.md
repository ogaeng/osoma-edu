---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 이벤트 설정(Webview, 모바일 앱)
subtitle: 
description: Webview를 주로 활용하는 하이브리드 앱 환경에서 Firebase Analytics 이벤트 설정하는 방법을 실습합니다.
permalink: /ga/event-setup-webview/
date: 2023-08-15 22:00:00 +0900
video_id: apON1XvDego
---

## 1. Firebase Analytics의 Webview 이벤트 처리 방식

모바일 앱의 웹뷰 영역에서 이벤트를 수집하려면 웹뷰 내 웹사이트에서 특정 행동이 발생할 때 웹뷰에서 네이티브 영역으로 데이터를 전달하고 네이티브 영역에서 전달받은 데이터를 이용해 파이어베이스 애널리틱스 이벤트를 전송하는 방식으로 사용합니다.(Webview → Native → 이벤트 수집)

## 2. 관련 문서 링크

- 📄 [Firebase Analytics Webview에서 애널리틱스 사용](https://firebase.google.com/docs/analytics/webview?hl=ko&platform=ios){:target="blank"}
- 📄 [Firebase Analytics 디버깅 이벤트](https://firebase.google.com/docs/analytics/debugview?hl=ko#ios+){:target="blank"}

## 3. 웹사이트 이벤트 실행

{% highlight html %}
{% raw %}

<script>
	// 버거 메뉴 다운로드 버튼 클릭 이벤트
	document.querySelector('#buger-menu').addEventListener('click', function(){
		logEvent('download_burger_menu', {
			'menu': '버거 메뉴'
		});
	});
</script>

{% endraw %}
{% endhighlight %}

- 웹사이트에서 버거 메뉴 다운로드 버튼을 누르면 Native 영역으로 `download_burger_menu` 이벤트를 전달합니다.

## 4. iOS 디버깅 모드 사용 설정

### 디버깅 모드 사용

Xcode의 Product > Edit Scheme 메뉴를 실행하고 Run(Side menu) > Arguments(Tab) > Arguments Passed On Launch에 아래 인수를 추가합니다.

{% highlight shell %}
{% raw %}

-FIRDebugEnabled

{% endraw %}
{% endhighlight %}

![iOS 디버깅 모드 설정](/images/docs/ga/event-setup-webview/01.png)

### 디버깅 모드 사용 중지

디버깅 모드를 종료하려면 Arguments Passed On Launch에 아래 인수를 추가합니다.

{% highlight shell %}
{% raw %}

-FIRDebugDisabled

{% endraw %}
{% endhighlight %}