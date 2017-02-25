---
title: javascript basic 1
layout: post
permalink: /javascript/
theme: sky

slides:
 - title: JavaScript var
   slide-data: JavaScript에서 변수는 var로 시작한다. var은 변수를 선언하겠다는 것을 의미한다. var을 생략 할수도 있지만 이것은 유효범위라는 것에 영향을 미친다. 그렇기 때문에 var의 의미를 명확하게 이해하기 전까지는 var를 사용하는 것이 권장된다. 유효범위에 대해서는 뒤에서 살펴볼 것이다. 변수의 이름은 $, _, 혹은 특수 문자를 제외한 모든 문자로 시작할 수 있다. 다음 예제는 변수에 값을 대입한 예제다.


 - title: JavaScript array
   slide-data: 그렇다면 여러 개의 데이터를 하나의 변수에 담아서 관리할 수 있는 방법은 없을까? 있다. 배열을 쓰면 된다. 변수 member에 회원정보를 담아보자. 대괄호([])는 배열을 만드는 기호다. 대괄호 안에 데이터를 콤마(,)로 구분해서 나열하면 배열이 된다.


 - title: JavaScript array push
   slide-data: push는 인자로 전달된 값을 배열(li)에 추가하는 명령

 - title: JavaScript array unshift
   slide-data: unshift는 인자로 전달한 값을 배열의 첫번째 원소로 추가하고 배열의 기존 값들의 색인을 1씩 증가시킨다.

 - title: JavaScript array splice
   slide-data: splice는 첫번째 인자에 해당하는 원소부터 두번째 인자에 해당하는 원소의 숫자만큼의 값을 배열로부터 제거한 후에 리턴한다. 그리고 세번째 인자부터 전달된 인자들을 첫번째 인자의 원소 뒤에 추가한다. ex.splice(3, 1, 'T'); 제거 하고 싶지 않을 땐 두번째 인자 값을 0

 - title: JavaScript array shift
   slide-data: shift는 첫번째 원소를 제거 하는 방법이다.

 - title: JavaScript array pop
   slide-data: pop은 배열 끝의 원소를 제거 하는 방법이다.
---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
