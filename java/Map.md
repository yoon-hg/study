Map (Interface)
: Map 인터페이스는 Collection 인터페이스와 다른 저장 방식을 가집니다.
Map 인터페이스를 구현한 Map 컬렉션 클래스들은 키와 값을 하나의 쌍으로 저장하는 방식(key-value 방식)을 사용합니다.


HashMap
  - key 와 value에 null을 허용한다.
  - 동기화를 보장하지 않는다.
 : HashMap은 thread-safe 하지 않는다. 싱글 쓰레드 환경에서 사용하는게 좋다. 
 동기화 처리를 하지 않기 때문에 데이터를 탐색하는 속도가 빠르다.
 HashTabe과 ConcurrentHashMap보다 데이터를 찾는 속도는 빠르지만, 신뢰성과 안정성이 떨어진다.


HashTable
  - key 와 value에 null을 허용하지 않는다.
  - 동기화를 보장한다.
: HashTable은 thread-safe하기 때문에, 멀티 쓰레드 환경에서 사용할 수 있다. 이는 데이터를 다르는 메소드(get(), put(), remove() 등)에 synchronized 키워드가 붙어있다. 해당 키워드는 메소드를 호출하기 전에 쓰레드간 동기화 락을 건다. 그래서 멀티 쓰레기 환경에서도 데이터의 무결성을 보장한다. 그러나, 쓰레드간 동기화 락은 매우 느린 동작이라는 단점이 있다.

ConcurrentHashMap
  - key 와 value에 null을 허용하지 않는다.
  - 동기화를 보장 한다.
: ConcurrentHashMap은 thread-safe하기 때문에, 멀티 쓰레드 환경에서 사용할 수 있다. 이 구현체는 HashMap의 동기화 문제를 보완하기 위해 나타났다. 동기화 처리를 할 때, 어떤 Entry를 조작하는 경우에 해당 Entry에 대해서만 락을 건다. 그래서 HashTable보다는 데이터를 다루는 속도가 빠르다. 즉, Entry 아이템별로 락을 걸어 멀티 쓰레드 환경에서의 성능을 향상시킨다.