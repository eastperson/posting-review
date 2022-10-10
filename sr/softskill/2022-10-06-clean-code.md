# 클린코드는 존재하지 않는다.

tag: #블로그포스팅-9기 #백엔드 #소프트스킬

## Intro

요즘은 모두가 CleanCode를 위해 다양한 노력을 하고 있고(사실 모두가 하는지는 알 수 없다.), 엔지니어링 팀은 함께 모여 클린 코드를 위해 어떤 방법이 나은지에 대해서 고민하고, 논의한다.

하지만 "CleanCode란 존재하지 않는다."라는 것을 깨달았다.

"클린"이란 유용한 것에 대한 지표가 되는 의미가 아니다. "클린(Clean)"이라는 의미가 코드에 대한 어떠한 구체적인 내용이 없다면, 말 그대로 clean한 코드를 만들 수 없다.

모두가 CleanCode에 대해서 이야기 하고, 나 또한 이 용어를 사용해왔다. 마케팅 용어 또는 비전이나 정신에 대한 설명으로, "클린 코드"는 훌륭하지만, 기술적인 용어로 사용하기에는 몇 가지 문제가 있다.

## Reference

- [There's No Such Thing as Clean Code](https://www.steveonstuff.com/2022/01/27/no-such-thing-as-clean-code)

## Clean code is good code, right?

대개 사람들이 코드가 깨끗하다고 표현할 때, 그 코드는 어떤 식으로든 좋다는 것을 의미한다.

문제는 코드가 좋다는 의미가 명확하지 않고 다양한 이유로 좋을 수 있다.

- 읽기 쉬운(readable)
- 이해할 수 있는(understandable)
- 단순한(simple)
- 성능이 뛰어난(performance)
- 안전한(safe)
- 우아한(elegant)
- 시험할 수 있는(testable)
- 캡슐화된(encapsulated)
- 확장 가능한(scaleable)
- 유지시킬 수 있는(maintainable)
- 재사용 가능한(reusable)
- 삭제하기 쉬운(easy to delete)
- 깔끔하고 깔끔한(neat and tidy)
- 확장하지 않는(noninvasive)
- 조직적인(systematic)
- 일치하는(consistent)
- 또는 다른 많은 것들(or any number of other things)

위 특성들은 어떤 면에서 서로 상충할 수 있다.
예를 들면, <mark style="background: #BBFABBA6;">간단한 코드(simple)</mark>라고해서 <mark style="background: #BBFABBA6;">테스트하기 쉬운 코드(testable)</mark>라 할 수 없다.
인터페이스와 의존성 주입(DI)으로 구성된 코드가 테스트하기에 좋지만 이는 단순함의 측면에서 비용이 든다.

특성의 일부는 근본적으로 동시에 만족할 수 없는 속성으로 볼 수 있다.
엔지니어링을 한다는 것은, 속성에 대한 장단점을 비교하고, 팀과 상의하여 현 상황에 맞는 속성들에 대해 우선순위를 나열하는 것이다.

## 코드가 좋다고 이야기 한다면, 우리는 그것에 대해 (구체적으로)이야기 해야한다. (If the code is good, we've gotta say why)

누군가가 'Clean'이 해결책이 될 수 있다고 말한다면, 그들은 종종 이유를 설명할 수 없어서 'Clean'이라 표현할 가능성이 높다.
기술적인 해결책에 대해서 건설적인 토론을 하고 싶다면, 왜? 특정 해결책이 다른 해결책보다 어떤 면에서 나은지 서로 명확하게 설명할 수 있어야 한다. 단순하게 각 해결책의 무게를 재는 것처럼 "cleanest"하다는 논쟁은 좋지 않다.
실제로 왜 한 접근 방식이 다른 접근 방식보다 좋거나 나쁜지 표현하는 것은 꽤 어렵지만, 이를 비교해보는 행위 자체가 가치가 있다.

### 어떠한 토론을 하고 싶은가요?

> A: "나는 X라는 해결책이 좋아, 그게 더 클린한 것 같아"

> B: "나는 X 해결책이 좋아. 오류 메시지 프레젠테이션을 코어 로직과 분리할 수 있어. 이렇게 되면 같은 시간에 두 가지 모두 고려할 필요가 없기 때문에 이해하기 더 쉬워. 이렇게 분리하면 한쪽 객체를 테스트하는 동안 다른 객체를 mocking 할 수 있어서 테스트하기에 유용해. 물론 객체가 의존성을 주입하도록 요구하는 비용이 들지만, 그것은 테스트 가능성에 대한 가치 있는 절충안이야."

두 번째 진술은 실제로 우리가 논의하고 있는 해결책의 장단점에 대해 실질적인 것을 전달한다. 'Clean'과 같은 용어는 우리가 아이디어를 명확하게 표현하는 능력을 향상하는 노력을 방해한다.

## 우리는 정확한 용어를 사용해야 한다. (We need to use precise terms)

코딩은 일반적으로 팀 스포츠이다. 스스로 감당하고 있다면 원하는 것을 할 수 있지만, 팀과 함께 일할 때 우리는 우리의 아이디어를 논의해야 한다.
팀 전체가 구체적이고 공통적인 이해를 한 언어를 사용하여 기술적인 해결책에 관해 토론할 수 있다는 것은 서로를 이해하는 데 매우 중요하다.

결국 'Clean Code'는 모든 사람에게 다른 것을 의미한다.

일부 개발자들에게 코드는 잘 <mark style="background: #FFF3A3A6;">정의된 아키텍처</mark>를 가지고 있기 때문에 깨끗(clean)하다. 또 다른 개발자들에게 코드는 <mark style="background: #FFF3A3A6;">단순히 일관된 서식 스타일</mark>을 사용하기 때문에 깨끗하다.

'encapsulated', 'testable', 'mockable', 'reusable'과 같은 단어는 우리가 모두 동의할 수 있는 의미를 가지고 있다. 프로젝트에 영향을 미치는 다양한 코드 특성을 설명하는 더 구체적인 단어를 사용할 때 우리는 모두 같은 페이지에 있다는 것을 확신할 수 있습니다.

'Clean'은 'good'과 같은 수준의 정밀도(precision)를 가지고 있다. 당신은 그것이 깨끗하다고 말할 수 있는 것처럼 코드가 좋다고 말할 수 있지만, 그것이 당신이 더 구체적인 근거로 그것을 정당화하는 것을 대신해주지 않는다.

## So what is clean code? (그래서 clean code가 뭐야?)

나는 종종 코드를 'clean'하다고 표현할 때 그것이 좋다고 생각하지만 왜 그런지 완전히 확신할 수 없다는 결론에 도달했다. 그건 그냥 올바른 해결책처럼 느껴진다.

또는 때때로 우리는 코드가 왜 좋은지 알지만, 그것을 명확하게 표현할 단어를 찾을 수 없으며, 대체로 블로그 게시물의 결론은 "보십시오! 그게 얼마나 깨끗한지 봐!"라는 식이다.

그 직감(intuition)을 쌓는 것은 좋지만, 우리는 거기서 멈출 수 없다. 우리는 왜 코드가 좋다고 생각하는지 이해하고 명확하게 표현하기 위해 그 감정(feelings)을 넘어 더 깊이 파고들 필요가 있다.

> 이 코드는 다른 해결책이 없는 어떤 특성을 가지고 있나요?
> 그것이 우리 프로젝트에 가장 적합한 특성인가요?

아마도 이런 식의 토론은 결국 올바른 해결책이 아닐 것이다.

깨끗한 코드가 필요하지 않으며 "____" 코드가 필요하다는 것을 확신할 수 있기를 바란다.
그 빈칸을 당신의 프로젝트에 필요한 것을 설명하는 단어로 채우는 것은 당신에게 달려 있습니다.