# hello-spring
### Spring을 사용해 간단한 웹페이지 구현
### Repository 변경가능-> SpringConfig에서 DI로 해결
### 구현한 Repository별 특징
   1. JDBC : SQL작성해야함, 반복적인 코드 작성
   2. JDBCTemplate : 코드가 훨씬 간단해졌지만 여전히 SQL 작성해야함
   3. JPA : EntityManager을 스프링 컨테이너에서 주입받아 이를 통해 엔티티의 영속성 관리
   4. Data JPA : 기본적인 CRUD 메서드를 구현하지 않아도된다.

### Test Code 작성
##### 주의사항
  1. 테스트 코드를 실행하기 전에 Service와 Repository를 컨테이너에서 주입받는다 -> @BeforeEach 어노테이션을 사용
  2. 테스트 메서드 하나를 실행하고 난 후에는 테스트에 사용된 테스트 케이스들이 남는다
    -> 오류 발생
    -> @AfterEach를 사용하여 테스트케이스를 삭제해준다.
