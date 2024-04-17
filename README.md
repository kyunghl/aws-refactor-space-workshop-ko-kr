# <p align="center">AWS 마이그레이션 허브 리팩터 스페이스</p>
[[`AWS Migration Hub Refactor Spaces`]](https://aws.amazon.com/ko/migration-hub/features/)는 프로덕션에서 운영하는 동안 리팩터링 프로세스를 쉽게 관리할 수 있게 해주는 점진적 앱 리팩터링을 위한 새로운 시작점입니다. 고객은 Refactor Spaces를 사용하여 리팩터링을 할 수 있는 기본 인프라의 생성 및 관리가 아닌 애플리케이션의 리팩터링에 집중할 수 있습니다. 이 신규 Migration Hub 기능은 애플리케이션을 마이크로서비스로 발전시키거나 마이크로서비스로 작성된 신규 기능으로 기존 애플리케이션을 확장하는 데 따른 비즈니스 리스크를 줄여줍니다. Refactor Spaces는 여러 계정에 걸친 AWS 서비스를 오케스트레이션하여 고객이 가치를 조기에 실현하도록 도움을 주는 애플리케이션을 점진적으로 발전시키기 위한 리팩터링 환경을 생성합니다.

Migration Hub Refactor Spaces는 다음에 의해 애플리케이션 리팩터링을 간소화합니다.

* 리팩터링 환경을 설정하는 시간 단축 
* 새로운 마이크로서비스로 기능을 반복적으로 추출하고 및 트래픽을 이전에서 새것으로 재라우팅(Strangler Fig Pattern)하기 위한 복잡성 감소
* 유연한 라우팅 제어, 격리, 중앙 집중화 관리를 통해 단일 애플리케이션으로 기존 앱과 마이크로서비스의 관리 간소화
* 앱이 변경되는 동안 개발, 관리, 운영을 간소화함으로써 데브 팀의 기술 및 배포 독립의 달성 및 가속화를 지원

---

이 워크숍은 `AWS Migration Hub Refactor Space`를 통해 모놀리식 아키텍처에서 마이크로서비스 아키텍처로 이동하는 과정을 안내합니다.

`Unishop`이라는 기존 모놀리식 애플리케이션을 살펴보고 해당 장바구니 기능을 별도의 마이크로서비스로 배포합니다. `AWS Migration Hub Refactor Spaces`를 사용하여 이러한 증분 전환을 단순화합니다.

아래 사항을 진행자와 함께 수행하면 됩니다. 간단한 소개로부터 시작하겠습니다.

---

## 워크샵 소개

[//]: # ([![소개]&#40;docs/images/introduction.png&#41;{: width="100" height="100"}]&#40;docs/introduction.md "소개"&#41;)

[//]: # (<br></br>)

<a href="docs/introduction.md" title="소개">
    <img src="docs/images/introduction.png" alt="소개" width="300" />
</a>
