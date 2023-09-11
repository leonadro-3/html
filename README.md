# html
html 끝장 내기

# 1.1 html 파일 만들기

> 000.html로 파일 확장자를 바꾸면 바뀐다.

# 1.2 html 기본 구조 만들기

> visual studio code에서 html을 치고 tap을 누르면 빠르게 자동완성이 된다.

https://www.youtube.com/watch?v=TJlt-LiqVCY(vs code 자동완성 커스텀 하기)

# 1.3 html 기본 구조 및 문법

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

1.3.1 특수기호 발음

> <!DOCTYPE html>을 보면 <>로 감싸져 있는 것을 알 수 있다. <>를 한국어로 꺽쇠라고 하는데 영어 강의를 듣다보면 특수기호에 따라서 다르게 발음 한다. 예를들어 - 하이픈이라고 하는 사람도 있지만 대시라고 하는 사람도 있다.
> https://jdm.kr/blog/87에 특수기호 발음을 참고해라.

1.3.1 여는 태그와 닫는 태그

> 시작은 <000>, 끝은 </000>으로 끝난다. 맨 위와 아래를 보면 <html lang="en"> ~ </html> 로 되어 있는 것을 알 수 있다.
> 물론 어떤 태그들은 </>를 작성하지 않아도 된다. <meta charset="UTF-8">

1.3.2 <!DOCTYPE html>은 무엇일까?

웹 브라우저가 html파일을 읽는데 필요한 선언이다. 과거의 html 버전에 따라서 선언하는 방식이 달랐으며 만약 선언을 하지 않았을 때 어떤 일들이 벌어지는지 알아보자.

```
https://www.w3.org/wiki/Choosing_the_right_doctype_for_your_HTML_documents
https://www.shecodes.io/athena/35857-what-happens-when-there-is-no-doctype-in-a-webpage-in-html
https://aboooks.tistory.com/169
https://github.com/whatwg/html
https://html.spec.whatwg.org/multipage/introduction.html#abstract
https://www.w3.org/QA/2002/04/valid-dtd-list.html
https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode
```

> 요약을 하면 웹 브라우저는 html이 어떤 버전인지 모르기 때문에 랜더링을 할 때 quirks mode로 실행한다. 실재로 기존에 있는 아무 웹 페이지의 html 태그를 제거하고 비교하기 위해서 2가지 (원본, html 태그 제거)를 실행하면 <!DOCTYPE html>이 없는 상태에서 없던 html 태그가 자동으로 생성되며 열린다. 즉, 웹 브라우저는 없는 html 태그가 없어도 열기 위해서 태그를 스스로 생성한다.

> 이러한 현상은 과거 W3C 표준이 없던 시기에 만들어진 웹사이트들 까지 호환하기 위한 목적으로 이뤄진다. 즉, 크로스 브라우징과 연결된다. 여러가지 버전의 html들이 있고 웹 브라우저마다 지원하는 태그나 기능이 다르기 때문에 크로스 브라우징이 필요하다. 이것은 개발이나 유지 보수시 고려되는 점이며 최신의 웹 사이트를 만드는 방식은 점점 조금씩 계속해서 변화하고 있다는 점을 의미한다. 

> 다르게 말해 개발공부를 해서 HTML를 배웠다고 생각하지만 시간이 지나면 새로운 것들이 생기며 개발 프로세스 또한 약간씩 변화한다는 것이다. 과거의 웹 공부와 지금의 웹 공부의 주제는 크게 다르지 않지만 주요 문제를 해결하는데 접근하는 방법이 달라질 수 있다는 점이다. 똑같이 개발을 해도 누군가는 더 빠르고 쉽게 개발을 하며 누군가는 옛날 방식대로 만들어서 굉장히 느리게 만들 수 있다. 물론 결국은 만들어 낸다는 점에서 큰 차이가 없겠지만 대부분이 동의하는 사실은 "처음에 의도적으로 힘들게 만들어봐야 나중에 쉽게 만드는 법을 배웠을 때 더 잘하게 된다."는 것이다. 이러한 것들이 실재 개발을 공부할 때 시간을 단축시키는 가장 중요한 것이 된다. 물론 겪어 봐야 아는 것이 있으며 절대적인 노력의 시간. 즉, 많은 고민 없이 만들어진 결과물은 쉽게 무너진다는 것이다.

1.3.3 <html lang="en">은 무엇일까?

```
<html lang="en">
</html>
```

> html의 태그가 있고 lang="en"이 있다. lang은 약어로 language를 의미하며 en은 english를 의미한다. html의 문서가 주로 어느 국가의 언어로 작성되어 있는지를 표현하는 것이다. lang과 같은 것들을 속성(Attributes)라고 하는데 나중에 자세히 다루겠다.
> en이라고 해서 한글을 무조건 쓰지 않아야 되는 것은 아니다. 다만 웹 사이트 개발시 해당 사이트에 표현되는 언어를 선택하는 것은 웹 사이트 설계시 매우 기초적인 분기점이 된다. 유튜브 영상을 영어 콘텐츠로 만드는 것과 한국어 콘텐츠로 만드는 것과 노출수 자체가 다르기 때문에
> 글로벌 서비스를 목적으로 한다면 여러가지 언어를 기반으로 만든 웹 사이트를 만드는 것이 가장 이상적이겠지만 그만큼 관리하는 사람도 필요하다.

> 예시
```
lang="en-US"
style="font-size: 10px;font-family: Roboto, Arial, sans-serif;"
system-icons
typography
typography-spacing
darker-dark-theme
class="translated-ltr"
```

1.3.4 <head>는 무엇일까?

```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```
> head 태그를 설명하기전에 알아야 하는 것이 있다. 바로 html 태그는 최상위 태그라고 하며 루트라고도 한다. 이것을 이해하기 위해서 트리 구조라는 것을 알아야 하는데 자료구조라는 CS 지식이 바탕이 되어야 한다. https://yoongrammer.tistory.com/68
> 쉽게 비유하면 크리스마스 트리처럼 맨 위는 별 하나가 있고 그 아래로 나눠지면서 여러가지 장식들을 배치한다. 물론 더 자세히 알아보고 싶다면 위 링크를 타고 들어가면 된다.
> head 태그는 메타 데이터를 작성한다고 되어 있다. 재밌는 것은 <head>의 주 목적은 기계 처리를 위한 정보이고, 사람이 읽을 수 있는 정보가 아닙니다. 최상위 제목, 작성자 목록 등 사람에게 보여야 할 정보는 <header> 요소를 사용하세요. 라고 되어 있는데
> title 태그는 웹 페이지의 탭에 있는 html 탭의 이름을 말하는 것이며 mdn 문서에는 없지만 favicon 이나 링크 북마크의 미리보기와 같은 것들을 보여주는 역할을 한다. 맨 초기에는 큰 생각을 하지 않는데 나중에 이 페이지의 링크를 타고 사용하는 사람들이 있기 때문에
> 단순히 링크 주소뿐만 아니라 미리보기가 보여지는 점에서 고려해야할 요소이다.

