## Circumstance
회사가 로그 데이터를 실시간으로 모니터링하고 분석해야 하는 경우.

### Pipeline
Apache Flume(로그 데이터 수집) => Apache Kafka(데이터 전송) => Apache Storm(실시간 데이터 처리) => Apache HBase(결과 저장&조회)