# 💡 데이터베이스란 무엇인가?

* **여러 사람에 의해 공유**되어 사용될 목적으로 통합하여 관리되는 데이터의 집합
* 작성된 목록으로써 여러 응용 시스템들의 통합된 정보들을 저장하여 운영할 수 있는 공용 **데이터들의 묶음**

# 💡 Database를 왜 사용하는가?

* 프로그램을 만들다보면 프로그램 사용자들에 의해 생성된 데이터, 프로그래머가 필요에 의해 프로그램에 넣어 놓은 데이터등 필연적으로 많은 데이터들이 생성되어지게 되는데 
데이터베이스를 사용하지 않으면 이 데이터들은 프로그램을 종료하는 순간 전부 날아가게 됩니다. 이러한 현상을 방지하기 위해 **데이터들을 데이터베이스에 넣고 보관하는 방법을 사용** 

# 💡 Database 용어?
<p align="center"><img src="https://user-images.githubusercontent.com/50662573/113497990-dabb7d80-9543-11eb-8546-07ce48531ed3.png"/></p>   

* 식별자(identifier) : 여러개의 집합체를 담고 있는 관계형 데이터베이스에서 각각의 구분할 수 있는 논리적인 개념   
    * 식별자의 특성
        * 유일성 : 하나의 릴레이션에서 모든 행은 서로 다른 키 값을 가져야 한다.
        * 최소성 : 꼭 필요한 최소한의 속성들로만 키를 구성해야한다. 
* 튜플(Tuple) : 테이블에서 행을 의미한다. 같은 말로 레코드(Record) 혹은 로우(Row)라고도 한다. 튜플은 릴레이션에서 같은 값을 가질 수 없다.
튜플의 수는 카디날리티(Cardinality)라고 한다.
* 속성(Attribute) : 테이블에서 열을 의미. 같은말로는 칼럼(Column)이라고도 하며 속성의 수를 의미하는단어는 Degree라고 한다.

# 💡 Database의 특징을 설명하시오.

1. 실시간 접근성
2. 지속적인 변화
3. 동시 공유
4. 내용에 대한 참조
5. 데이터 논리적 독립성

# 💡 Database 설계 시, 고려할 점을 설명하시오.

1. 무결성 : 삽입, 삭제, 갱신 등의 연산 후에도 데이터베이스에 저장된 **데이터가 정해진 제약조건을 항상 만족**해야함
2. 일관성 : 데이터베이스에 저장된 데이터들 사이나, 특정 질의에 대한 **응답이 처음부터 끝까지 변함없이 일정**해야함
3. 회복성 : 시스템에 장애가 발생했을 떄 **장애 발생 직전의 상태로 복구**할 수 있어야함
4. 보안성 : 불법적인 데이터의 노출 또는 변경이나 **손실로부터 보호**할 수 있어야함
5. 효율성 : **응답시간**의 단축, 시스템의 **생산성**, **저장 공간**의 최적화 등이 가능해야함
6. 확장성 : 데이터베이스 운영에 영향을 주지 않으면서 **지속적으로 데이터를 추가**할 수 있어야함

# 💡 Schema가 무엇인가요?

* **데이터베이스의 구조와 제약 조건**에 관한 **전반적인 명세를 기술**한 **메타데이터의 집합**
* 데이터베이스를 구성하는 데이터 **개체(Entity), 속성(Attribute), 관계(Relationship)** 및 데이터 조작 시 데이터 값들이 갖는 제약 조건 등에 관해 전반적으로 정의
* 사용자의 관점에 따라 **외부 스키마(사용자 뷰(View)), 개념 스키마(전체적인 뷰(View)), 내부 스키마(저장 스키마(Storage Schema))** 로 나눠진다.

# 💡 메타데이터란 무엇인가?

* 데이터에 대한 데이터이다. 
* "어떤 목적을 가지고 만들어진 데이터"라고도 정의한다.

# 💡 DBMS는 무엇인가요?

* 데이터베이스 관리 시스템 (Database Management System)
* **사용자와 데이터베이스 사이**에서 사용자의 요구에 따라 정보를 생성해주고 데이터베이스를 관리해주는 소프트웨어
* 기존의 파일 시스템이 갖는 데이터의 종속성과 중복성의 문제를 해결하기 위해 제안된 시스템으로 모든 응용 프로그램이 데이터베이스를 공용할 수 있도록 관리해준다.
* 데이터베이스의 구성, 접근 방법, 유지 관리에 대한 모든 책임을 진다.

# 💡 DBMS의 기능에는 무엇이 있나요?

* 정의 : 데이터에 대한 형식, 구조, 제약조건들을 명세하는 기능. 데이터베이스에 대한 정의 및 설명은 카탈로그나 사전의 형태로 저장
* 구축 : DBMS가 관리하는 기억 장치에 데이터를 저장하는 기능
* 조작 : 특정한 데이터를 검색하기 위한 질의, 데이터베이스의 갱신, 보고서 생성 기능 등을 포함
* 공유 : 여러 사용자와 프로그램이 데이터베이스에 동시에 접근하도록 하는 기능
* 보호 : 하드웨어나 소프트웨어의 오동작 또는 권한이 없는 악의적인 접근으로부터 시스템을 보호
* 유지보수 : 시간이 지남에 따라 변화하는 요구사항을 반영할 수 있도록 하는 기능

# 💡 DBMS의 종류에는 무엇이 있나요?

* Oracle
* MySQL
* MSSQL
* MariaDB

# 💡 데이터 모델링이 무엇인가요?

* 모델링이란 복잡한 현실 세계에 존재하는 데이터를 단순화시켜 표현해 컴퓨터 세계의 데이터베이스로 옮기는 변환 과정
* 현실의 개념들을 체계적으로 수집하여 정보모델링을 통해 사용자의 정보요구사항을 조사하고 이를 **개체, 관계, 속성을 중심으로 명확하게 체계적**으로 
**표현**하고 **문서화**하는 기법을 데이터 모델링이라고 한다.

* 데이터 모델링 3단계
    * 개념적 모델링
    * 논리적 데이터 모델링
    * 물리적 데이터 모델링

# 💡 키(Key)란?

* 데이터베이스에서 **조건에 만족하는 튜플을 찾거나** **순서대로 정렬**할 때 **다른 튜플들과 구별**할 수 있는 **유일한 기준**이 되는 Attribute(속성)이다.

# 💡 키의 종류에는 어떤게 있나요?

1. **후보키(Candidate Key)** : 릴레이션을 구성하는 **속성들 중**에서 **튜플을 유일하게 식별**할 수 있는 속성들의 부분집합을 의미
  * 모든 릴레이션은 반드시 하나 이상의 후보키를 가져야한다.
  * 릴레이션에 있는 모든 튜플에 대해서 유일성과 최소성을 만족시켜야한다.

2. **기본키(Primary Key)** : 후보키 중에서 선택한 주키(**Main Key**)
  * 한 릴레이션에서 특정 **튜플을 유일하게 구별**할 수 있는 속성
  * **Null 값을 가질 수 없다**.(개체 무결성의 첫번째 조건)
  * 기본키로 정의된 속성에는 동일한 값이 **중복되어 저장될 수 없다**.(개체 무결성의 두번째 조건)
  
3. **대체키(Alternate Key)** : 후보키가 둘 이상일 때 **기본키를 제외한 나머지 후보키**들을 말한다. **보조키**라고도 한다.

4. **슈퍼키(Super Key)** : 슈퍼키는 한 릴레이션 내에 있는 속성들의 집합으로 구성된 키로써 릴레이션을 구성하는 모든 튜플 중 슈퍼키로 구성된 
속성의 집합과 동일한 값은 나타내지 않는다.
  * 릴레이션을 구성하는 모든 튜플에 대해 **유일성은 만족하지만, 최소성은 만족시키지 못한다.**

5. **외래키(Foreign Key)** : 관계(Relation)을 맺고 있는 릴레이션 R1, R2에서 **릴레이션 R1이 참조하고 있는 릴레이션 R2의 기본키와 같은 R1 릴레이션의 속성**
  * 외래키는 참조되는 릴레이션의 기본키와 대응되어 릴레이션 간에 참조 관계를 표현하는데 중요한 도구로 사용
  * 외래키로 지정되면 **참조 테이블의 기본키에 없는 값은 입력할 수 없다**.(참조 무결성 조건)

# 💡 무결성 제약조건에 대해 아는대로 서술하시오.

1. **개체 무결성 **
  * 릴레이션에서 기본키를 구성하는 속성은 **Null값이나 중복값을 가질 수 없다.**
  
2. **참조 무결성**
  * 외래키 값은 **Null이거나 참조 릴레이션의 기본키 값과 동일**해야 한다. 즉 릴레이션은 참조할 수 없는 외래키 값을 가질 수 없다.

3. **도메인 무결성**  
  * 특정 속성의 값이 그 속성이 정의된 도메인에 속한 값이어야 한다는 규정 ex) 고등학교 학년은 1, 2, 3학년이니까 '학년'이라는 속성값의 범위는 무조건 1~3이다.

4. **고유 무결성**
  * 특정 속성에 대해 고유한 값을 가지도록 조건이 주어진 경우, 그 **속성값은 모두 달라야하는 제약조건**을 말한다.

5. **NULL 무결성** 
  * 특정 속성값에 Null이 올 수 없다는 조건이 주어진 경우, 그 속성값은 Null값이 올 수 없다는 제약 조건을 말한다.

6. 키 무결성
  * 한 릴레이션(테이블)에는 최소한 하나의 키가 존재해야 한다는 제약조건

# 💡 서브쿼리가 뭐에요?

* 하나의 SQL 문에 포함되어 있는 또다른 SQL문을 말한다.
* 서브쿼리 사용 가능한 위치
    * SLECT 절
    * FROM 절
    * WHERE 절
    * HAVING 절
    * ORDER BY 절
    * INSERT 문의 VALUES 절
    * UPDATE 문의 SET 절
 
* 단일행 서브쿼리
* 다중행 서브쿼리
* 다중칼럼 서브쿼리

# 💡 서브쿼리의 성능은 어때요?

* WHERE 절에 많은 서브쿼리가 포함될 경우, 성능이 좋지 않은 실행계획이 수립할 확률이 매우 높으므로 서브쿼리를 조인으로 변경하는 것이 더 좋다.