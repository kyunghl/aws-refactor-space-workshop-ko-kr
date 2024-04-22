# <p align="center">통합 작업 환경 준비 (AWS Cloud9)</p>


## 1. Cloud9 통합 환경 (IDE) 생성

### 1.1. AWS Cloud9 환경 생성 (AWS CLI 사용)
진행자가 제공한 AWS 관리 콘솔에서 ```CloudShell```을 실행한 후 아래 명령을 수행하여 ```Cloud9``` 환경을 생성해 줍니다.<br>
```CloudShell```도 다수의 개발 언어와 런타임, 그리고 클라우드 환경을 다룰 수 있는 CLI를 기본적으로 제공하지만 보다 풍부한 통합 개발 환경을 제공하는 ```Cloud9```을 사용하기로 합니다.<br>
아래 명령은 ```Cloud9``` 환경을 구성하기 위하여 일련의 작업을 수행하므로 완료될 때까 다소 시간이 걸립니다 (1 ~ 2분)
```bash
curl -fsSL https://raw.githubusercontent.com/shkim4u/m2m-travelbuddy/main/cloud9/bootstrap-v2-with-admin-user-trust.sh | bash -s -- c5.4xlarge
```

## 2. Cloud9 통합 환경 (IDE) 설정
```Cloud9``` 통합 환경에 접속하여 필요한 사항을 사전에 구성한 쉘 스크립트 파일을 아래와 같이 실행합니다.

여기에는 다음 사항이 포함됩니다.

1. IDE IAM 설정 확인
2. 쿠버네테스 (Amazon EKS) 작업을 위한 Tooling
    * kubectl 설치
    * eksctl 설치
    * k9s 설치
    * Helm 설치
3. AWS CLI 업데이트
4. AWS CDK 업그레이드
5. 기타 도구 설치 및 구성
    * AWS SSM 세션 매니저 플러그인 설치
    * AWS Cloud9 CLI 설치
    * jq 설치하기
    * yq 설치하기
    * bash-completion 설치하기
6. Cloud9 추가 설정하기
7. 디스크 증설
8. (Optional) CUDA Deep Neural Network (cuDNN) 라이브러리
9. Terraform 설치
10. ArgoCD 설치
11. Python 3.11 설치

```bash
cd ~/environment/

# Cloud9 환경 설정
curl -fsSL https://raw.githubusercontent.com/shkim4u/m2m-travelbuddy/main/cloud9/cloud9.sh | bash

# Amazon Corretto Headless 17 설치
sudo yum install -y java-17-amazon-corretto-headless

# Docker 빌드를 위한 Docker Compose 설치
sudo curl -L "https://github.com/docker/compose/releases/download/v2.25.0/docker-compose-linux-x86_64" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

# JWT CLI 설치
npm install -g jwt-cli
```

## 3. 워크샵 소스 받기
이제부터 모든 작업은 `Cloud9` 상에서 이루어지며, 먼저 워크샵 소스를 아래와 같이 다운로드합니다.<br>
```bash
cd ~/environment/
git clone https://github.com/shkim4u/aws-refactor-space-workshop-ko-kr.git refactor-workshop
cd refactor-workshop
```

해당 소스 코드에는 `CloudFormation`으로 작성된 `IaC` 코드도 포함되어 있으며 여기에는 ```레거시 모놀리스 애플리케이션 자원```, ```AWS Refactor Space 자원```, ```리팩터링을 위한 마이크로서비스 (람다)``` 등의 자원이 포함되어 있습니다.<br>

이후 과정에서 이러한 자원들을 배포하고, 리팩터링을 진행하게 됩니다.
