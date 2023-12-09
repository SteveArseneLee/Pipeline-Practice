## Circumstance
머신러닝 모델을 학습하고 배포해야 하는 경우.

### Pipeline
Apache Hadoop(대용량 데이터 저장&처리) => Apache Spark(MLlib을 이용하여 머신러닝 모델을 학습) => Apache Kafka(실시간 데이터를 모델에 입력) => Apache Flink(실시간 분석 결과 생성).
