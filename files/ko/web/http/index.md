---
title: HTTP
slug: Web/HTTP
tags:
  - CORS
  - HTTP
  - Reference
  - TCP/IP
  - Web
  - l10n:priority
translation_of: Web/HTTP
---
{{HTTPSidebar}}

**_하이퍼텍스트 전송 프로토콜(HTTP)_**_은 HTML과 같은 하이퍼미디어 문서를 전송하기위한 _[애플리케이션 레이어](https://en.wikipedia.org/wiki/Application_Layer) 프로토콜입니다. 웹 브라우저와 웹 서버간의 커뮤니케이션을위해 디자인되었지만, 다른 목적으로도 사용될 수 있습니다. HTTP는 클라이언트가 요청을 생성하기 위한 연결을 연다음 응답을 받을때 까지 대기하는 전통적인 [클라이언트-서버 모델](https://en.wikipedia.org/wiki/Client%E2%80%93server_model)을 따릅니다. HTTP는 [무상태 프로토콜](https://en.wikipedia.org/wiki/Stateless_protocol)이며, 이는 서버가 두 요청간에 어떠한 데이터(상태)도 유지하지 않음을 의미합니다.

## 자습서

가이드와 튜토리얼을 통해 HTTP를 사용하는 방법을 배워보세요.

- [HTTP 개요](/ko/docs/Web/HTTP/Overview)
  - : 클라이언트-서버 프로토콜의 기본 기능들. 할 수 있는 것과 의도된 용도.
- [HTTP 캐시](/ko/docs/Web/HTTP/Caching)
  - : 캐싱은 빠른 웹 사이트를 위해 아주 중요합니다. 이 글은 여러 캐싱 방법과 HTTP 헤더를 사용하여 이를 제어하는 방법을 설명합니다.
- [HTTP 쿠키](/ko/docs/Web/HTTP/Cookies)
  - : 쿠키가 동작하는 방식은 [RFC 6265](https://tools.ietf.org/html/rfc6265)에서 정의합니다. HTTP 요청을 제공할 때, 서버는 응답과 함께 `Set-Cookie` HTTP 헤더를 전송합니다. 그 다음에 클라이언트는 모든 요청과 함께 쿠키의 값을 `Cookie` 요청 헤더의 형태로 동일한 서버에 반환합니다. 쿠키는 특정 날짜에 만료되도록 설정하거나 특정 도메인 및 경로에 제한되도록 설정할수도 있습니다.
- [교차 출처 리소스 공유(CORS)](/ko/docs/Web/HTTP/CORS)
  - : **교차 사이트 HTTP 요청**은 요청을 생성한 리소스의 도메인과 **다른 도메인**의 리소스에 대한 HTTP 요청입니다. 예를 들면, 도메인 A(`http://domaina.example/`)의 HTML 페이지가 `img` 엘리먼트를 통해 도메인 B(`http://domainb.foo/image.jpg`)의 이미지에대한 요청을 생성하는 것입니다. 오늘날의 웹 페이지가 CSS 스타일시트, 이미지, 스크립트 등을 포함하는 교차-사이트 리소스을 로드하는 것을 아주 흔하게 볼 수 있습니다. CORS를 통해 웹 개발자는 그들의 사이트가 교차-사이트 요청에 대해 어떻게 반응할지 제어할 수 있습니다.

<!---->

- [클라이언트 힌트](/ko/docs/Web/HTTP/Client_hints)
  - : **클라이언트 힌트**는 서버가 클라이언트로부터 디바이스, 네트워크, 사용자 및 사용자 에이전트별 기본 설정에 대한 정보를 사전에 요청하기 위해 사용할 수 있는 응답 헤더의 집합입니다. 이에 따라 서버는 클라이언트가 제공하는 정보에 기반하여 전송할 리소스를 결정할 수 있습니다.
- [HTTP의 진화](/ko/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)
  - : 초기 버전의 HTTP와 현대의 HTTP/2 및 새로 등장한 HTTP/3 이후 버전 간의 변경 사항에 대한 간략한 설명입니다.
- [Mozilla 웹 보안 가이드라인](https://wiki.mozilla.org/Security/Guidelines/Web_Security)
  - : 안전한 웹 어플리케이션을 생성하는 운영 팀에 도움이되는 팁 모음입니다.

<!---->

- [HTTP 메시지](/ko/docs/Web/HTTP/Messages)
  - : HTTP/1.x와 HTTP/2의 다양한 종류의 메시지 타입과 구조에 대해 설명합니다.
- [전형적인 HTTP 세션](/ko/docs/Web/HTTP/Session)
  - : 일반적인 HTTP 세션의 흐름을 보여주고 설명합니다.
- [HTTP/1.x의 연결 관리](/ko/docs/Web/HTTP/Connection_management_in_HTTP_1.x)
  - : HTTP/1.x에서 사용가능한 세 가지 연결 관리 모델과 그 장단점을 설명합니다.

## 참고서

상세한 HTTP 참고서를 살펴보세요.

- [HTTP 헤더](/ko/docs/Web/HTTP/Headers)
  - : HTTP 메시지 헤더는 리소스 또는 서버나 클라이언트의 동작을 설명하는데 사용됩니다. 커스텀 등록 헤더는 `X-`를 앞에 붙여 추가할 수 있습니다. 그 외에는 원본 컨텐츠가 [RFC 4229](https://tools.ietf.org/html/rfc4229)에서 정의된 [IANA 레지스트리](https://www.iana.org/assignments/message-headers/message-headers.xhtml#perm-headers)에 있습니다.
- [HTTP 요청 메서드](/ko/docs/Web/HTTP/Methods)
  - : HTTP로 수행할 수 있는 여러 작업. {{HTTPMethod("GET")}}, {{HTTPMethod("POST")}} 요청 및 덜 자주 사용되는 {{HTTPMethod("OPTIONS")}}, {{HTTPMethod("DELETE")}}, {{HTTPMethod("TRACE")}} 요청.
- [HTTP 상태 응답 코드](/ko/docs/Web/HTTP/Status)
  - : HTTP 응답 코드는 지정한 HTTP 요청이 성공적으로 완료되었는지를 나타냅니다. 응답은 다섯 가지 클래스로 그룹핑됩니다. 정보성 응답, 성공 응답, 리다이렉트, 클라이언트 에러, 서버 에러.
- [CSP 지시문](/ko/docs/Web/HTTP/Headers/Content-Security-Policy)
  - : {{HTTPHeader("Content-Security-Policy")}} 응답 헤더 필드는 주어진 페이지를 로드하기 위해 유저 에이전트가 허용한 리소스를 웹 사이트 관리자가 제어할 수 있도록 해줍니다. 몇 가지 예외를 제외하고, 대부분의 정책은 서버 오리진과 스크립트 엔드포인트 지정을 포함합니다.

## 도구 & 리소스

HTTP를 이해하고 디버깅하는데 도움이되는 도구와 리소스.

- [Firefox 개발자 도구](/ko/docs/Tools)
  - : [네트워크 모니터](/ko/docs/Tools/Network_Monitor)
- [Mozilla Observatory](https://observatory.mozilla.org/)
  - : 개발자, 시스템 관리자, 보안 전문가가 사이트를 안전하게 구성하는 것을 돕기위해 디자인된 프로젝트.
- [RedBot](https://redbot.org/)
  - : 캐시 관련 헤더를 확인하는 도구
- [브라우저가 동작하는 방식](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
  - : 브라우저 내부와 HTTP 프로토콜을 통한 요청 흐름에 대한 아주 이해하기 쉬운 문서. 웹 개발자라면 필독.
