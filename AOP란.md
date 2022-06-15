AOP (Aspect orented programming)

- Targer
 : 어떤 대상에 부가 기능을 부여할 것인가

- Advice
 : 어떤 부가 기능 ? Before, AfterReturning, AfterThrowing, After, Around

- Join point
 : 어디에 적용할 것인가? 메서드, 필드 객체, 생성사 등

- Point cut
 : 실제 advice가 적용될 지점, Spring AOP에서는 advice가 적용될 메서드 선정


            Spring AOP                      AspectJ

목표        간단한 AOP 기능 제공            완벽한 AOP 기능 제공

joinPoint   메서드 레벨만 지원              생성자, 필드, 메서드등 다양하게 지원

weaving     런타임 시에만 가능              런타임은 제공하지 않음.(compile-time, post-compile, load-time 제공)

대상        spring container가 관리하는
            Bean에만 가능