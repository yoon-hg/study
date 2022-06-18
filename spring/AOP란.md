AOP (Aspect orented programming)
 : AOP는 여러 오브젝트에 나타나는 공통적인 부가 기능을 모듈화하여 재사용하는 기법이다.

- Targer
 : 어떤 대상에 부가 기능을 부여할 것인가

- Advice
 : 어떤 부가 기능 ? Before, AfterReturning, AfterThrowing, After, Around
   * Before -> 매소드가 실행되기 전에
   * AfterReturning -> 매소드가 정상적으로 실행이 되었을 때
   * AfterThrowing -> 메소드가 예외처리를 실행 할 때
   * After -> 메소드가 정상적으로 실행이 되었을 때, 예외처리가 실행 되었을때 메소드가 종료 될 때
   * Around -> 메소드 시작, 종료 모두에 적용

- Join point
 : 어디에 적용할 것인가? 
  * 메서드 호출 할 때 (Spring에서 사용할 때는 메소드에서 사용한다고 보면 된다.)
  * 변수에 접근할 때
  * 객체를 초기화할 때
  * 객체에 접근할 때

- Point cut
 : 실제 advice가 적용될 지점, Spring AOP에서는 advice가 적용될 메서드 선정


 - AOP는 어디에 사용 될까?
  : 성능검사
  : 트랜젝션 처리
  : 로깅


            Spring AOP                      AspectJ

목표        간단한 AOP 기능 제공            완벽한 AOP 기능 제공

joinPoint   메서드 레벨만 지원              생성자, 필드, 메서드등 다양하게 지원

weaving     런타임 시에만 가능              런타임은 제공하지 않음.(compile-time, post-compile, load-time 제공)

대상        spring container가 관리하는
            Bean에만 가능