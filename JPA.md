# JPA 심화 주제

## 1. 고급 매핑
- **상속 매핑**: 객체 지향에서의 상속 개념을 데이터베이스에 매핑합니다. 주요 전략으로는 조인 전략, 단일 테이블 전략, 테이블 별 구분 전략이 있습니다.
- **복합 키와 임베디드 키**: 복합 키를 사용하여 엔티티를 매핑합니다. `@Embeddable`과 `@EmbeddedId`를 사용하여 복합 키를 구현합니다.

## 2. 쿼리
- **JPQL**: Java Persistence Query Language는 SQL과 유사하지만 엔티티 객체에 집중된 쿼리 언어입니다.
- **Criteria API**: 프로그래매틱하게 쿼리를 생성하는 방법으로, 복잡한 쿼리 작성에 유용합니다.
- **네이티브 SQL**: JPA를 사용하면서도 특정 데이터베이스에 특화된 순수 SQL 쿼리를 실행할 수 있습니다.

## 3. 캐싱
- **1차 캐시**: 영속성 컨텍스트 내부에 있는 캐시로, 트랜잭션 내에서 엔티티를 재사용할 때 사용됩니다.
- **2차 캐시**: 애플리케이션 범위의 캐시로, 여러 영속성 컨텍스트 간에 엔티티를 공유할 수 있습니다.

## 4. 트랜잭션과 락
- **트랜잭션 관리**: JPA에서 데이터베이스 작업을 트랜잭션으로 묶어 일관성을 유지합니다.
- **락(Lock)**: 동시성 문제를 관리하기 위한 메커니즘. 낙관적 락과 비관적 락을 사용할 수 있습니다.

## 5. 성능 최적화
- **페치 전략**: 지연 로딩(Lazy Loading)과 즉시 로딩(Eager Loading)을 사용하여 성능을 최적화합니다.
- **배치 처리**: 대량의 데이터를 효율적으로 처리하기 위해 배치 작업을 수행합니다.
- **N+1 문제**: 관계형 엔티티 조회 시 발생할 수 있는 성능 문제를 해결하는 전략을 구현합니다.

## 6. JPA 확장 기능
- **객체 그래프 탐색**: 엔티티 간의 관계를 통해 복잡한 객체 그래프를 탐색하고 조작합니다.
- **리스너와 콜백**: 엔티티의 생명주기 이벤트(생성, 업데이트, 삭제 등)에 대한 콜백을 처리합니다.

JPA의 심화 주제들은 복잡한 애플리케이션에서 데이터베이스 작업의 효율성과 안정성을 높이는 데 중요한 역할을 합니다. 이러한 주제들을 이해하고 적용함으로써, 개발자는 더 효과적이고 유지보수가 용이한 데이터 액세스 레이어를 구축할 수 있습니다.