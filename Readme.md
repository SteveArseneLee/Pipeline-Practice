## 다양한 파이프라인들을 테스트해보기 위한 레포지토리입니다.

어떤 기술스택이 어떤 상황에서 쓰이는지부터 분석합니다.

1. **Data Collection**
    - 기술 및 도구: Apache Kafka, Fluentd, Logstash, Beats, Scrapy, Beautiful Soup 등
    - 학습 방법: 공식 문서를 통해 기본 사용법을 익히고, 간단한 데이터 수집 프로젝트를 직접 수행해 보세요.
2. **Data Storage**
    - 기술 및 도구: MySQL, PostgreSQL, MongoDB, Apache Cassandra, Hadoop HDFS, Apache Parquet 등
    - 학습 방법: 각 데이터베이스의 특성과 사용법을 공식 문서로 학습하고, 실제 데이터를 저장하고 조회하는 실습을 진행해 보세요.
3. **Data Processing**
    - 기술 및 도구: Apache Hadoop, Apache Spark, Apache Flink, Apache Beam 등
    - 학습 방법: 공식 문서와 튜토리얼을 통해 기본 개념과 API를 익히고, 대용량 데이터 처리를 위한 실제 프로젝트를 수행해 보세요.
4. **Data Analysis**
    - 기술 및 도구: Python(pandas, numpy), R, Apache Hive, Apache Pig, Apache Zeppelin 등
    - 학습 방법: 기본 문법과 라이브러리 사용법을 익히고, 실제 데이터셋을 가지고 분석하는 프로젝트를 진행해 보세요.
5. **Data Monitoring and Feedback**
    - 기술 및 도구: Grafana, Kibana, Prometheus, Apache Superset 등
    - 학습 방법: 각 도구의 설치 및 설정 방법을 공식 문서를 통해 학습하고, 실시간 모니터링 대시보드를 구축해 보세요.

Data Engineering에서 활용되는 Data Pipeline에서 

## Pipeline 예시들
### 실시간 스트리밍 파이프라인

***상황***  
실시간 데이터 스트리밍과 분석이 필요한 상황.

***중요한 점***  
실시간 처리, 데이터의 실시간 유입을 처리할 수 있는 유연성, 실시간 분석 및 대시보드 지원 필요

***기술 도구***  
Fluentd, Logstash(데이터 수집) -> Kafka -> Apache Storm, Samza, Flink(Stream Processing) -> ElasticSearch, Cassandra(실시간 조회)


### 빅데이터 처리 파이프라인

***상황***  
대용량의 데이터를 처리해야하는 상황.

***중요한 점***  
대용량 데이터 처리, 분산 처리, 확장성, 데이터 무결성 및 복원력

***기술 도구***  
Sqoop, Flume(데이터 수집) -> Hadoop HDFS(데이터 저장) -> MapReduce, Spark(데이터 처리) -> HBase, Hive(데이터베이스) -> BI Tool(분석 결과 시각화)


### 데이터 웨어하우스 파이프라인

***상황***  
다양한 데이터 소스로부터 데이터를 통합해 분석을 수행하려는 상황.

***중요한 점***  
데이터 통합, 일관성, 데이터 보안 및 관리, 고성능 쿼리 처리 필요

***기술 도구***  
NiFi(데이터 수집) -> Beam(데이터 처리) -> Google BigQuery, Apache Druid(저장 및 OLAP 질의)


### MLOps 파이프라인
***상황***  
머신러닝 모델의 전체 생애주기를 관리하려는 상황.  

***중요한 점***  
모델 학습 및 배포 자동화, 모델 버전 관리, 모델 모니터링 및 재학습이 필요합니다.  

***기술 도구***  
Hadoop HDFS(데이터 수집&저장) -> PyTorch, TensorFlow(데이터 처리) -> Kubeflow, MLflow(모델 학습) -> Docker(배포)


### 실시간 데이터 처리 파이프라인
***상황***  
실시간으로 발생하는 데이터를 즉시 처리하고 분석해야하는 상황.

***중요한 점***  
실시간 처리, 데이터의 실시간 유입을 처리할 수 있는 유연성, 실시간 분석 및 대시보드 지원 필요  

***기술 도구***  
Kafka, RabbitMQ(데이터 수집) -> Flink, Storm, Spark Streaming(데이터 처리) -> ElasticSearch, Cassandra(데이터 저장)


### 데이터 레이크 파이프라인
***상황***  
다양한 형식의 데이터를 원시 형태로 저장하고, 필요에 따라 유연하게 조회하려는 상황

***중요한 점***  
다양한 형식의 데이터 저장, 데이터의 원시 형태 유지, 유연한 데이터 조회 필요

***기술 도구***
NiFi, Logstash(데이터 수집) -> Hadoop HDFS, AWS S3(데이터 저장) -> Hive, Presto(데이터 조회)