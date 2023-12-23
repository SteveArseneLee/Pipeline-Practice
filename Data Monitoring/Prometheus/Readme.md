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