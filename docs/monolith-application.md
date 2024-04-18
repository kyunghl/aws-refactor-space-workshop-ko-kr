# <p align="center">`모놀리스 (Monolith)` 애플리케이션</p>

이 모듈에서는 `Unishop` 레거시 애플리케이션을 알아보도록 하겠습니다.

![](images/asis-architecture.png)

해당 애플리케이션은 `Spring Boot` 부트스트랩을 사용하는 `Java` 애플리케이션입니다. 이 백엔드 애플리케이션은 `MySQL` 데이터베이스에 연결된 단일 `EC2 인스턴스`에 배포됩니다. 프론트엔드 웹사이트는 `Amazon S3 정적 웹 호스팅`을 사용하여 호스팅됩니다.

`CloudFormation`을 사용하여 `레거시 모놀리스` 자원을 배포하도록 하겠습니다.

---

## 1. `모놀리스 애플리케이션` 자원 배포

`AWS Cloud9` 환경에서 `CloudFormation`을 사용하여 `모놀리스 애플리케이션` 자원을 배포합니다.

```bash

```
