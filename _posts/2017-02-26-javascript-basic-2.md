---
title: javascript basic 2
layout: post
permalink: /javascript/
theme: sky

slides:
 - title: JavaScript Object
   slide-data: 데이터가 추가되면 배열 전체에서 중복되지 않는 인덱스가 자동으로 만들어져서 추가된 데이터에 대한 식별자가 된다. 이 인덱스를 이용해서 데이터를 가져오게 되는 것이다. 만약 인덱스로 문자를 사용하고 싶다면 객체(dictionary)를 사용해야 한다. 다른 언어에서는 연관배열(associative array) 또는 맵( map), 딕셔너리(Dictionary)라는 데이터 타입이 객체에 해당한다. Hash Map도 비슷한 원리 이다.


 - title: JavaScript Object Create
   slide-data: var object = {}; or var object = new Object();


 - title: JavaScript Object Data
   slide-data: for(key in object) 에서 value는 object[key]로 데이터를 추출 할 수가 있다.

 - title: JavaScript Module
   slide-data: 프로그램은 작고 단순한 것에서 크고 복잡한 것으로 진화한다. 그 과정에서 코드의 재활용성을 높이고, 유지보수를 쉽게 할 수 있는 다양한 기법들이 사용된다. 그 중의 하나가 코드를 여러개의 파일로 분리하는 것이다.  - 자주 사용되는 코드를 별도의 파일로 만들어서 필요할 때마다 재활용할 수 있다.  - 코드를 개선하면 이를 사용하고 있는 모든 애플리케이션의 동작이 개선된다.  - 코드 수정 시에 필요한 로직을 빠르게 찾을 수 있다.  - 필요한 로직만을 로드해서 메모리의 낭비를 줄일 수 있다.

 - title: JavaScript Library
   slide-data: 라이브러리는 모듈과 비슷한 개념이다. 모듈이 프로그램을 구성하는 작은 부품으로서의 로직을 의미한다면 라이브러리는 자주 사용되는 로직을 재사용하기 편리하도록 잘 정리한 일련의 코드들의 집합을 의미.

---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
