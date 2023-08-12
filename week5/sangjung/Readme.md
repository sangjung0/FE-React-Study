배포 사이트: https://todoproject-45b57.web.app/

영어 영상 요약:
리엑트에서 코드를 깨끗하게 작성하기 위해 SOLID 원칙을 따라야 합니다. SOLID 원칙을 따라서 코드를 작성하면 수정, 유지보수, 테스트하기 그리고 읽는데 더 좋은 효과를 얻을 수 있습니다. SOLID는 약자이며 실제 뜻은 Single Responsiblity, Open-closed, Liskov Substitution, Interface Segregation, Dependency Inversion이다. 각각 단일 책임 원칙, 개발-폐쇄 원칙, Liskov 치환 원칙, 인터페이스 분리 원칙, 의존 역전 원칙이다.
Single Responsiblity
단일 책임 원칙이란, 컴포넌트 하나에 하나의 기능만을 넣는 것을 말한다. 하나의 컴포넌트에 여러가지 기능과 해당 기능을 랜더링하는 거대한 jsx를 넣으면 읽기도 쉽지 않을분더러 재사용성, 유지보수가 힘들게 된다. 그렇기에 각 기능별로 컴포넌트와 랜더링 부분을 나누는게 좋다. 또한 특정 기능이나 상태를 관리하기 위해서는 커스텀 훅을 사용하여 중복된 함수의 선언과 호출을 방지하는게 좋다.
Open-closed
개방-폐쇄 원칙이란, 프로그램 구성요소(컴포넌트 등)가 확장에는 열려있어야 되지만 수정에는 닫혀있어야 된다는 것을 의미한다. 확장을 할때는 구성요소의 코드 수정이 아닌 프로퍼티와 추상화를 활용하여 확장해야 한다.
Liskov Substitution
Liskov 치환 원칙이란, 프로그램(컴포넌트)의 상위 타입 객체를 하위 타입 객체로 치환해도 정상 작동해야 한다는 원칙이다. 상위 타입이 Input이고 하위 타입이 SearchInput이라면 같은 Props 값을 상위 타입과 하위 타입 어느 한 쪽에 줘도 정상 작동해야 한다는 의미이다. 
Interface Segregation
인터페이스 분리 원칙이란, 컴포넌트가 사용하지 않는 인터페이스(프로퍼티)에 의존해서는 안된다는 것이다. 각 컴포넌트에서만 사용할 프로퍼티를 생성하여 전달해야 한다. 예를들어 Img 컴포넌트에 imgValue를 전달하기위해 Product객체를 전달하여 Product.imgValue 값을 사용한다면 Product의 다른 값이 변해도 Img 컴포넌트가 작동하게 된다. 이를 Product가 아닌 Product.imgValue만을 전달하여 해결할 수 있다. 이렇게 컴포넌트에서 필요로하는 프로퍼티만 전달해야한다.
Dependency Inversion
의존 역전 원칙이란, 컴포넌트를 추상화하여 어디서든지 사용할 수 있게 하는 것이다. 컴포넌트 API와 유사하다고 보면 된다. 연결된 컴포넌트에서 추상화된 프로퍼티를 받아 구현할 수 있게 해야한다. 이렇게 하면 어떤 프로퍼티에 대해서든 구현가능하게 되며 재사용성이 높아진다.