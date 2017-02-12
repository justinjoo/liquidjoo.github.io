---
title: php basic
layout: post
permalink: /white/
theme: white

slides:
 - title: 클래스 자동 로딩딩 __autoload()
   slide-data: 클래스 하나당 하나의 php 소스파일을 만들어 클래스를 정의하지만 스크립트마다 매번 클래스를
   include 하는 것은 성가신 일!
   php5 에서는 __autoload() 함수를 정의하면 사용하려는 클래스나 인터페이스가 아직 정의 되지 않았을 경우
   자동으로 호출 합니다.

 - title: 생성자 __construct()
   slide-data: PHP 5 에서는 클래스의 생성자 메서드를 선언하는것을 허용.
   클래스는 새로이 생성된 오브젝트마다 자신의 생성자 메서드를 호출합니다.
   주로 객체 초기화를 위해 사용 합니다.

 - title: 소멸자 __destruct ( void )
   slide-data: 소멸자 메서드는 더이상 객체를 참조하지 않거나, 종료가 일어나는동안 호출될수 있을 것입니다. 생성자처럼, 부모 소멸자는 묵시적으로 호출되지 않습니다. 부모 소멸자를 호출하기 위해서는, 소멸자 내부에서 parent::__destruct() 를 명시적으로 호출해 줘야 합니다. 또한 생성자처럼, 자식 클래스가 소멸자를 가지지 않는다면 부모의 것을 상속합니다.

 - title: 스코프 해결 연산자 (::)
   slide-data: 스코프 해결 연산자, 더블콜론은 static이나 constant와,
   클래스의 재정의된 프로퍼티나 메서드에 접근할수 있도록 해주는 토큰입니다.

 - title: static 키워드
   slide-data: 클래스의 메서드와 프로퍼티를 static으로 선언한다는 것은 해당 클래스의 인스턴스화가
   필요없이 해당 프로퍼티와 메서드에 접근가능 하게함을 의미합니다. static 키워드로 선언된 프로퍼티는
   인스턴스화된 클래스의 객체로 접근할 수 없습니다.(하지만 static 메서드는 가능합니다.)
   static 메서드가 인스턴스객체의 필요없이 호출이 가능한 이유로, 의사변수 $this 는 static으로 선언된 메서드안에는 존재하지 않습니다.
   정적 프로퍼티는 객체의 -> 연산자를 통한 접근을 할수 없습니다.
   스코프 해결 연산자로 해결!


---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
