---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 이벤트 설정(Flutter, 모바일 앱)
subtitle: 
description: 플러터로 제작된 앱 환경에서 Firebase Analytics 이벤트 설정하는 방법을 실습합니다.
permalink: /ga/event-setup-flutter/
date: 2023-05-02 00:00:00 +0900
video_id: 6Bp_BkOCneU
---

## 1. 관련 문서 링크

- 📄 [Firebase Analytics 이벤트 로깅](https://firebase.google.com/docs/analytics/events?platform=flutter&hl=ko){:target="_blank"}
- 📄 [Firebase Analytics 디버깅 이벤트](https://firebase.google.com/docs/analytics/debugview){:target="_blank"}
- 📄 [안드로이드 SDK 플랫폼 도구 다운로드](https://developer.android.com/studio/releases/platform-tools?hl=ko){:target="_blank"}

## 2. 이벤트 함수 작성

{% highlight dart %}
{% raw %}

Future<void> gaEvent(String eventName, Map<String, dynamic> eventParams) async {
  await FirebaseAnalytics.instance.logEvent(
    name: eventName,
    parameters: eventParams,
  );
}

{% endraw %}
{% endhighlight %}

- `Future<void>`는 반환하는 값이 없는 비동기 함수 → 비동기란 특정 코드의 작업이 끝날 때 까지 실행을 멈추지 않고 다음 코드를 먼저 실행합니다.
- `Map`은 키-값 쌍으로 이루어진 자료형으로 `eventParams`에 들어갈 이벤트 매개변수는 `{매개변수 키: 매개변수 값}`으로 구성되어 있습니다.
- 매개변수 키는 `String`이고 매개변수 값은 다양한 데이터 형식이 들어올 수 있어 `dynamic`으로 설정합니다.

## 이벤트 실행

{% highlight dart %}
{% raw %}

gaEvent('click_floating', {
  'color': 'blue',
  'count': _counter
});

{% endraw %}
{% endhighlight %}

- 플로팅 버튼을 누르면 실행되는 `click_floating` 이벤트가 수집됩니다.
- `count` 매개변수에는 버튼을 누를 때의 숫자가 수집됩니다.

## 3. 안드로이드 디버깅 모드 사용 설정

### 디버깅 모드 사용

에뮬레이터를 실행한 뒤 터미널에서 아래 명령어를 실행해 디버깅 모드를 시작합니다.

{% highlight shell %}
{% raw %}

adb shell setprop debug.firebase.analytics.app <패키지명>

{% endraw %}
{% endhighlight %}

### 디버깅 모드 사용 중지

디버깅 모드를 중지하려면 터미널에 아래 명령어를 실행합니다.

{% highlight shell %}
{% raw %}

adb shell setprop debug.firebase.analytics.app .none.

{% endraw %}
{% endhighlight %}