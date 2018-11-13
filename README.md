# sqld-study



## 데이터 모델링의 이해

##### 발생시점에 따른 엔터티 분류

- 기본/키엔터티(Fundamental Entity, Key Entity)

- 중심엔터티(Main Entity)

- 행위엔터티(Active Entity)

##### 모델링의 특징

현실세계를 일정한 형식에 맞추어 표현하는 추상화의 의미를 가질 수 있음.

복잡한 현실을 제한된 언어나 표기법을 통해 이해하기 쉽게 하는 단순화의 의미를 가지고 있음

애매모호함을 배제하고 누구나 이해가 가능하도록 정확하게 현상을 기술하는 정확화의 의미를 가짐


##### 데이터 모델링이란

정보시스템을 구축하기 위한 데이터 관점의 업무 분석 기법

현실세계의 데이터(what)에 대해 약속된 표기법에 의해 표현하는 과정

데이터베이스를 구축하기 위한 분석/설계의 과정


##### 데이터 모델링이 필요한 주요 이유

업무정보를 구성하는 기초가 되는 정보들에 대해 일정한 표기법에 의해 표현한다

분석된 모델을 가지고 데이터베이스를 생성하여 개발 및 데이터 관리에 사용하기 위한 것이다.

데이터모델링 자체로서 업무의 흐름을 설명하고 분석하는 부분에 의미를 가지고 있다.


##### 데이터모델링의 유의점

데이터 모델을 어떻게 설계했느냐에 따라 사소한 업무변화에도 데이터 모델이 수시로 변경됨으로써 유지보수의 어려움을 가중시킬 수 있다. (비유연성)

데이터의 정의를 데이터의 사용 프로세스와 분리함으로써 데이터 모델링은 데이터 혹은 프로세스의 작은 변화가 애플리케이션과 데이터베이스에 중대한 변화를 일으킬 수 있는 가능성을 줄인다.(비유연성)

여러 장소의 데이터베이스에 같은 정보를 저장하지 않도록 하여 중복성을 최소화 한다.(중복)

데이터의 정의를 데이터의 사용 프로세스와 분리하여 유연성을 높인다.(비유연성)

데이터간의 상호 연관관계를 명확하게 정의하여 일관성 있게 데이터가 유지되도록 한다.(비일관성)

- 중복
- 비유연성
- 비일관성

##### 개념적 데이터 모델링

- 추상화 수준이 높고 업무중심적으로 포괄적인 수준의 모델링 진행.
- 전사적 데이터 모델링
- EA수립시 많이 이용

##### 논리적 데이터 모델링

- 시스템을 구축하고자 하는 업무에 대해 Key,  속성, 관계 등을 정확하게 표현, 재사용성이 높음

##### 물리적 데이터 모델링

- 실제로 데이터베이스에 이식할 수 있도록 성능, 저장 등 물리적인 성격을 고려하여 설계

##### 데이터 모델
전사적 데이터 모델링을 수행할 때 많이 하며, 추상화 수준이 높고 업무 중심적으로 포괄적인 수준의 모델링을 진행하는 것을 ***개념적*** 데이터 모델링 이라고 한다.

이와 달리 실제로 데이터베이스에 이식할 수 있도록 성능, 저장 등의 물리적인 성격을 고려한 데이터 모델링은 ***물리적*** 데이터 모델링 이라고 한다.

##### 데이터베이스 스키마 구조 3단계

- 외부스키마(External Schema)
- 개념스키마(Conceptual Schema)
  - 모든 사용자 관점을 통합한 조직 전체 관점의 통합적 표현
  - 모든 응용시트템들이나 사용자들이 필요로 하는 데이터를 통합한 조직 전체의 DB를 기술한 것으로
    DB에 저장되는 데이터와 그들간의 관계를 표현한 스키마

- 내부스키마(Internal Schema)

##### ERD 작성 순서

1. 엔터티를 그린다.
2. 엔터티를 적절하게 배치한다.
3. 엔터티간 관계를 설정한다.
4. 관계명을 기술한다.
5. 관계의 참여도를 기술한다.
6. 관계의 필수여부를 기술한다.

##### ERD에 대한 설명

1. 1976년 피터첸(Peter Chen)에 의해 Entity-Relationship Model(E-R Model)이라는 표기법이 만들어졌다.

2. 일반적으로 ERD를 작성하는 방법은 엔터티 도출 → 엔터티 배치 → 관계 설정 → 관계명 기술의 흐름으로 작업을 진행한다.
3. 관계의 명칭은 관계 표현에 있어서 매우 중요한 부분에 해당한다.
4. 가장 중요한 엔터티를 왼쪽 상단에 배치하고 추가 발생되는 엔터티들을 오른쪽 편과 하단에 배치하는 것이 원칙이다.

##### 엔터티 

S병원은 여러 명의 환자가 존재하고 각 환자에 대한 이름, 주소 등을 관리해야 한다.

(단, 업무범위와 데이터의 특성은 상기 시나리오에 기술되어 있는 사항만을 근거하여 판단해야 함)

→ 병원은 S병원 1개이므로 엔터티로 성립되지 않는다.

엔터티는 2개 이상의 속성과 2개이상의 인스턴스를 가져 면적으로 표현될 수 있어야 비로소 기본적인 엔터티 자격이 된다.

'여러명'의 복수 인스턴스와 이름, 주소 등의 복수속성을 가진 '환자'가 엔터티로 적절하다.

##### 엔터티의 특징

- 반드시 해당 업무에서 필요하고 관리하고자 하는 정보이어야 한다.(예. 토익의 응시횟수 ...)
- 유일한 식별자에 의해 식별이 가능해야 한다.
- 영속적으로 존재하는 인스턴스의 집합이어야 한다.('한 개'가 아니라 '두 개 이상')
- 업무 프로세스에 의해 이용되어야 한다.
- 반드시 속성이 있어야 한다.
- 다른 엔터티와 최소 한 개 이상의 관계가 있어야 한다.

##### 기본 엔터티

- 기본엔터티(키엔터티)란 그 업무에 원래 존재하는 정보로서 다른 엔터티와의 관계에 의해 생성되지 않고
  독립적으로 생성이 가능하고 자신은 타 엔터티의 부모의 역할을 하게 된다. 다른 엔터티로부터 주식별자를 상속받지않고 자신의 고유한 주식별자를 가지게 된다. 예를 들어 사원, 부서, 고객, 상품, 자재 등이 기본엔터티가 될 수 있다.

##### 엔터티를 부여하는 방법

1. 현업의 업무 용어를 사용하여 업무상의 의미를 분명하게 한다.
2. 모든 엔터티에서 유일한 이름이 부여되어야 한다.
3. 엔터티가 생성되는 의미대로 자연스럽게 부여하도록 한다.
4. 가능하면 약어를 사용하지 않는다.
5. 단수명사를 사용한다.

##### 엔터티, 인스턴스, 속성, 속성값의 관계

- 한 개의 엔터티는 두 개 이상의 인스턴스의 집합이어야 한다.
- 한 개의 엔터티는 두 개 이상의 속성을 갖는다.
- 한 개의 속성은 한 개의 속성값을 갖는다.

##### 속성 

- 사물의 성질, 특징 또는 본질적인 성질.
- "업무에서 필요로 하는 인스턴스에서 관리하고자 하는 의미상 더 이상 분리되지 않는 최소의 데이터 단위"
- 엔터티에 대한 자세하고 구체적인 정보를 나타낸다.
- 하나의 엔터티는 두 개 이상의 속성을 갖는다.
- 속성도 집합이다.
- 하나의 인스턴스에서 각각의 속성은 한 개의 속성값을 가져야 한다.

##### 속성의 특성에 따른 분류

- 기본속성
- 설계속성
- 파생속성
  - 데이터를 조회할 때 빠른 성능을 낼 수 있도록 하기 위해 원래 속성의 값을 계산하여 저장할 수 있도록 만든 속성



##### 데이터 모델의 개념

###### 도메인

- 각 엔터티(테이블)의 속성에 대해서 어떤 유형의 값이 들어가는지를 정의하는 개념
- 엔터티 내에서 속성에 대한 데이터타입과 크기 그리고 제약사항을 지정

##### 속성의 명칭 부여

- 해당 업무에서 사용하는 이름을 부여한다.
- 서술식 속성명은 사용하지 않는다.
- 약어사용은 가급적 제한한다.
- 전체 데이터모델에서 유일성 확보하는 것이 좋다.
- 속성의 명칭은 애매모호하지 않게, 복합 명사를 사용하여 구체적으로 명명함으로써 전체 데이터모델에서 유일성을 확보하는 것이 반정규화, 통합 등의 작업을 할 때 혼란을 방지할 수 있는 방법이 된다.

##### 데이터모델링의 관계

- 관계는 존재에 의한 관계와 행위에 의한 관계로 구분될 수 있으나 ERD에서는 관계를 연결할 때, 존재와 행위를 구분하지 않고 단일화된 표기법을 사용한다.
- UML(Unified Modeling Language)에는 클래스 다이어그램의 관계 중 연관관계(Association)와 의존관계(Dependency)가 있고 이것은 실선과 점선의 표기법으로 다르게 표현이 된다.
- 데이터모델링에서는 존재적 관계와 행위에 의한 관계를 구분하는 표기법이 없으며, UML 에서는 연관관계와 의존관계에 대해 다른 표기법을 가지고 표현하게 되어 있다.

##### 관계

- 관계는 존재적 관계와 행위에 의한 관계로 나누어볼 수 있다.
- 관계의 표기법은 관계명, 관계차수, 선택성(선택사양)의 3가지 개념으로 표현한다.
- 부서와 사원 엔터티 간의 '소속 ' 관계는 존재적 관계의 사례이다.
- 주문과 배송 엔터티 간의 '배송근거' 관계는 행위에 의한 관계의 사례이다.

##### 관계의 표기법

- 관계명(Membership) : 관계의 이름
- 관계차수(Cardinality) : 1:1, 1:M, M;N (관계의 기수성)
- 관계선택사양(Optionality) : 필수관계, 선택관계

##### 두 개의 엔터티 사이에서 관계를 도출 할 때 체크 할 사항

- 두 개의 엔터티 사이에 관심 있는 연관규칙이 존재하는가
- 두 개의 엔터티 사이에 정보의 조합이 발생되는가
- 업무기술서, 장표에 관계연결을 가능하게 하는 동사(Verb)가 있는가
- 업무기술서, 장표에 관계연결에 대한 규칙이 서술되어 있는가

##### 식별자의 종류

- 엔터티 내에서 대표성을 가지는가에 따라 주식별자(Primary Identifier)와 보조식별자(Alternate Identifier)로 구분
- 엔터티 내에서 스스로 생성되었는지 여부에 따라 내부식별자와 외부식별자(Foreign Identifier)로 구분
- 단일 속성으로 식별이 되는가에 따라 단일식별자(Single Identifier)와 복합식별자(Composit Identifier)로 구분
- 원래 업무적으로 의미가 있던 식별자 속성을 대체하여 일련번호와 같이 새롭게 만든 식별자를 구분하기 위해 본질식별자와 인조식별자로 구분

##### 주식별자를 지정할 때 고려해야 할 사항

- 주식별자에 의해 엔터티내에 모든 인스턴스들이 유일하게 구분되어야 한다.
- 주식별자를 구성하는 속성의 수는 유일성을 만족하는 최소의 수가 되어야 한다.
- 지정된 주식별자의 값은 자주 변하지 않는 것이어야 한다.
- 주식별자가 지정이 되면 반드시 값이 들어와야 한다.

##### 주식별자의 특징

- 유일성 : 주식별자에 의해 엔터티내에 모든 인스턴스들을 유일하게 구분함
- 최소성 : 주식별자를 구성하는 속성의 수는 유일성을 만족하는 최소의 수가 되어야 함
- 불변성 : 주식별자가 한 번 특정 엔터티에 지정되면 그 식별자의 값은 변하지 않아야 함
- 존재성 : 주식별자가 지정되면 반드시 데이터 값이 존재(Null 안됨)


##### 식별자와 비식별자관계 비교

| <center>**항목**</center>           | <center>**식별자 관계**</center> | <center>**비식별자관계**</center> |
| :----------------- | :-------------- | :--------------- |
| <center>목적</center>               | 강한 연결관계 표현 | 약한 연결관계 표현 |
| <center>자식 주식별자 영향</center> | 자식 주 식별자의 구성에 포함됨 | 자식 일반 속성에 포함됨 |
| <center>표기법</center>             | 실선 표현 | 점섬 표현 |
| <center>연결 고려사항</center>      | - 반드시 부모엔터티 종속<br />- 자식 주식별자구성에 부모 주식별자포함 필요<br />- 상속받은 주식별자속성을 타엔터티에 이전 필요 | - 약한 종속관계<br />- 자식 주식별자구성을 독립적으로 구성<br />- 자식 주식별자 구성에 부모 주식별자 부분 필요<br />- 상속받은 주식별자속성을 타 엔터티에 차단 필요<br />- 부모쪽의 관계참여가 선택관계 |



##### 비식별자 관계로 연결하는 것을 고려해야 하는 경우

- 부모엔터티에 참조값이 없어도 자식엔터티의 인스턴스가 생성될 수 있는 경우
- 여러 개의 엔터티를 하나로 통합하면서 각각의 엔터티가 갖고 있던 여러 개의 개별 관계가 통합되는 경우
- 자식쪽 엔터티의 주식별자를 부모엔터테와는 별도로 생성하는 것이 더 유리하다고 판단하는 경우
- 부모엔터티의 인스턴스가 자식의 엔터티와 관계를 가지고 있었지만 자식만 남겨두고 먼저 소멸될 수 있는 경우 비식별자관계로 연결
- 부모엔터티의 인스턴스가 자식 엔터티와 같이 소멸되는 경우는 비식별자 관계보다 식별자 관계로 정의하는 것이 더 적합


##### 식별자의 분류체계

<table>
    <thead>
        <th>분류</th>
        <th>식별자</th>
        <th>설명</th>
    </thead>
    <tr>
        <td width=120 rowspan=2>대표성 여부</td>
        <td width=120>주식별자</td>
        <td>엔터티 내에서 각 어커런스를 구분할 수 있는 구분자이며, 타 엔터티와 참조관계를연결할 수 있는 식별자</td>
    </tr>
	<tr>
    	<td>보조식별자</td>
        <td>엔터티 내에서 각 어커런스를 구분할 수 있는 구분자이나 대표성을 가지지 못해 참조관계를 연결하지 못함</td>
    </tr>
	<tr>
		<td rowspan=2>스스로 <br>생성 여부</td>
        <td>내부식별자</td>
        <td>엔터티 내부에서 스스로 만들어지는 식별자</td>
	</tr>
	<tr>
		<td>외부식별자</td>
        <td>타 엔터티와의 관계를 통해 타 엔터티로부터 받아오는 식별자</td>
	</tr>
    <tr>
		<td rowspan=2>속성의 수</td>
        <td>단일식별자</td>
        <td>하나의 속성으로 구성된 식별자</td>
	</tr>
	<tr>
		<td>복합식별자</td>
        <td>둘 이상의 속성으로 구성된 식별자</td>
	</tr>
    <tr>
		<td rowspan=2>대체 여부</td>
        <td>본질식별자</td>
        <td>업무에 의해 만들어지는 식별자</td>
	</tr>
	<tr>
		<td>인조식별자</td>
        <td>업무적으로 만들어지지는 않지만 원조식별자가 복잡한 구성을 가지고 있기 때문에 인위적으로 만든 식별자</td>
	</tr>
</table>

## 데이터 모델과 성능


##### 성능데이터모델링

- 데이터베이스 성능향상을 목적으로 설계단계의 데이터 모델링 때부터 성능과 관련된 사항이 데이터 모델링에 반영될 수 있도록 하는 것.
- 데이터의 증가가 빠를수록 성능저하에 따른 성능개선비용은 증가한다.
- 데이터모델은 성능을 튜닝하면서 변경이 될 수 있는 특징이 있다.
- 분석/설계 단계에서 성능을 고려한 데이터모델링을 수행할 경우 성능 저하에 따른 Rework비용을 최소화 할 수 있는 기회를 가지게 된다.

###### 문제 발생 시점의 SQL을 중심으로 집중 튜닝하는 것은 성능 데이터모델링과 무관

##### 반정규화(역정규화) 모델링 순서

1. 데이터모델링을 할 때 정규화를 정확하게 수행한다.
2. 데이터베이스 용량산정을 수행한다
3. 데이터베이스에 발생되는 트랜잭션의 유형을 파악한다.
4. 용량과 트랜잭션의 유형에 따라 반정규화를 수행한다.
5. 이력모델의 조정, PK/FK조정, 슈퍼타입/서브타입 조정 등을 수행한다.
6. 성능관점에서 데이터모델을 검증한다.

반정규화 고려할 때 판단 요소

- 다량 데이터 탐색의 경우 인덱스가 아닌 파티션 및 데이터 클러스터링 등의 다양한 물리 저장 기법을 활용하여 성능 개선을 유도할 수 있다. 다만, 하나의 결과셋을 추출하기 위해 다량의 데이터를 탐색하는 처리가 반복적으로 빈번하게 발생한다면 이때는 반정규화를 고려하는 것이 좋다.
- 이전 또는 이후 위치의 레코드에 대한 탐색은 window function으로 접근 가능하다.
- 집계 테이블 이외에도 다양한 유형(다수 테이블의 키 연결 테이블 등)에 대하여 반정규화 테이블 적용이 필요할 수 있다.

##### 테이블의 반정규화

<table>
    <thead>
        <th>기법분류</th>
        <th>반정규화 기법</th>
    </thead>
    <tr>
        <td rowspan=3>테이블 병합</td>
		<td>1:1 관계 테이블 병합</td>
    </tr>
    <tr>
        <td>1:M 관계 테이블병합</td>
    </tr>
    <tr>
        <td>슈퍼/서브타입 테이블병합</td>
    </tr>
    <tr>
        <td rowspan=2>테이블 분할</td>
        <td>수직분할</td>
    </tr>
    <tr>
        <td>수평분할</td>
    </tr>
    <tr>
        <td rowspan=4>테이블추가</td>
        <td>종목테이블 추가</td>
    </tr>
    <tr>
        <td>통계테이블 추가</td>
	</tr>
    <tr>
        <td>이력테이블 추가</td>
	</tr>
    <tr>
        <td>부분테이블 추가</td>
	</tr>
</table>


##### 칼럼의 반정규화

| <center>반정규화 기법</center>     |
| ---------------------------------- |
| 중복칼럼 추가                      |
| 파생칼럼 추가                      |
| 이력테이블 칼럼 추가               |
| PK에 의한 칼럼 추가                |
| 응용시스템 오작동을 위한 칼럼 추가 |

###### 디스크 I/O를 줄이기 위해 해당 칼럼들을 별도로 모아놓는 정규화 기법 : 테이블추가 - 부분테이블 추가



##### 반정규화 절차

1. 반정규화 대상조사
   - 범위처리빈도수 조사
   - 대량의 범위 처리 조사
   - 통계성 프로세스 조사
   - 테이블 조인 갯수
2. 다른 방법유도 검토
   - 뷰(VIEW) 테이블
   - 클러스터링 적용
   - 인덱스의 조정
   - 응용애플리케이션
3. 반정규화 적용
   - 테이블 반정규화
   - 속성의 반정규화
   - 관계의 반정규화

##### 반정규화의 대상에 대해 다른 방법으로 처리

- 지나치게 많은 조인(JOIN)이 걸려 데이터를 조회하는 작업이 기술적으로 어려울 경우 뷰(VIEW)를 사용하면 이를 해결할 수도 있다.
- 대량의 데이터처리나 부분처리에 의해 성능이 저하되는 경우에 클러스터링을 적용하거나 인덱스를 조정함으로써 성능을 향상시킬 수 있다.
- 대랴의 데이터는 Primary Key의 성격에 따라 부분적인 테이블로 분리할 수 있다. 즉 파티셔닝 기법이 적용되어 성능저하를 방지할 수 있다.
- 응용 애플리케이션에서 로직을 구사하는 방법을 변경함으로써 성능을 향상시킬 수 있다.

##### 칼럼수가 많은 테이블에 대한 설명

- 한 테이블에 많은 칼럼들이 존재할 경우 데이터가 물리적으로 저장되는 디스크 상에 넓게 분포할 가능성이 커지게 되어 디스크 I/O가 대량으로 발생할 수 있고, 이로 인해 성능이 저하될 수 있음.
- 트랜잭션이 접근하는 칼럼유형을 분석해서 자주 접근하는 칼럼들과 상대적으로 접근 빈도가 낮은 칼럼들을 구분하여 1:1로 테이블을 분리하면 디스크 I/O가 줄어들어 성능을 향상 시킬 수 있다.

##### 파티셔닝(Partitionning)

: 하나의 테이블에 많은 양의 데이터가 저장되면 인덱스를 추가하고 테이블을 몇 개로 쪼개도 성능이 저하되는 경우가 있다. 이때 논리적으로는 하나의 테이블이지만 물리적으로 여러 개의 테이블로 분리하여 데이터 액세스 성능도 향상시키고, 데이터 관리방법도 개선할 수 있도록 테이블에 적용하는 기법

##### 논리데이터모델의 슈퍼타입과 서브타입 데이터 모델을 물리적인 테이블 형식으로 변환할 때

- 트랜잭션은 항상 전체를 대상으로 일괄 처리하는데 테이블은 서브타입별로 개별 유지하는 것으로 변환하면 Union 연산에 의해 성능이 저하될 수 있다.
- 트랜잭션은 항상 서브타입 개별로 처리하는데 테이블은 하나로 통합하여 변환하면 불필요하게 많은 양의 데이터가 집적되어 있어 성능이 저하될 수 있다.
- 트랜잭션은 항상 슈퍼+서브 타입을 함께 처리하는데 개별로 유지 하면 조인에 의해 성능이 저하될 수 있다.
- 트랜잭션은 항상 전체를 통합하여 분석처리하는데 슈퍼-서브타입이 하나의 테이블로 통합되어 있으면 하나의 테이블에 집적된 데이터만 읽어 처리할 수 있기 때문에 다른 형식에 비해 더 성능이 우수하다(조인감소)

SQL의 성능 설명

select건수, 금액

from실적

where일자 between '20110101' and '20110102'

​	and 지사코드 = '1001'

- '=' 로 들어온 조건에 해당하는 칼럼이 인덱스의 가장 앞쪽에 위치할 때 인덱스의 이용 효율성이 가장 높다.
  (Where 절에 첫 번째 조건으로 , 첫번째에 위치하는 것이 효율성이 높음)


##### 분산 데이터베이스 장단점

1. 장점
   - 지역 자치성, 점증적 시스템 용량 확장
   - 신뢰성과 가용성
   - 효용성과 융통성
   - 빠른 응답속도와 통신비용 절감
   - 데이터의 가용성과 신뢰성 증가
   - 시스템 규모의 적절한 조절
   - 각 지역 사용자의 요구 수용 증대
2. 단점
   - 소프트웨어 개발 비용
   - 오류의 잠재성 증대
   - 처리 비용의 증대
   - 설계, 관리의 복잡성과 비용
   - 불규칙한 응답 속도
   - 통제의 어려움
   - 데이터 무결성에 대한 위협

데이터가 여러 지역에 분산되어 있지만 하나의 데이터베이스 처럼 사용하기를 원하는 분산데이터베이스 환경에서 데이터베이스 분산 설계를 적용하여 효율성을 증대시킬 수 있는 것

- 공통코드, 기준정보 등 마스터 데이터는 분산데이터베이스에 복제분산을 적용
- DBMS가 제공하는 FK Constraints를 생성했는지 여부와 상관없이 조인성능을 향상시키기 위한 인덱스를 생성해주는 것이 좋다.
- Gloabal Single Instance(GSI)를 구성할 때 분산데이터베이스를 활용하여 구성하는 것이 효율적이다.



## SQL 기본 및 활용



##### SQL 문장들의 종류

<table>
    <thead>
    	<th>명령어의 종류</th>
        <th>명령어</th>
        <th>설명</th>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3>데이터 조작어(DML : DataManipulation Language)</td>
        </tr>
        <tr>
            <td>SELECT</td>
            <td>데이터베이스에 들어 있는 데이터를 조회하거나 검색하기 위한 명령어를 말하는 것으로 RETRIEVE 라고도 한다.</td>
        </tr>
    	<tr>
        	<td>INSERT<br>UPDATE<br>DELETE</td>
        	<td>데이터베이스의 테이블에 들어 있는 데이터에 변형을 가하는 종류들의 명령어들을 말한다.예를 들어 데이터를 테이블에 새로운 행을 집어넣거나, 원하지 않는 데이터를 테이블에 새로운 행을 집어넣거나, 원하지 않는 데이터를 삭제하거나 수정하는 것들의 명령어들을 DML 이라고 부른다.</td>
    	</tr>
        <tr>
            <td>데이터 정의어(DDL: Data Definition Language)</td>
            <td>CREATE<br>ALTER<br>DROP<br>RENAME</td>
            <td>테이블과 같은 데이터 구조를 정의하는데 사용되는 명령어들로 그러한 구조를 생성하거나 변경하거나 삭제하거나 이름을 바꾸는 데이터 구조와 관련된 명령어들을 DDL이라고 부른다.</td>
        </tr>
		<tr>
            <td>데이터 제어어(DCL: Data Control Language)</td>
            <td>GRANT<br>REVOKE</td>
            <td>데이터베이스에 접근하고 객체들을 사용하도록 권한을 주고 회수하는 명령어를 DCL이라고 부른다.</td>
        </tr>
        <tr>
            <td>트랜잭션 제어어(TCL: Transaction Control Language)</td>
            <td>COMMIT<br>ROLLBACK</td>
            <td>논리적인 작업의 단위를 묶어서 DML에 의해 조작된 결과를 작업단위(트랜잭션)별로 제어하는 명령어를 말한다.</td>
        </tr>
	</tbody>
</table>

​    



##### 테이블 칼럼에 대한 정의 변경

- [Oracle]
  Alter table 테이블명 modify (칼럼명1 데이터 유형 [default 식], [not null], 칼럼명2 데이터 유형 ...);
- [SQL Server]
  Alter table 테이블명 alter (칼럼명1 데이터 유형 [default 식], [not null], 칼럼명2 데이터 유형...);

##### Null 설명

- 모르는 값을 의미한다.
- 값의 부재를 의미한다.
- 공백문자(Empty String) 혹은 숫자 0과 동일하지 않다.
- Null 과의 모든 비교(is null 제외) 는 알 수 없음(Unknown)을 반환한다.
- 아직 정의되지 않은 미지의 값
- 현재 데이터를 입려하지 못하는 경우



##### DDL 구문(DBMS는 Oracle 기준)

- DDL 올바른 문장

###### 1번 문장

create table PRODUCT( 

​	prod_id varchar2(10) not null

​	, prod_nm varchar2(100) not null)

​	, reg_dt date not null

​	, regr_no number(10) null

);

- DDL 잘못된 문장

###### 1번 문장

alter table PRODUCT add primary key product_pk on(prod_id); (X)

→ alter table PRODUCT add ***constraint*** product_pk primary key(prod_id); (O)

###### 2번 문장

create table PRODUCT( 

​	prod_id varchar2(10) not null

​	, prod_nm varchar2(100) not null)

​	, reg_dt date not null

​	, regr_no number(10) null

​	, ***add constraint primary key (prod_id***)

); (X)

→

create table PRODUCT( 

​	prod_id varchar2(10) not null

​	, prod_nm varchar2(100) not null)

​	, reg_dt date not null

​	, regr_no number(10) null

​	, ***constraint product_pk primary key(prod_id)***

); (O)



##### DDL 구문(DBMS는 SQLServer 기준)

기관분류(가)

| 분류 ID : varchar(10) not null                               |
| ------------------------------------------------------------ |
| 분류명 : varchar(10) not null<br />등록일자 : varchar(10) null |

→ 기관분류(가) 테이블을 아래 기관분류(나) 테이블처럼 변경하고자 한다.

기관분류(나)

| 분류 ID : varchar(10) not null                              |
| ----------------------------------------------------------- |
| 분류명 : varchar(30) not null<br />등록일자 : date not null |



- DDL 올바른 문장

alter table 기관분류 alter column 분류명 varchar(30) not null;



- DDL 잘못된 문장

###### 1번 문장

alter table 기관분류 alter column (분류명 varchar(30), 등록일자 date not null); (X)

alter table 기관분류 alter column (분류명 varchar(30) not null, 등록일자 date not null); (X)

→ SQLServer에서는 ***여러개의 컬럼을 동시에 수정하는 구문은 지원하지 않으므로*** 오류 발생. 또한 괄호를 사용하지 않는다.



###### 2번문장

alter table 기관분류 alter column 등록일자 date not null; (X)

→ 분류명을 수정할 때 not null 구문을 지정하지 않으면, 기존의 not null 제약조건이 null로 변경되므로 not null 요건을 만족하지 않는다.



EMP

| EMP_NO : varchar2(10) not null                               |
| ------------------------------------------------------------ |
| emp_nm : varchar2(30) not null<br />dept_code : varchar2(4) not null<br />join_date : date not null<br />regist_date : date null |

- DDL 올바른 문장

###### 1번 문장

create table EMP (

​	emp_no varchar2(10) primary key

​	, emp_nm varchar2(30) not null

​	, dept_code varchar2(4) default '0000' not null

​	, join_date date not null

​	, regist_date date null

); 

###### 2번 문장

create table EMP (

​	emp_no varchar2(10) not null

​	, emp_nm varchar2(30) not null

​	, dept_code varchar2(4) default '0000' not null

​	, join_date date not null

​	, regist_date date

);

alter table EMP add constraint emp_pk_primary key(emp_no);

create index idx_emp_01 on EMP (join_date);



- DDL 잘못된 문장

###### 1번 문장

create table EMP (

​	emp_no varchar2(10) primary key

​	, emp_nm varchar2(30) not null

​	, ***dept_code varchar2(4) default '0000'***

​	, join_date date not null

​	, regist_date date

);

→ SQL은 정상적으로 수행되지만, dept_code 칼럼에 not null 제약조건이 생성되지 않는다.

해당 칼럼에 null 을 입력하게 되면 문제가 발생한다.



###### 2번문장

create table EMP (

​	emp_no varchar2(10) not null ***primary key***

​	, emp_nm varchar2(30) not null

​	, dept_code varchar2(4) default '0000' not null

​	, join_date date not null

​	, join_date not null

);

***alter table EMP add constraint emp_pk_primary key (emp_no);***

create index idx_emp_01 on EMP (join_date);

→ 테이블 생성문과 인덱스 생성문은 정상적으로 수행되지만, 테이블 생성문장에서 이미 primary key를 지정하였으므로 alter table 문장에서 오류가 발생한다.



##### 테이블 생성시 칼럼별 생성할 수 있는 제약 조건(Constraints) 설명

- UNIQUE : 테이블 내에는 중복되는 값이 없으며 NOT NULL 특징을 갖는다.
- PK : 주키로 테이블당 1개만 생성이 가능하다.
- FK : 외래키로 테이블당 여러 개 생성이 가능하다.
- NOT NULL : 명시적으로 NULL 입력을 방지한다.

##### 테이블 생성의 주의사항

- 테이블명은 객체를 의미할 수 있는 적절한 이름을 사용한다. 가능한 단수형을 권고한다.
- 테이블 명은 다른 테이블 의 이름과 중복되지 않아야 한다.
- 한 테이블 내에서는 칼럼명이 중복되게 지정될 수 없다.
- 테이블 이름을 지정하고 각 칼럼들은 괄호 "( )"로 묶어 지정한다.
- 각 칼럼들은 콤마 "."로 구분되고, 테이블 생성문의 끝은 항상 세미콜론";"으로 끝난다.
- 칼럼에 대해서는 다른 테이블까지 고려하여 데이터베이스 내에서는 일관성 있게 사용하는 것이 좋다.(데이터 표준화 관점)
- 칼럼 뒤에 데이터 유형은 꼭 지정되어야 한다.
- 테이블명과 칼럼명은 반드시 문자로 시작해야 하고, 벤더별로 길이에 대한 한계가 있다.
- 벤더에서 사전에 정의한 예약어(Reserved word)는 쓸 수 없다.
- A-Z, a-z, 0-9, _, $, # 문자만 허용된다.



##### 왜래키

- 테이블 생성시 설정할 수 있다.
- 왜래키 값은 널 값을 가질 수 있다.
- 한 테이블에 여러개 존재할 수 있다.
- 왜래키 값은 참조 무결설 제약을 받을 수 있다.

##### 데이터베이스 테이블의 제약조건(Constraint)에 대한 설명

- Check 제약조건(Constraint)은 데이터베이스에서 데이터의 무결성을 유지하기 위하여 테이블의 특정 컬럼(Column)에 설정하는 제약이다.
- 기본키(Primary Key)는 반드시 테이블 당 하나의 제약만을 정의할 수 있다.
- 고유키(Unique Key)로 지정된 모든 컬럼은 Null 값을 가질 수도 있다.
- 왜래키(Foreign Key)는 테이블 간의 관계를 정의하기 위해 기본키(Primary Key)를 다른 테이블의 왜래키가 참조하도록 생성한다.

##### 테이블의 칼럼 삭제

- alter table 테이블명 drop column 삭제할 칼럼명;

##### 테이블에 데이터를 입력하는 두 가지 유형

- insert into 테이블명 ( column_list) values  (column_list);
  : column_list에 넣을 value_list
- insert into 테이블명 values ( 전체 column에 넣을 value_list);

##### 입력된 데이터의 수정

- update 테이블명 set 수정되어야 할 칼럼명 = 수정될 새로운 값

##### 테이블에 입력된 데이터 조회

- select [ALL / DISTINCT] 조회할 칼럼명, 조회할 칼럼명, ... from 해당 칼럼들이 있는 테이블명
  - ALL : Default 옵션이므로 별도로 표시하지 않아도 된다. 중복된 데이터가 있어도 모두 출력
  - DISTINCT : 중복된 데이터가 있는 경우 1건으로 처리해서 출력

##### DEPENDENT

표준 SQL(SQL:1999)에서 테이블 생성시 참조관계를 정의하기 위해 외래키(Foreign Key)를 선언한다. 관계형 데이터베이스에서 Child Table의 FK 데이터 생성시 Parent Table에 PK가 없는 경우, Child Table 데이터 입력을 허용하지 않는 참조동작(Referential Action)



##### Delete(/Modify) Action : Cascade, Set Null, Set Default, Restrict

1. Cascade : Master 삭제 시 Child 같이 삭제
2. Set Null : Master 삭제 시 Child 해당 필드 Null
3. Set Default : Master 삭제 시 Child 해당 필드 Default 값으로 설정
4. Restrict : Child 테이블에 PK 값이 없는 경우만 Master 삭제 허용
5. No Action : 참조무결성을 위반하는 삭제/수정 액션을 취하지 않음

##### Insert Action : Automatic, Set Null, Set Default, Dependent

1. Automatic  : Master 테이블에 PK가 없는 경우 Master PK를 생성 후 Child 입력
2. Set Null : Master 테이블에 PK가 없는 경우 Child 외부키를 null 값으로 처리
3. Set Default : Master 테이블에 PK가 없는 경우 Child 외부키를 지정된 기본값으로 입력
4. Dependent : Master 테이블에 PK가 존재할 때만 Child 입력 허용
5. No Action : 참조무결성을 위반하는 입력 액션을 취하지 않음

##### SQL 명령어

- TRUNCATE TABLE 테이블명;
  : 특정 테이블의 모든 데이터를 삭제하고, 디스크 사용량을 초기화 
- DELETE FROM 테이블명;
  : 테이블의 데이터를 모두 삭제하지만, 디스크 사용량을 초기화하지 않는다.
- DROP TABLE 테이블명;
  : 테이블의 데이터를 모두 삭제하고 디스크 사용량도 삭제(초기화) 하고 테이블의 스키마 정의도 함께 삭제된다.

###### DELETE TABLE FROM 테이블명; : 존재하지 않는 명령어



<table>
    <thead>
        <th>DROP</th>
        <th>TRUNCATE</th>
        <th>DELETE</th>
    </thead>
    <tbody>
        <tr>
            <td>DDL</td>
            <td>DDL(일부 DML 성격 가짐)</td>
            <td>DML</td>
        </tr>
        <tr>
            <td>Rollback 불가능</td>
            <td>Rollback 불가능</td>
            <td>Commit 이전 Rollback 가능</td>
        </tr>
        <tr>
            <td>Auto Commit</td>
            <td>Auto Commit</td>
            <td>사용자 Commit</td>
        </tr>
        <tr>
            <td>테이블이 사용했던 Storage를 모두 Release(해제)</td>
            <td>테이블이 사용했던 Storage중 최초 테이블 생성시 할당된 Storage만 남기고 Release</td>
            <td>데이터를 모두 Delete해도 사용했던 Storage는 Release되지 않음</td>
        </tr>
        <tr>
            <td>테이블의 정의 자체를 완전히 삭제함</td>
            <td>테이블을 최초 생성된 초기상태로 만듦</td>
            <td>데이터만 삭제</td>
        </tr>
    </tbody>
</table>



##### 트랜잭션의 특징

- 원자성(atomicity) : 트랜잭션에서 정의된 연산들은 모두 성공적으로 실행되던지 아니면 전혀 실행되지 않은 상태로 남아 있어야 한다.(All or Nothing)
- 일관성(consistency) : 트랜잭션이 실행 되기 전의 데이터베이스 내용이 잘못 되어 있지 않다면 트랜잭션이 실행된 이후에도 데이터베이스의 내용에 잘못이 있으면 안된다.
- 고립성(isolation) : 트랜잭션이 실행되는 도중에 다른 트랜잭션의 영향을 받아 잘못된 결과를 만들어서는 안된다.
- 지속성(durability) : 트랜잭션이 성공적으로 수행되면 그 트랜잭션이 갱신한 데이터베이스의 내용은 영구적으로 저장된다.



##### 데이터베이스 트랜잭션에 대한 격리성이 낮은 경우 발생할 수 있는 문제

1. Dirty Read : 다른 트랜잭션에 의해 수정되었고 이미 커밋된 데이터를 읽는 것
2. isolation : 트랜잭션이 실행되는 도중에 다른 트랜잭션의 영향을 받아 잘못된 결과를 만들어서는 안된다.



- 트랜잭션(Transaction) :  데이터베이스의 논리적 연산산뒤로서 밀접히 관련되어 분리될 수 없는 한 개 이상의 데이터베이스 조작
- 커밋(Commit) : 트랜잭션의 종료를 위한 대표적 명령어로서는 데이터에 대한 변경사항을 데이터베이스에 영구적으로 반영
- 롤백(Rollback) : 데이터에 대한 변경사항을 모두 폐기하고 변경전의 상태로 되돌림.



- Begin Transaction

  : Begin Transaction ( BEGIN TRAN ) 으로 시작하고 Commit Transaction( Transaction은 생략 가능 ) 또는 Rollback 구문을 만나면 최초의 BEGIN TRANSACTION 시점까지 모두 ROLLBACK 수행

- 저장점(SAVEPOINT)
  : 롤백(ROLLBACK)할 때 트랜잭션에 포함된 전체 작업을 롤백하는 것이 아니라 현 시점에서 SAVEPOINT까지 트랜잭션의 일부만 롤백할 수 있다.

---

##### ORACLE

SAVEPOINT SVPT1;

...

ROLLBACK TO SVPT1;



##### SQL Server

SAVE TRANSACTION

​	SVTR1;

...

ROLLBACK

​	TRANSACTION

​	SVTR1;

---



##### WHERE 절

- FROM 절 다음에 위치
- 칼럼(Column)명 (보통 조건식의 좌측에 위치)
- 비교 연산자
- 문자, 숫자, 표현식(보통 조건식의 우측에 위치)
- 비교 칼럼명(JOIN 사용시)

##### 실행 결과 적절한 것

| EMPNO | SAL  |
| ----- | ---- |
| 100   | 1500 |
| 200   | 3000 |
| 300   | 2000 |

SELECT COUNT(*)

FROM EMP

WHERE EMPNO > 100 AND SAL >= 3000 OR EMPNO = 200;

→ 1

논리연산자의 우선순위는 NOT > AND > OR 순



##### 연산자의 우선순위

1. 괄호로 묶은 연산
2. 부정 연산자(NOT)
3. 비교 연산자 (=, >, >=, <=)와 SQL 비교 연산자 ( BETWEEN a AND b, IN (list), LIKE, IS NULL)
4. 논리 연산자 중 AND, OR 의 순으로 처리

##### BETWEEN a AND b

- a와 b의 값 사이에 있으면 된다. (a와 b 값이 포함됨)

##### IN (list)

- 리스트에 있는 값 중에서 어느 하나라도 일치하면 된다.



##### NULL의 연산

- NULL 값과의 연산(+, -, *, / 등) 은 NULL 값을 리턴
- NULL 값과의 비교연산 (=, >, >=, <=)은 거짓(FALSE)을 리턴
- 특정 값보다 크다, 적다라고 표현할 수 없음.



##### 부정 비교 연산자

- != : 같지 않다.
- ^= : 같지 않다.
- <> : 같지 않다. (ISO 표준, 모든 운영체제에서 사용 가능)
-  NOT 칼럼명 = : ~와 같지 않다.
- NOT 칼럼명 > : ~보다 크지 않다.



| 문자형 함수                                               | 함수 설명                                                    |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| LOWER(문자열)                                             | 문자열의 알파벳 무자를 소문자로 바꾸어 준다.                 |
| UPPER(문자열)                                             | 문자열의 알파벳 문자를 대문자로 바꾸어 준다.                 |
| ASCII(문자)                                               | 문자나 숫자를 ASCII 코드 번호로 바꾸어 준다.                 |
| CHR / CHAR(ASCII번호)                                     | ASCII 코드 번호를 문자나 숫자로 바꾸어 준다.                 |
| CONCAT(문자열1, 문자열2)                                  | Oracle, My SQL에서 유효한 함수이며 문자열1과 문자열2를 연결한다.<br />합성 연산자 '\|\|' (Oracle)나 '+'(SQL Server)와 동일하다. |
| SUBSTR / SUBSTRING (문자열, m [,n])                       | ex) substring("test", 1, 3) , substring("test", 1)<br />문자열 중 m 위치에서 n개의 문자 길이에 해당하는 문자를 돌려준다.<br />n이 생략되면 마지막 문자까지다. |
| LENGTH / LEN(문자열)                                      | 문자열의 갯수를 숫자값으로 돌려준다.                         |
| LTRIM(문자열 [, 지정문자])                                | 문자열의 첫 문자부터 확인해서 지정 문자가 나타나면 해당 문자를 제거한다. (지정 문자가 생략되면 공백 값이 디폴트)<br />SQL Server에서는 LTRIM 함수에 지정문자를 사용할 수 없다. 즉, 공백만 제거할 수 있다. |
| RTRIM(문자열 [, 지정문자])                                | 문자열의 마지막 문자부터 확인해서 지정 문자가 나타나는 동안 해당 문자를 제거한다. (지정 문자가 생략되면 공백 값이 디폴트)<br />SQL Server 에서는 RTRIM 함수에 지정문자를 사용할 수 없다. 즉 , 공백만 제거할 수 있다. |
| TRIM ([leading \| trailing \| both] 지정문자 FROM 문자열) | 문자열에서 머릿말, 꼬릿말, 또는 양쪽에 있는 지정 문자를 제거한다.<br />(leading \| trailing \| both 가 생략되면 both 가 디폴트)<br />SQL Server에서는 TRIM 함수에 지정문자를 사용할 수 없다. 즉, 공백만 제거할 수 있다. |

###### ※주 : Oracle함수 / SQL Server 함수 표시,  '/' 없는 것은 공통 함수



##### DUAL 테이블의 특성

- 사용자 SYS가 소유하며 모든 사용자가 액세스 가능한 테이블이다.
- SELECT ~ FROM ~ 의 형식을 갖추기 위한 일종의 DUMMY 테이블이다.
- DUMMY라는 문자열 유형의 칼럼에 'X' 라는 값이 들어 있는 행을 1건 포함하고 있다.



##### 오라클 환경 날짜형 데이터

SELECT TO_CHAR(TO_DATE('2015.01.10 10', 'YYYY.MM.DD HH24') + 1/24/(60/10), 'YYYY.MM.DD HH24:MI:SI') FROM DUAL;

1/24/60 = 1분을 의미

1/24/(60/10) = 10분

→ 2015.01.10 10:10:00



---

##### SEARCHED_CASE_EXPRESSION SQL 문장을 SIMPLE_CASE_EXPRESSION 문장으로

- SEARCHED_CASE_EXPRESSION
  SELECT LOC,
  ​	CASE WHEN LOC = 'NEW YORK' THEN 'EAST'
  ​		ELSE 'ETC'
  ​	END as AREA
  FROM DEPT

→

- SIMPLE_CASE_EXPRESSION
  SELECT LOC,
  ​	CASE LOC WHEN 'NEW YORK' THEN 'EAST'
  ​		ELSE 'ETC'
  ​	END as AREA
  FROM DEPT;

---

##### NULL의 특성

- 널 값은 아직 정의되지 않은 값으로 - 또는 공백과 다르다. -은 숫자이고, 공백은 하나의 문자이다.
- 테이블을 생성할 때 NOT NULL 또는 PRIMARY KEY로 정의되지 않은 모든 데이터 유형은 널 값을 포함할 수 있다.
- 널 값을 포함하는 연산의 경우 결과 값도 널 값이다. 모르는 데이터에 숫자를 더하거나 빼도 결과는 마찬가지로 모르는 데이터인 것과 같다.
- 결과 값을 NULL 이 아닌 다른 값을 얻고자 할 때 NVL / ISNULL 함수를 사용한다.
- NULL 값의 대상이 숫자유형 데이터인 경우는 주로 0(Zero)으로, 문자유형 데이터인 경우는 블랭크 보다는 'x' 같이 시스템에서 의미 없는 문자로 바꾸는 경우가 많다.


##### 단일행 NULL 관련 함수의 종류

| 일반형 함수                                      | 함수 설명                                                    |
| ------------------------------------------------ | ------------------------------------------------------------ |
| NVL(표현식1, 표현식2) / ISNULL(표현식1, 표현식2) | 표현식 1의 결과 값이 NULL 이면 표현식 2의 값을 출력한다.<br />단, 표현식 1과 표현식 2의 결과 데이터 타입이 같아야 한다.<br />NULL 관련 가장 많이 사용되는 함수이므로 상당히 중요하다. |
| NULLIF(표현식1, 표현식2)                         | 표현식1이 표현식2와 같으면 NULL, 같지 않으면 표현식1을 리턴한다. |
| COALESCE(표현식1, 표현식2, ...)                  | 임의이 개수 표현식에서 NULL이 아닌 최초의 표현식을 나타낸다. <br />모든 표현식이 NULL 이라면 NULL을 리턴한다. |

###### ※ 주 : Oracle 함수/ SQL Server 함수 표시, '/' 없는 것은 공통 함수

##### NULL 관련 함수

- NVL(표현식1, 표현식2)
  Oracle 함수
  ISNULL(표현식1, 표현식2)
- SQL Server 함수
  NULLIF(표현식1, 표현식2)
  COALESCE(표현식1, 표현식2, ...)

##### 단일행 NULL 관련 함수의 종류

| 일반형 함수                                      | 함수 설명                                                    |
| ------------------------------------------------ | ------------------------------------------------------------ |
| NVL(표현식1, 표현식2) / ISNULL(표현식1, 표현식2) | 표현식1의 결과값이 NULL 이면 표현식2의 값을 출력한다. 단, 표현식1과 표현식2의 결과 데이터 타입이 같아야 한다. |
| NULLIF(표현식1, 표현식2)                         | 표현식1이 표현식2와 같으면 NULL을, 같지 않으면 표현식1을 리턴한다. |
| COALESCE(표현식1, 표현식2, ...)                  | 임의의 개수 표현식에서 NULL이 아닌 최초의 표현식을 나타낸다.<br />모든 표현식이 NULL이라면 NULL을 리턴한다. |

※ 주 : Oracle 함수/ SQL Server 함수 표시, '/' 없는 것은 공통 함수

##### SQL 수행 결과 값은?

| C1   | C2   | C3   |
| ---- | ---- | ---- |
| 1    | 2    | 3    |
|      | 2    | 3    |
|      |      | 3    |

SELECT SUM(COALESCE(C1, C2, C3)) FROM TAB1

→ 6  (COALESCE 함수는 첫번째 NULL이 아닌 값을 반환한다. → 1 2 3)


##### 집계 함수의 종류

| 집계 함수                        | 사용 목적                                                  |
| -------------------------------- | ---------------------------------------------------------- |
| COUNT(*)                         | NULL 값을 포함한 행의 수를 출력한다.                       |
| COUNT(표현식)                    | 표현식의 값이 NULL 값인 것을 제외한 행의 수를 출력한다.    |
| SUM([DISTINCT \| ALL] 표현식)    | 표현식의 NULL 값을 제외한 합계를 출력한다.                 |
| AVG([DISTINCT \| ALL] 표현식)    | 표현식의 NULL 값을 제외한 평균을 출력한다.                 |
| MAX([DISTINCT \| ALL] 표현식)    | 표현식의 최대값을 출력한다.(문자, 날짜 데이터 타입도 가능) |
| MIN([DISTINCT \| ALL] 표현식)    | 표현식의 최소값을 출력한다.(문자, 날짜 데이터 타입도 가능) |
| STDDEV([DISTINCT \| ALL] 표현식) | 표현식의 표준 편차를 출력한다.                             |
| VARIAN([DISTINCT \| ALL] 표현식) | 표현식의 분산을 출력한다.                                  |
| 기타 통계 함수                   | 벤더별로 다양한 통계식을 제공한다.                         |



##### GROUP BY 문장

SELECT (DISTINCT) 칼럼명 (ALIAS명) FROM 테이블명

 (WHERE 조건식) (GROUP BY 칼럼(COlUMN)이나 표현식) (HAVING 그룹조건식);



###### 직원 테이블(EMP)이 직급(GRADE) 별로 사원 500명, 대리 100명, 과장 30명, 차장 10명, 부장 5명, 직급이 정해지지 않은(NULL) 사람 25명

SQL1) 부터 SQL3) 까지 순차 실행 결과값? 

SQL1) SELECT COUNT(GRADE) FROM EMP;

SQL2) SELECT GRADE FROM EMP WHERE GRADE IN ('차장', '부장', '널');

SQL3) SELECT GRADE, COUNT(*) FROM EMP GROUP BY GRADE;



###### SELECT COUNT(GRADE) FROM EMP;

- 645명 : 사원 500명 + 대리 100명 + 과장 30명 + 차장 10명 + 부장 5명  이때 NULL 25건은 제외

###### SELECT GRADE FROM EMP WHERE GRADE IN ('차장', '부장', '널');

- 15명 : 차장 10명 + 부장 5명
  - '널' 텍스트로 입력된 데이터는 없다고 봐야 함.
  - 정의되지 않은 미지의 값인 NULL 과 '널'텍스트 데이터는 다름. 또한 IN('차장', '부장', NULL)로 변경하여도 실제 NULL 데이터는 출력되지 않음. NULL 비교는 오직 'IS NULL, IS NOT NULL' 만 가능

###### SELECT GRADE, COUNT(*) FROM EMP GROUP BY GRADE;

- 6건 : 5개 직급 + NULL 기준별 데이터 수가 6건 출력됨



##### GROUP BY 절과 HAVING 절의 특성

- GROUP BY 절을 통해 소그룹별 기준을 정한 후, SELECT 절에 집계 함수를 사용한다.
- 집계 함수의 통계 정보는 NULL 값을 가진 행을 제외하고 수행한다
- GROUP BY 절에서는 SELECT 절과는 달리 ALIAS 명을 사용할 수 없다.
- 집계 함수는 WHERE 절에는 올 수 없다.(집계 함수를 사용할 수 있는 GROUP BY 절보다는 WHERE 절이 먼저 수행된다)
- WHERE 절은 전체 데이터를 GROUP 으로 나누기 전에 행들을 미리 제거시킨다.
- HAVING 절은 GROUP BY 절의 기준 항목이나 소그룹의 집계 함수를 이용한 조건을 표시할 수 있다.
- GROUP BY 절에 의한 소그룹별로 만들어진 집계 데이터 중, HAVING 절에서 제한 조건을 두거 조건을 만족하는 내용한 출력한다.
- HAVING 절은 일반적으로 GROUP BY 절 뒤에 위치한다.



##### PARTITION BY

- 특정 조건을 기준으로 그룹핑을 하고, 해당 그룹 별 순위를 부여함
- OVER 절이 있어야 함
- SELECT NAME, AGE, RANK() OVER ( PARTITION BY AGE ORDER BY NAME DESC) AS Rank FROM USER



##### ORDER BY 문장

- SELECT 칼럼명 (ALIAS명) FROM 테이블명 (WHERE 조건식) (GROUP BY 칼럼(COLUMN)이나 표현식) (HAVING 그룹조건식) (ORDER BY 칼럼(COLUMN이나 표현식 {ASC 또는 DESC}));
- ASC(Ascending) : 조회한 데이터를 오름차순으로 정렬한다. (기본 값이므로 생략 가능)
- DESC(Descending) : 조회한 데이터를 내림차순으로 정렬한다.



##### ORDER BY 절 특징

- 기본적인 정렬 순서는 오름차순(ASC)이다.
- 숫자형 데이터 타입은 오름차순으로 정렬했을 경우에 가장 작은 값부터 출력된다.
- 날짜형 데이터 타입은 오름차순으로 정렬했을 경우 날짜 값이 가장 빠른 값이 먼저 출력된다.
- Oracle에서는 NULL 값을 가장 큰 값으로 간주하여 오름차순으로 정렬했을 경우에는 가장 마지막에, 내림차순으로 정렬했을 경우에는 가장 먼저 위치한다.
- 반면, SQL Server에서는 NULL 값을 가장 작은 값으로 간주하여 오름차순으로 정렬했을 경우에는 가장 먼저, 내림차순으로 정렬했을 경우네느 가장 마지막에 위치한다.

##### SELECT 문자 실행 순서

1. 발췌 대상 테이블을 참조한다.(FROM)
2. 발췌 대상 데이터가 아닌 것을 제거한다.(WHERE)
3. 행들을 소그룹화 한다.(GROUP BY)
4. 그룹핑된 값의 조건에 맞는 것만을 출력한다. (HAVING)
5. 데이터 값을 출력/ 게산한다. (SELECT)
6. 데이터를 정렬한다. (ORDER BY)

##### [TOP () 예제] 사원

- 테이블에서 급여가 높은 2명을 내림차순으로 출력하는데 같은 급여를 받는 사원이 있으면 같이 출력한다.
  - SELECT TOP(2) WITH TIES ENAME, SAL FROM EMP ORDER BY SAL DESC;

###### 5개의 테이블로부터 필요한 칼럼을 조회하려고 할 때, 최소 몇 개의 JOIN 조건이 필요한가?

→ 4개 ( 최소 N-1 개의 JOIN 조건이 필요)

##### EUQI JOIN 문장

- SELECT 테이블1.칼럼명, 테이블2.칼럼명, ... FROM 테이블1, 테이블2 WHERE 테이블1.칼럼명1 = 테이블2.칼럼명2; → WHERE 절에 JOIN 조건을 넣는다.

##### ANSI/ISO SQL 표준 EQUI JOIN 문장

- SELECT 테이블1.칼럼명, 테이블2.칼럼명, ... FROM 테이블1 INNER JOIN 테이블2 ON 테이블1.칼럼명1 = 테이블2.칼럼명2; → ON 절에 JOIN 조건을 넣는다.



##### Join에 대한 설명

1. 일반적으로 Join은 PK와 FK 값의 연관성에 의해 성립된다.
2. EQUI Join은 Join에 관여하는 테이블 간의 컬럼 값들이 정확하게 일치하는 경우에 사용되는 방법이다.
3. EQUI Join은 '=' 연산자에 의해서만 수행되며, 그 이외의 비교 연산자를 사용하는 경우에는 모두 Non EQUI Join이다.
4. 대부분 Non EQUI Join을 수행할 수 있지만, 때로는 설계상의 이유로 수행이 불가능한 경우도 있다.



##### LIKE 연산자 조인

[EMP_TBL]

| EMPNO | ENAME |
| ----- | ----- |
| 1000  | SMITH |
| 1050  | ALLEN |
| 1100  | SCOTT |

[RULE_TBL]

| RULE_NO | RULE |
| ------- | ---- |
| 1       | S%   |
| 2       | %T%  |

[SQL]

SELECT COUNT(*) CNT

FROM EMP_TBL A, RULE_TBL B

WHERE A.ENAME LIKE B.RULE

→ 4



| EMPNO | ENAME | RULE |
| ----- | ----- | ---- |
| 1100  | SMITH | S%   |
| 1100  | SCOTT | S%   |
| 1000  | SMITH | %T%  |
| 1100  | SCOTT | %T%  |



## SQL 활용

##### 순수 관계 연산자와 SQL 문장 비교

- SELECT 연산은 WHERE 절로 구현
- PROJECT 연산은 SELECT 절로 구현
- (NATURAL) JOIN 연산은 다양한 JOIN 기능으로 구현
- DIVIDE 연산은 현재 사용되지 않음



ANSI/ISO SQL 에서 표시하는 FROM 절의 JOIN형태

- INNER JOIN
  - INNER JOIN은 OUTER(외부) JOIN과 대비하여 내부 JOIN이라고 하며, JOIN 조건에서 동일한 값이 있는 행만 반환
  - 교집합, 모두의 값에 있는 행들만 포함시키고 그렇지 않는 행들은 제외 시킨다.
- NATURAL JOIN
- USING 조건절
- ON 조건절
- CROSS JOIN
  - 테이블 간 JOIN 조건이 없는 경우 생길 수 있는 조합을 말한다. 결과는 양쪽 집합의 M*N건의 데이터 조합이 발생한다.
- OUTER JOIN(LEFT, RIGHT, FULL)
  - LEFT OUTER JOIN : 조인 수행시 먼저 표기된 좌측 테이블에 해당하는 데이터를 먼저 읽은 후, 나중 표기된 우측 테이블에서 JOIN 대상 데이터를 읽어 온다. 즉, Table A와 B가 있을 때 (Table 'A'가 기준이 됨),
    A와 B를 비교해서 B의 JOIN 칼럼에서 같은 값이 있을 때 그 해당 데이터를 가져오고, B의 JOIN 칼럼에서 같은 값이 없는 경우에는 B 테이블에서 가져오는 칼럼들을 NULL 값으로 채운다.
  - FULL OUTER JOIN : 조인 수행시 좌측, 우측 테이블의 모든 데이터를 읽어 JOIN하여 결과를 생성한다. 즉, TABLE A와 B가 있을 때 (TABLE 'A', 'B' 모두 기준이 됨), RIGHT OUTER JOIN과 LEFT OUTER JOIN의 결과를 합집합으로 처리한 결과와 동일하다.

##### OUTER JOIN 문장 예시

- LEFT OTER JOIN
  - SELECT X.KEY1, Y.KEY2 FROM TAB1 X LEFT OUTER JOIN TAB2 Y ON (X.KEY1=Y.KEY2)
  - 오른쪽 테이블에 조인시킬 칼럼이 없는 경우 사용
- RIGHT OUTER JOIN
  - SELECT X.KEY1, Y.KEY2 FROM TAB1 X RIGHT OUTER JOIN TAB2 Y
  - 왼쪽 테이블에 조인시킬 칼럼의 값이 없는 경우 사용
- FULL OUTER JOIN
  - SELECT X.KEY1, Y.KEY2 FROM TAB1 X FULL OUTER JOIN TAB2 Y ON (X.KEY1 = Y.KEY2)
  - 양쪽 테이블 모두 Outer Join 걸어야 하는 경우



##### 집합 연산자의 종류

| 집합 연산자 | 연산자의 의미                                                |
| ----------- | ------------------------------------------------------------ |
| UNION       | 여러 개의 SQL 문의 결과에 대한 합집합으로 결과에서 모든 중복된 행은 하나의 행으로 만든다. |
| UNION ALL   | 여러 개의 SQL문의 결과에 대한 합집합으로 중복된 행도 그대로 결과로 표시된다. 즉, 단순히 결과만 합쳐놓은 것이다. 일반적으로 여러 질의 결과가 상호 배타적인(Exclusive)일 때 많이 사용한다. 개별 SQL문의 결과가 서로 중복되지 않는 경우, UNION과 결과가 동일하다.(결과의 정렬 순서에는 차이가 있을 수 있음) |
| INTERSECT   | 여러 개의 SQL문의 결과에 대한 교집합이다. 중복된 행은 하나의 행으로 만든다. |
| EXCEPT      | 앞의 SQL문의 결과에서 뒤의 SQL문의 결과에 대한 차집합이다. 중복된 행은 하나의 행으로 만든다. (일부 데이터베이스는 MINUS를 사용함) |

##### SET OPERATOR

- UNION : 합집합
- INTERSECT : 교집합
- MINUS / EXCEPT : 차집합

##### PRIOR

- CONNECT BY절에 사용되며, 현재 읽은 칼럼을 지정한다.
- PRIOR 자식 = 부모 형태를 사용하면 계층구조에서 부모 데이터에서 자식 데이터(부모 → 자식) 방향으로 전개하는 순방향 전개를 한다. 그리고 PRIOR 부모 = 자식 형태를 사용하면 반대로 자식 데이터에서 부모 데이터(자식 → 부모) 방향으로 전개하는 역방향 전개를 한다.

##### 오라클 계층형 질의

- START WITH 절은 계층 구조의 시작점을 지정하는 구문이다. 즉, 루트 데이터를 지정한다.(액세스)
- ORDER SIBLINGS BY 절은 형제 노드 사이(동일 LEVEL)에서 정렬을 지정하는 구문이다.
- 순방향 전개란 부모 노드로부터 자식 노드 방향으로 전개하는 것을 말한다.
- 루트 노드의 LEVEL 값은 1이다.

##### 셀프 조인(Self Join)

- 동일 테이블 사이의 조인을 말한다.
- FROM 절에 동일 테이블이 두 번 이상 나타난다.
- 동일 테이블 사이의 조인을 수행하면 테이블과 칼럼 이름이 모두 동일하기 때문에 식별을 위해 반드시 테이블 별칭(Alias)를 사용해야 한다.
- 한 테이블 내에서 두 칼럼이 연관 관계가 있다.

##### 셀프 조인 문장

- SELECT ASLIAS명1.칼럼명, ASLIAS명2.칼럼명, ...
  FROM 테이블 ALIAS명1, 테이블 ALIAS명2
  WHERE ALIAS명1.칼럼명2 = ALIAS명2.칼럼명1;



<table>
    <thead>
        <th width=200>서브 쿼리 종류</th>
        <th>설명</th>
    </thead>
    <tbody>
        <tr>
            <td>Single Row<br />서브쿼리<br />(단일 행 서브쿼리)</td>
            <td>서브쿼리의 실행 결과가 항상 1건 이하인 서브쿼리를 의미한다.<br />단일 행 서브쿼리는 단일 행 비교 연산자와 함께 사용된다.<br />단일 행 비교 연산자에는 =, <,  <=, >, >=, <>이 있다.</td>
        </tr>
        <tr>
            <td>Multi Row<br />서브쿼리<br />(다중 행 서브쿼리)</td>
            <td>서브쿼리의 실행 결과가 여러 건인 서브쿼리를 의미한다.<br />다중행 서브쿼리는 다중 행 비교 연산자와 함께 사용된다.<br />다중 행 비교 연산자에는 IN, ALL, ANY, SOME, EXISTS가 있다.<br />다중 행 서브쿼리 비교 연산자는 단일 행 서브쿼리의 비교 연산자로도 사용할 수 있다.</td>
        </tr>
        <tr>
            <td>Multi Column<br />서브쿼리<br />(다중 칼럼 서브쿼리)</td>
            <td>서브쿼리의 실행 결과로 여러 칼럼을 반환한다.<br />메인쿼리의 조건절에 여러 칼럼을 동시에 비교할 수 있다. 서브 쿼리와 메인 쿼리에서 비교하고자 하는 칼럼 갯수와 칼럼의 위치가 동일해야 한다.</td>
        </tr>
    </tbody>
</table>

###### 서브쿼리의 결과가 복수행 결과를 반환하는 경우네느 IN, ALL, ANY등의 복수 행 비교 연산자와 사용하여야 한다.

###### 다중 칼럼 서브쿼리는 서브쿼리의 결과로 여러 개의 칼럼이 반환되어 메인 쿼리의 조건과 비교되는데, SQL Server에서는 현재 지원하지 않는 기능이다.

##### 서브쿼리를 사용시 주의사항

1. 서브쿼리를 괄호로 감싸서 사용한다.
2. 서브쿼리는 단일행(Single Row)또는 복수행(Multiple Row) 비교 연산자와 함께 사용 가능하다.
   단일 행 비교 연산자는 서브쿼리의 결과가 반드시 1건 이하이어야 하고 복수행 비교 연산자는 서브쿼리의 결과 건수와 상관없다.
3. 서브쿼리에서는 ORDER BY를 사용하지 못한다.
   ORDER BY절은 SELECT 절에서 오직 한 개만 올 수 있기 때문에 ORDER BY 절은 메인쿼리의 마지막 문장에 위치해야 한다.

##### 서브쿼리

- 단일 행 서브쿼리의 비교연산자로는 =, <, <=, >, >=, <>가 되어야 한다. IN, ALL 등의 비교연산자는 다중 행 서브쿼리의 비교 연산자 이다.
- 단일 행 서브커리의 비교연산자는 다중 행 서브쿼리의 비교연산자로 사용할 수 없지만, 반대의 경우는 가능하다.
- 비 연관 서브쿼리가 주로 메인쿼리에 값을 제공하기 위한 목적으로 사용된다.
- 메인 쿼리의 결과가 서브쿼리로 제공될 수도 있고, 서브쿼리의 결과가 메인쿼리로 제공될 수도 있으므로 실행 순서는 상황에 따라 달라진다.

##### 뷰 사용의 장점

- 독립성 : 테이블 구조가 변경되어도 뷰를 사용하는 응용 프로그램은 변경하지 않아도 된다.
- 편리성 : 복잡한 질의를 뷰로 생성함으로써 관련 질의를 단순하게 작성할 수 있다. 또한 해당 형태의 SQL문을 자주 사용할 때 뷰를 이용하면 편리하게 사용할 수 있다.
- 보안성 : 직원의 급여정보와 같이 숨기고 싶은 정보가 존재한다면, 뷰를 생성할 때 해당 칼럼을 빼고 생성함으로써 사용자에게 정보를 감출 수 있다.
- 뷰는 단지 정의만을 가지고 있으며, 실행 시점에 질의를 재작성하여 수행한다.
- 뷰는 보안을 강화하기 위한 목적으로도 활용할 수 있다.
- 실제 데이터를 저장하고 있는 뷰를 생성하는 기능을 지원하는 DBMS도 있다.

##### ROLLUP : 계층 구조를 가진 SUB TOTAL을 생성하는 함수로 나열된 칼럼의 순서가 변경되면 수행결과도 변경된다. ROLLUP(A, B)를 수행하면 (A, B) 별 집계,  A별 집계와 전체 집계를 출력할 수 있다.

- Grouping Columns이 가질 수 있 는 모든 경우에 대하여 Subtotal을 생성해야 하는 경우에는 CUBE를 사용하는 것이 바람직하나, ROLLUP에 비해 시스템에 많은 부담을 주므로 사용에 주의해야 한다.

- CUBE는 결합 가능한 모든 값에 대하여 다차원 집계를 생성한다. CUBE 도 결과에 대한 정렬이 필요한 경우는 ORDER BY절에 명시적으로 정렬 칼럼이 표시가 되어야 한다.

- CUBE, GROUPING SETS, ROLLUP 세가지 그룹 함수 모두 일반 그룹함수로 동일한 결과를 추출할 수 있다.
- 함수의 인자로 주어진 칼럼의 순서에 따라 다른 결과를 추출하게 되는 그룹 함수는 ROLLUP이며, 나열된 칼럼에 대해 계층 구조로 집계를 출력한다.
- CUBE, ROLLUP, GROUPING SETS함수들에 의해 집계된 레코드에서 집계 대상 칼럼 이외의 GROUP 대상 칼럼의 값은 NULL을 반환한다.
- GROUPING SETS은 다양한 소계 집합을 만들 수 있는데, GROUPING SETS에 표시된 인수들에 대한 개별 집계를 구할 수 있으며, 이때 표시된 인수들 간에는 계층 구조인 ROLLUP과는 달리 평등한 관계이므로 인수의 순서가 바뀌어도 결과는 같다.
- GROUPING SETS 함수도 결과에 대한 정렬이 필요한 경우는 ORDER BY 절에 명시적으로 정렬 칼럼이 표시되어야 한다.

##### 순위를 구하는 함수

1.  RANK 함수
   - ORDER BY 를 포함한 QUERY문에서 특정 항목(칼럼)에 대한 순위를 구하는 함수이며 동일한 값에 대해서는 동일한 순위를 부여하게 된다. 중간 순위를 비워 둠

2.  DENSE_RANK 함수
   - 동일 순위를 부여하되 중간 순위를 비우지 않는다.
   - 동일한 순위를 하나의 건수로 취급
3. ROW_NUMBER 함수
   - 동일 값에 대해서도 유일한 순위를 부여한다.



##### LAG 함수

- 파티션별 윈도우에서 이전 몇 번째 행의 값을 가져올 수 있다.  

##### LEAD 함수

- 파티션별 윈도우에서 이후 몇 번째 행의 값을 가져올 수 있다.

###### (SQL Server에서는 지원하지 않는 함수)



##### ROLE

- DBMS 사용자를 생성하면 기본적으로 많은 권한을 부여해야 한다. 많은 DBMS에서는 DBMS 관리자가 사용자별로 권한을 관리해야 하는 부담과 복잡함을 줄이기 위하여 다양한 권한을 그룹으로 묶어 관리할 수 있도록 사용자와 권한 사이에서 중개 역할을 수행

##### GRANT 

- DBMS에 생성된 USER와 다양한 권한들 사이에서 중개 역할을 할 수 있도록 DBMS에는 ROLE을 제공한다.
  이러한 ROLE을 DBMS USER에게 부여하기 위해서 사용하는 명령어

##### REVOKE

- 권한을 회수하기 위한 명령어

##### PL / SQL 의 특징

- Block 구조로 되어 있어 각 기능별로 모듈화가 가능하다.
- 여러 SQL 문장을 Block으로 묶고 한 번에 Block 전부를 서버로 보내기 때문에 통신량을 줄일 수 있다.
- 변수, 상수 등을 선언하여 SQL 문장 간 값을 교환한다.
- IF, LOOP 등의 절차형 언어를 사용하여 절차적인 프로그램이 가능하도록 한다.
- DBMS정의 에러나 사용자 정의 에러를 정의하여 사용할 수 있다.
- Oracle에 내장되어 있으므로 Oracle과 PL / SQL을 지원하는 어떤 서버로도 프로그램을 옮길 수 있다.
- 응용프로그램의 성능을 향상시킨다.













