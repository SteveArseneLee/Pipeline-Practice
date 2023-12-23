# Prometheus

### Observability
**Tracing**  
- 프로그램의 실행 과정을 상세히 남기는 것
    - 호출하는 메소드의 시작 시간과 끝 시간을 남겨서 걸린 시간을 계산할 수 있게 하는 것.
    - 에러 발생 시 Stacktrace
    - network ping의 router trip 경로
- ex) Zipkin, Jaeger

**Monitoring**  
에러, 다운타임, 비정상 상태 등을 감지하기 위해서 이벤트, 메트릭 정보들을 남기고 추적하는 것. 크게 메트릭 모니터링과 로그 모니터링으로 나눌 수 있다.
- Metric Monitoring
    - 특정 기간이나 범위의 성공/실패 상태를 모니터링
    - 목표치 대비 성능의 상태나 관계를 모니터링
    - memory use, requests per second, active connections, flow, or number of errors
- Log Monitoring
    - 관심 있는 이벤트 데이터를 남기고 내용을 살피는 방식
    - 이벤트 데이터를 분석
        - filter -> aggregation -> metric
        - 텍스트 검색, 필터 검색

### 대표적인 Observability 도구들
1. Opentelemetry  
오픈소스로 만들어지는 통합 observability 스택.
- Tracing, Metric, Log를 수집해서 통합된 모니터링, 분석 환경을 제공함.
- 여러 언어별로 instrument sdk를 제공하고 여러 인프라 환경별로 collector도 개발되어 있음
- 전용 OpenTelemetry Protocol(OTLP)를 정의해놓아 직접 agent, collector를 구현할 수 있음.
2. Datadog
Cloud에서 운영되는 Observability 제품
- AWS, Azure, GCP등에 쉽게 integration할 수 있음
- 각 언어나 플랫폼 별로 데이터 수집을 위한 agent들도 제공하고 설치도 쉬움.
- 웹, 앱부터 백엔드까지 통합해서 모니터링하고 병목이나 장애지점을 진단할 수 있는 것이 큰 장점
3. Dynatrace
오래전부터 APM분야를 시작한 회사
- Java Tracing 도구들의 기능이 더 상세하고 성능이 좋은 편
- Datadog과 마찬가지로 Full stack observability를 제공하거나 제공하려고 함
- Cloud와 On-premise도 부분적 제공