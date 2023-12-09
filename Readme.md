## 다양한 파이프라인들을 테스트해보기 위한 레포지토리입니다.

어떤 기술스택이 어떤 상황에서 쓰이는지부터 분석합니다.

1. Data Collection
2. Data Storage
3. Data Processing
4. Data Analysis
5. Data Monitoring and Feedback

Data Engineering에서 활용되는 Data Pipeline에서 

### Pipeline 예시들
실시간 스트리밍 파이프라인:
상황 : 실시간 데이터 스트리밍과 분석이 필요한 상황.
중요한 점: 실시간 처리, 데이터의 실시간 유입을 처리할 수 있는 유연성, 실시간 분석 및 대시보드 지원이 필요합니다.
기술 도구: 데이터 수집에는 Fluentd 또는 Logstash를 사용하고, 이를 Kafka로 전달합니다. 스트림 처리는 Apache Storm, Apache Samza 또는 Flink를 사용하며, 처리된 데이터는 Elasticsearch나 Cassandra에 저장하여 실시간 조회를 수행합니다.

빅데이터 처리 파이프라인:
상황 : 대용량의 데이터를 처리해야하는 상황.
중요한 점: 대용량 데이터 처리, 분산 처리, 확장성, 데이터 무결성 및 복원력이 중요합니다.
기술 도구: 데이터 수집에는 Sqoop이나 Flume를 사용하며, Hadoop HDFS에 저장합니다. 데이터 처리는 MapReduce나 Spark를 사용하고, 데이터베이스는 HBase 또는 Hive를 사용합니다. 분석 결과는 BI 도구를 통해 시각화합니다.

데이터 웨어하우스 파이프라인:
상황 : 다양한 데이터 소스로부터 데이터를 통합해 분석을 수행하려는 상황.
중요한 점: 데이터 통합, 일관성, 데이터 보안 및 관리, 고성능 쿼리 처리가 필요합니다.
기술 도구: 데이터 수집에는 Apache NiFi를 사용하며, 데이터 처리는 Apache Beam을 사용합니다. 처리된 데이터는 Google BigQuery나 Apache Druid에 저장하여 OLAP 질의를 수행합니다.

MLOps 파이프라인:
상황 : 머신러닝 모델의 전체 생애주기를 관리하려는 상황.
중요한 점: 모델 학습 및 배포 자동화, 모델 버전 관리, 모델 모니터링 및 재학습이 필요합니다.
기술 도구: 데이터 수집과 저장에는 Hadoop HDFS를 사용하며, 데이터 처리는 PyTorch나 TensorFlow를 사용합니다. 모델 학습은 Kubeflow, MLflow 등을 이용하고, 학습된 모델은 Docker 컨테이너로 배포합니다.

실시간 데이터 처리 파이프라인:
상황 : 실시간으로 발생하는 데이터를 즉시 처리하고 분석해야하는 상황.
중요한 점: 실시간 처리, 데이터의 실시간 유입을 처리할 수 있는 유연성, 실시간 분석 및 대시보드 지원이 필요합니다.
기술 도구: 데이터 수집에는 Apache Kafka나 RabbitMQ를 사용하고, 데이터 처리에는 Apache Flink, Storm, Spark Streaming을 이용합니다. 처리된 데이터는 Elasticsearch, Cassandra 등에 저장합니다.

데이터 레이크 파이프라인:
상황 : 다양한 형식의 데이터를 원시 형태로 저장하고, 필요에 따라 유연하게 조회하려는 상황
중요한 점: 다양한 형식의 데이터 저장, 데이터의 원시 형태 유지, 유연한 데이터 조회가 필요합니다.
기술 도구: 데이터 수집에는 Apache NiFi나 Logstash를 사용하며, 데이터 저장에는 Hadoop HDFS나 Amazon S3를 사용합니다. 데이터 조회에는 Apache Hive나 Presto를 이용합니다.