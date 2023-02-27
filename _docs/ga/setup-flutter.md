---
type: docs
layout: ga
category: 구글 애널리틱스 4 기초 강의
title: 구글 애널리틱스 4 설치 실습(Flutter, 모바일 앱)
subtitle: 
description: 플러터로 제작된 앱 환경에서 GA4를 어떻게 설치하는지 알아봅니다.
permalink: /ga/setup-flutter/
date: 2023-02-20 13:00:00 +0900
video_id: B0wDmwZ7pOg
---

## Flutter 설치

- [Flutter 공식 웹사이트의 가이드](https://docs.flutter.dev/get-started/install){:target="_blank"}를 통해 Flutter를 설치합니다.
- 새로운 Flutter 프로젝트를 생성합니다.

{% highlight shell %}
{% raw %}

flutter create <프로젝트명>

{% endraw %}
{% endhighlight %}

- VSCode로 생성한 Flutter 프로젝트를 불러옵니다.

## Firebase 프로젝트 생성

- [Firebase 웹사이트](https://firebase.google.com/){:target="_blank"}로 이동하여 새로운 프로젝트를 생성합니다.
- `이 프로젝트에서 Google 애널리틱스 사용 설정`을 활성화합니다.
![프로젝트 생성](/images/docs/ga/setup-flutter/01.png)

## Firebase CLI 설치

VSCode에서 터미널을 열고 npm을 통해 Firebase CLI를 설치합니다.

{% highlight shell %}
{% raw %}

npm install -g firebase-tools

{% endraw %}
{% endhighlight %}

설치가 완료되면 Firebase 로그인을 합니다.

{% highlight shell %}
{% raw %}

firebase login

{% endraw %}
{% endhighlight %}

## FlutterFire CLI 설치

VSCode에서 터미널을 열고 FlutterFire CLI를 설치합니다.

{% highlight shell %}
{% raw %}

dart pub global activate flutterfire_cli

{% endraw %}
{% endhighlight %}

Firebase 프로젝트와 Flutter 프로젝트를 연결하도록 구성합니다.

{% highlight shell %}
{% raw %}

flutterfire configure

{% endraw %}
{% endhighlight %}

## Firebase Core 설치

Flutter 디렉토리에서 Firebase Core를 추가합니다.

{% highlight shell %}
{% raw %}

flutter pub add firebase_core

{% endraw %}
{% endhighlight %}

`lib/main.dart` 파일에서 Firebase_core 구성 파일을 import 합니다.

{% highlight dart %}
{% raw %}

import 'package:firebase_core/firebase_core.dart';
import 'firebase_options.dart';

{% endraw %}
{% endhighlight %}

DefaultFirebaseOptions 객체로 Firebase를 초기화합니다.

{% highlight dart %}
{% raw %}

await Firebase.initializeApp(
  options: DefaultFirebaseOptions.currentPlatform,
);

{% endraw %}
{% endhighlight %}

## Firebase Analytics 설치

Firebase Analytics 플러그인을 추가합니다.

{% highlight dart %}
{% raw %}

flutter pub add firebase_analytics

{% endraw %}
{% endhighlight %}

`lib/main.dart` 파일에서 Firebase Analytics 플러그인을 import 합니다.

{% highlight dart %}
{% raw %}

import 'package:firebase_analytics/firebase_analytics.dart';

{% endraw %}
{% endhighlight %}

Firebase Analytics 인스턴스를 추가합니다.

{% highlight dart %}
{% raw %}

static FirebaseAnalytics analytics = FirebaseAnalytics.instance;

{% endraw %}
{% endhighlight %}