---
aliases:
- /ko/integrations/awspolly/
categories:
- cloud
- aws
- log collection
dependencies: []
description: Amazon Polly의 핵심 메트릭 추적하기.
doc_link: https://docs.datadoghq.com/integrations/amazon_polly/
draft: false
git_integration_title: amazon_polly
has_logo: true
integration_id: ''
integration_title: Amazon Polly
integration_version: ''
is_public: true
kind: 통합
manifest_version: '1.0'
name: amazon_polly
public_title: Datadog-Amazon Polly 통합
short_description: Amazon Polly의 핵심 메트릭 추적하기.
version: '1.0'
---

<!--  SOURCED FROM https://github.com/DataDog/dogweb -->
## 개요

Amazon Polly는 텍스트를 자연스러운 음성 발화로 변환하는 서비스입니다.

이 통합을 활성화하면 Datadog에서 Polly 메트릭을 모두 확인할 수 있습니다.

## 설정

### 설치

아직 설치하지 않았다면 [먼저 Amazon Web Services 통합][1]을 설치하세요.

### 메트릭 수집

1. [AWS 통합 페이지][2]에서 `Metric Collection` 탭 하단에 `Polly`가 활성화되어 있는지 확인합니다.
2. [Datadog - Amazon Polly 통합][3]을 설치하세요.

### 로그 수집

#### 로깅 활성화

S3 버킷이나 CloudWatch로 로그를 전송하도록 Amazon Polly를 구성하세요.

**참고**: S3 버킷에 로깅하는 경우 `amazon_polly`가 _Target prefix_로 지정되어야 합니다.

#### Datadog에 로그 전송

1. 이미 하지 않은 경우 [Datadog 포워더 람다 함수][4]를 설정하세요.
2. Lambda 함수를 설치한 후 AWS 콘솔에서 Amazon Polly 로그를 포함하는 S3 버킷이나 CloudWatch 로그 그룹에 수동으로 트리거를 추가하세요.

    - [S3 버킷에 수동으로 트리거 추가][5]
    - [CloudWatch 로그 그룹에 수동으로 트리거 추가][6]

## 수집한 데이터

### 메트릭
{{< get-metrics-from-git "amazon_polly" >}}


AWS에서 검색된 각 메트릭에는 호스트 이름, 보안 그룹 등을 포함하되 이에 국한되지 않고 AWS 콘솔에 표시되는 동일한 태그가 할당됩니다.

### 이벤트

Amazon Polly 통합에는 이벤트가 포함되어 있지 않습니다.

### 서비스 검사

Amazon Polly 통합에는 서비스 점검이 포함되지 않습니다.

## 트러블슈팅

도움이 필요하신가요? [Datadog 지원팀][8]에 문의하세요.

[1]: https://docs.datadoghq.com/ko/integrations/amazon_web_services/
[2]: https://app.datadoghq.com/integrations/amazon-web-services
[3]: https://app.datadoghq.com/integrations/amazon-polly
[4]: https://docs.datadoghq.com/ko/logs/guide/forwarder/
[5]: https://docs.datadoghq.com/ko/integrations/amazon_web_services/?tab=allpermissions#collecting-logs-from-s3-buckets
[6]: https://docs.datadoghq.com/ko/integrations/amazon_web_services/?tab=allpermissions#collecting-logs-from-cloudwatch-log-group
[7]: https://github.com/DataDog/dogweb/blob/prod/integration/amazon_polly/amazon_polly_metadata.csv
[8]: https://docs.datadoghq.com/ko/help/