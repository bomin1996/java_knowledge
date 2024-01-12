### 면접 준비: Spring과 Spring Boot, BeanFactory와 ApplicationContext

#### Spring과 Spring Boot의 차이점

1. **Spring Framework**:
   - Spring은 경량화된 Java 기반의 엔터프라이즈 애플리케이션 개발을 위한 프레임워크입니다.
   - 의존성 주입, AOP, 트랜잭션 관리 등의 기능을 제공합니다.
   - 상세한 설정과 구성이 필요하며, 개발자가 많은 부분을 수동으로 설정해야 합니다.

2. **Spring Boot**:
   - Spring Boot는 Spring 기반 애플리케이션을 쉽게 만들 수 있도록 지원하는 도구입니다.
   - 'Convention over Configuration' 원칙에 따라 많은 설정을 자동화합니다.
   - 내장 서버, 메트릭스, 건강 체크, 외부 설정 등을 기본적으로 제공하여 빠르게 개발 시작이 가능합니다.

3. **주요 차이점**:
   - Spring Boot는 Spring Framework 위에 구축되어, 기존 Spring 프레임워크보다 더 빠르고 쉬운 개발 환경을 제공합니다.
   - Spring Boot는 별도의 설정 없이도 독립 실행이 가능한 애플리케이션을 만들 수 있게 해줍니다.

#### BeanFactory와 ApplicationContext의 차이점

1. **BeanFactory**:
   - Spring의 가장 기본적인 컨테이너로, DI 기능을 제공합니다.
   - `getBean()` 호출 시점에 의존성 주입이 이루어집니다 (Lazy Loading).
   - XML 파일을 통해 Bean 정의를 읽어들이고 관리합니다.

2. **ApplicationContext**:
   - BeanFactory를 확장한 컨테이너로, BeanFactory의 모든 기능을 포함합니다.
   - 추가적으로 이벤트 발행, AOP 지원, 국제화 지원 등의 기능을 제공합니다.
   - 컨테이너가 시작될 때 Bean 인스턴스를 미리 생성합니다 (Eager Loading).

3. **주요 차이점**:
   - ApplicationContext는 BeanFactory보다 더 많은 엔터프라이즈 지원 기능을 제공합니다.
   - BeanFactory는 자원이 제한된 디바이스와 같은 경량 애플리케이션에 적합한 반면, ApplicationContext는 엔터프라이즈급 애플리케이션 개발에 더 적합합니다.

### 결론
- Spring과 Spring Boot는 각각의 특징과 장단점을 갖고 있으며, 프로젝트의 요구사항과 개발 환경에 따라 적절히 선택하여 사용해야 합니다.
- BeanFactory와 ApplicationContext는 Spring의 IoC 컨테이너 구현체로, ApplicationContext가 더 많은 기능을 제공하는 고급 버전으로 볼 수 있습니다.
