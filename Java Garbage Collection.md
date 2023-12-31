# Java Garbage Collection

Java의 가비지 컬렉션(Garbage Collection, GC)은 자바 런타임 환경의 중요한 부분으로, 메모리 관리를 자동화하는 기능을 담당합니다. 이 프로세스는 사용되지 않는 메모리(즉, 더 이상 참조되지 않는 객체)를 자동으로 식별하고, 이를 해제하여 재사용할 수 있도록 만듭니다. 가비지 컬렉션의 주요 목표는 메모리 누수를 방지하고, 프로그래머가 메모리 관리에 대해 걱정하지 않도록 하는 것입니다.

## 가비지 컬렉션의 작동 원리

- **객체 추적**: Java는 '루트' 집합(예: 스택에 있는 지역 변수, 스태틱 변수 등)으로부터 도달할 수 있는 모든 객체를 추적합니다. 이러한 객체들은 '살아있는' 것으로 간주됩니다.
- **가비지 식별**: 도달할 수 없는 객체들, 즉 어떤 루트 집합에서도 참조되지 않는 객체들은 가비지로 간주됩니다.
- **메모리 회수**: 가비지 컬렉터는 이러한 가비지 객체들이 차지하고 있는 메모리를 해제하고, 필요에 따라 이를 다시 사용 가능한 상태로 만듭니다.

## 가비지 컬렉션 알고리즘

Java에서는 다양한 가비지 컬렉션 알고리즘을 사용합니다. 이 알고리즘들은 각각의 사용 사례와 성능 요구 사항에 따라 다를 수 있습니다:

- **Mark-and-Sweep**: 객체가 살아있는지 식별한 후, 사용되지 않는 객체들을 제거합니다.
- **Generational Collection**: 객체를 '세대'로 분류하고, 각 세대에 맞는 방식으로 메모리를 관리합니다. 이는 대부분의 객체가 젊은 세대에서 생성되고 빠르게 소멸된다는 관찰에 기반합니다.
- **Copying**: 사용되는 객체를 새로운 메모리 영역으로 복사하고, 나머지는 모두 버립니다.
- **Compacting**: 프래그먼테이션을 줄이기 위해 살아있는 객체들을 메모리의 한 쪽으로 몰아넣어 공간을 최적화합니다.

## 가비지 컬렉션의 장단점

### 장점

- 메모리 관리를 자동화하여 프로그래머의 부담을 줄입니다.
- 메모리 누수를 방지하고, 안정적인 애플리케이션 성능을 유지하는 데 도움이 됩니다.

### 단점

- 가비지 컬렉션 프로세스가 실행될 때 CPU 자원을 사용하므로 성능 저하가 발생할 수 있습니다.
- 예측하기 어려운 가비지 컬렉션 주기로 인해, 리얼타임 시스템에서는 문제가 될 수 있습니다.
