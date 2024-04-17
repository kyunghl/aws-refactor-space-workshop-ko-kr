# <p align="center">AWS 마이그레이션 허브 리팩터 스페이스 워크샵 소개</p>

![](images/unishop_front.en.png)

## 배경

`Unishop`은 필요한 유니콘을 입양할 수 있는 원스톱 쇼핑몰입니다. `Unishop`에서는 가장 다양한 유니콘을 찾아보고, 24시간 이내에 유니콘을 전달받을 수 있습니다! 그러나 현재의 `모노리식` 아키텍처는 비즈니스 확장에 따른 성장을 어렵게 만듭니다. CTO는 `Strangler Fig 패턴`을 사용하여 `Unishop`을 마이크로서비스 아키텍처로 이전하는 것을 탐색하고 싶어합니다.

## `AWS Migration Hub Refactor Space`

우리는 `AWS Migration Hub Refactor Space`를 사용하여 마이크로서비스 기반 아키텍처로의 점진적인 전환을 단순화하고 가속화할 것입니다. `Refactor Space`를 사용하면, 리팩토링에 필요한 기본 인프라의 생성 및 관리가 아닌 애플리케이션의 리팩토링에 집중할 수 있습니다.

이 워크숍은 단일 계정에서 진행되지만, `Refactor Space`는 다중 계정 환경에서 리팩토링을 점진적으로 단순화하는 과정도 지원합니다. 여러 AWS 계정을 사용하는 것은 `비용 가시성`, `보안 격리`, `팀 자율성`을 가능하게 하는 모범 사례입니다. `Refactor Space`는 두 가지 주요 리소스를 통해 다중 계정 리팩토링을 단순화합니다:

* `Refactor Spaces 환경 (Environment)` — `Refactor Spaces 환경`은 다른 `Refactor Space` 리소스의 논리적 구분 단위이며, 점진적으로 현대화하는 데 필요한 인프라, 다중 계정 네트워킹, 라우팅을 제공합니다. `환경`은 선택적으로 `Transit Gateway`와 `VPC`를 조정하여 AWS 계정 간의 네트워킹을 연결하고, 레거시 서비스와 새로운 서비스가 직접 통신할 수 있게 합니다.
* `Refactor Spaces 애플리케이션 (Application)` — `애플리케이션`은 `API Gateway`, `VPC Link`, `리소스 정책`을 배포하고 관리하여 새로운 서비스로 트래픽을 투명하고 점진적으로 라우팅할 수 있게 합니다. 이는 기본 아키텍처 변경을 애플리케이션 사용자에게 투명하게 유지합니다.
