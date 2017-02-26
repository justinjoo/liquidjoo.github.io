---
title: javascript basic 3
layout: post
permalink: /javascript/
theme: sky

slides:
 - title: JavaScript Regular Expression
   slide-data: 정규표현식(regular expression)은 문자열에서 특정한 문자를 찾아내는 도구이다. 정규표현식은 두가지 단계로 이루어진다. 하나는 컴파일(compile) 다른 하나는 실행(execution)이다. 컴파일은 검출하고자 하는 패턴을 만드는 일이다. 우선 정규표현식 객체를 만들어야 한다. 객체를 만드는 방법은 두가지가 있다. 하나는 var pattern = /a/; 슬래쉬를 이용한 방법과 다른 하나는 var pattern = new RegExp('a'); 객체를 이용한 방법이다.


 - title: JavaScript String like Regular Expression (String.match(), String.replace)
   slide-data: String.match() 함수는 RegExp.exec()와 비슷하다. 'apple'.match(pattern); 으로 쓰이고 String.replace()는 문자열에서 패턴을 검색해서 이를 변경한 후에 변경된 값을 리턴한다. 'apple'.replace(pattern, 'A'); => Apple


 - title: JavaScript Regular Expression Pattern
   slide-data: 괄호안의 패턴은 마치 변수처럼 재사용할 수 있다. 이 때 기호 $를 사용하는데 아래 코드는 coding과 everybody의 순서를 역전시킨다.<br>var pattern = /(\w+)\s(\w+)/;</br><br>var str = "coding everybody";</br><br>var result = str.replace(pattern, "$2, $1");</br><br>console.log(result);</br>

---

{% for slide in page.slides %}

<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}"><h1>{{slide.title}}</h1>{{ slide.slide-data }}</section>

{% endfor %}
