# Kafka: The Definitive Guide Study

> 이 레포지토리는 **카프카 핵심 가이드** 북스터디를 위한 실습, 기록, 그리고 **팀 기준 카프카 도입·설계·운영 문서**를 남기기 위한 공간입니다.

**period**: `2026-02-02 ~ `

### 👥 멤버

- 강동윤 `@mentaldy`
- 김기찬 `@gichan222`
- 댐댐 `@GwonDooHyeon`
- 박종훈 `@Chapakook`
- 홍용준 `@yonggoose`

### 🐳 Kafka 실행 방법

#### Zookeeper 기반 Kafka 실습 환경

실습 환경 실행:

```bash
cd docker/zookeeper
./start.sh
```

- Bootstrap Server: localhost:9092

Kafka 데이터 초기화가 필요한 경우:

```bash
./stop.sh
rm -rf docker/zookeeper/data
```

#### KRaft 기반 Kafka 실습 환경

실습 환경 실행:

```bash
cd docker/kraft
./start.sh
```

- Bootstrap Server: localhost:9092

Kafka 데이터 초기화가 필요한 경우:

```bash
./stop.sh
rm -rf docker/kraft/data
```

#### ✅ Kafka 정상 기동 확인:

> start.sh 실행 후 아래 명령이 정상 출력되면 Kafka는 정상 기동 상태입니다.

1. 컨테이너 접속

```bash
docker exec -it kafka-tdg bash
```

2. Kafka 상태 확인 커맨드 실행

```bash
kafka-topics --bootstrap-server localhost:9092 --list
```

![kafka](https://github.com/user-attachments/assets/7e0bf971-6727-40fc-9118-a1ca99be1619)
