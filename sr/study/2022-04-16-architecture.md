# 아키텍처라는 주제

이번 주도 새로운 약을 한번 팔아보려고 합니다.

특정 도서 사이트에서 `소프트웨어 아키텍처`라는 키워드를 입력하여 조회를 하면 많은 책들이 나옵니다. 보통은 `특정 기술`을 소개하면서 이를 잘 활용하기
위해서 `이 기술은 어떠한 매커니즘을 갖고 있으니 이렇게 사용하면 된다.`라는 식의 설명입니다.

특정 기술 기반이 아닌 말 그대로 소프트웨어 아키텍처만을 위한 책은 대학교 교재마냥 관심있는 사람도 관심 뚝 떨어질 것 같은 읽기 싫을 것 같은 표지에 가격이 4만원대나 하는 책들만 있습니다. 다행히 어느 누가
마케팅 했는지, 최근에 밋코더에서도 [만들면서 배우는 클린 아키텍처](https://github.com/Meet-Coder-Study/Get-Your-Hands-Dirty-on-Clean-Architecture)
라는 책으로 스터디를 하신 분도 계시고, 저도 아직 진행중인 [소프트웨어 아키텍처 101](https://github.com/Meet-Coder-Study/book-software-architecture-101)
라는 스터디를 통해 소프트웨어 아키텍처에 대해 학습 중에 있습니다.

아키텍처를 왜 따로 공부해야 할까요?, 회사 또는 개인 프로젝트를 통해 아키텍처를 배울 수 없을까요?

## `주니어`의 시점에서 바라보는 아키텍처

`아키텍처`라는 키워드는 프로젝트의 기저에 깔려있는 `핵심적인 내용`으로 해당 프로젝트의 `전체적인 프로세스 매커니즘`을 정의하는 것이라고 볼 수 있다. 하지만 대부분의 개발자(주니어)는 눈 앞의 `요구사항`
과 `주어진 시간`에만 신경쓰고, 프로젝트를 전체적으로 설계한 근거가 되는 `아키텍처`라는 것에 대해서는 외면하는 것이 현실이다.

연차가 높은 개발자가 설계를 하고, 요구사항을 정의하여 그 밑의 팀원들의 역량에 따라 또는 성장을 위해 업무 분장을 하는 식이라면 아키텍처라는 개념을 접하기 위해서는 연차 높은 개발자의 판단에 따라 수동적으로 익힐
수 있을 것이다. 물론 자신이 언제든지 새로운 것을 받아들일 자세가 되어있고, 새로운 것을 학습하는 데에 거부감이 없다면 말이다.

> 현 상황

요즘 회사는 수직적인 회사보다 수평적인 회사 분위기가 많아, 단방향으로 연차 높은 개발자의 판단에 따라 팀원이 학습하는 것이 아니라 팀원들이 스스로 프로젝트를 위해 필요한 부분을 학습해야 하는 환경이 만들어진다.

## 아키텍처를 학습하다.

현재 프로젝트의 아키텍처에 대해서 알고 있고, 해당 아키텍처가 어떠한 부분에서 특징이 있는지 알기 위해서는 다양한 아키텍처를 접해보고 비교할 수 있는 기준이 무엇인지 알아야 한다.
`소프트웨어 아키텍처 101` 이라는 책은 아키텍처의 역할과 개발자의 역할을 이미 구분하고 있다는 관점에서 시작하게 된다. 하지만 우리는 개발자로서 `아키텍트가 프로젝트를 바라보는 관점`을 학습하여, 개발자의
입장에서 단순하게 눈앞의 요구사항을 개발하는 것이 아니라 `개발자의 입장에서 아키텍트의 판단도 어느정도 가능하다는 관점`으로 학습하도록 한다.

아키텍처의 관점으로 볼 수 있는 역량 또는 판단을 하기 위해서는 `아키텍처의 특성`, `아키텍처 결정`, `설계 원칙`, `시스템의 구조`에 대한 기준을 둘 수 있어야 한다.

> 시스템 구조(structure)

`시스템 구조`란 시스템이 구현된 `아키텍처 스타일의 종류`를 말하는 것이다. 하지만 구조를 아는 것만으로는 아키텍처를 전체적으로 설명하기에 부족하다. 
가령 아키텍처를 설명해달라는 요청에 아키텍트가 "우리 서비스는 마이크로서비스 아키텍처입니다." 라고 대답하는 경우, 아키텍트는 시스템 구조만 언급했을 뿐, 시스템 아키텍처에 대해서 이야기 한 것은 아니다. 
시스템 아키텍처를 이해하기 위해서는 `아키텍처 특성`, `아키텍처 결정`, `설계 원칙`에 대해 알아야 한다.

> 아키텍처 특성(architecture characteristic)

소프트웨어 아키텍처를 다른 관점에서 바라본 것으로 `시스템이 올바르게 동작하기 위해서 반드시 필요한 것`들이다.

- 운영 아키텍처 특성
	- 가용성, 연속성, 성능, 복구성, 신뢰성/안전, 견고성, 확장성
- 구조 아키텍처 특성
	- 설정성, 신장성, 설치성, 활용성/재사용, 지역성, 유지보수성, 이식성, 지원성, 업그레이드성
- 아키텍처 공통 특성
	- 접근성, 보관성, 인증, 인가, 합법성, 프라이버시, 보안, 사용성/성취성

아키텍처 특성은 정해져 있는 것이 아니라 소프트웨어마다 고유한 요소를 바탕으로 중요한 아키텍처 특성이 새롭게 도출될 수 있다. 
국제 표준 기구에서 [기능별 목록](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010) 으로 어느정도 정의를 해두었지만 이는 표준으로 정의할 수 있는 부분만 나열되어 있을 뿐이지 모든 특성에 대해서 나열되어 있지는 않다.

> 아키텍처 결정(architecture decision)

소프트웨어 아키텍처를 규정하는 또 다른 측면인 `아키텍처 결정`은 시스템 구축에 필요한 규칙들을 정한 것이다.
가령, 아키텍트가 `레이어드 아키텍처에서는 프레젠테이션 레이어가 데이터베이스를 직접 호출하지 못하도록 비즈니스와 서비스 레이어에서만 데이터베이스에 액세스 할 수 있다.` 라고 결정하는 식이다.
아키텍처 결정은 시스템의 제약조건을 형성하며, 개발자가 해도 되는 것과 하지 말아야 하는 것을 알려주는 것이다.
아키텍트는 이러한 `아키텍처 결정`의 `컴플라이언스를 보장`하기 위해 `아키텍처 피트니스 함수`(JUnit, ArchUnit..) 같은 시스템을 도입하여 정확한 목적을 개발자에게 이해할 수 있도록 설명한다.

- `아키텍처 피트니스 함수`
	- 어떤 아키텍처 특성의 객관적인 무결성을 평가하는 모든 매커니즘
- `컴플라이언스 보장`
	- 아키텍트가 정의하고 문서화하여 전달한 아키텍처 결정과 설계 원칙들을 개발팀이 제대로 준수하고 있는지 지속적으로 확인하는 것

> 설계 원칙(design principal)

아키텍처를 정의하는 마지막 요소는 설계 원칙이다. 아키텍처 결정이 반드시 시켜야 할 규칙이라면 설계 원칙은 가이드 라인이다.
예를 들어, 마이크로서비스 아키텍처의 성능 향상을 위해서 서비스 간의 통신은 비동기 메시징을 활용해야 한다고 기술하는 것이 설계 원칙이다.
서비스 간의 통신에 관한 모든 조건과 구현 방안을 아키텍처 결정으로 다룰 수는 없기에, 특정 환경에서 개발자가 더 적합한 통신 프로토콜을 선택할 수 있도록, 
우선 권장하는 방법에 대한 가이드를 설계 원칙으로 제공하는 것이다.

## 그래서 아키텍트의 관점이란?

1. 아키텍처와 설계의 차이를 이해하고 아키텍처 작업을 진행하려면 개발팀과 어떻게 협력해야 할지 아는 것이다.
2. 어느 정도 기술 깊이를 유지하면서 폭넓은 기술 지식을 확보하는 것, 그래서 다른 사람들이 보지 못하는 해결책과 가능성을 떠올릴 수 있는 것.
3. 다양한 솔루션과 기술 간의 트레이드 오프를 이해하고 분석하고 조율하는 것.
4. 비즈니스 동인의 중요성을 이해하고 그것을 아키텍처 관심사로 해석할 줄 아는 것.

## 그래서 우리는..

개발할 시간도 부족하고, 개발공부할 시간도 부족하지만, 아키텍트의 관점을 키우기 위해서 새로운 것을 배우거나 특정 주제를 깊이 파고드는 시간을 매일 어느정도는 투자할 수 있어야 한다.

매일 익숙하지 않은 전문 용어를 인터넷 검색을 통해 배우고, 그렇게 습득한 지식을 `모른다는 사실조차 알지 못하는 상황`에서 `모른다는 사실을 알고 있는 수준`으로 격상시킴으로써 어제보다 조금 나은 개발자가 될 수 있지 않을까?


- [참고](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&ejkGb=KOR&barcode=9791162244869&orderClick=JAj)
- [밋코더 - 소프트웨어 아키텍처 101](https://github.com/Meet-Coder-Study/book-software-architecture-101)