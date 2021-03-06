## 1. 개념

> 데코레이터 패턴은 기본 객체에추가적인 기능을 동적으로 유연하게 첨가하는 패턴이다.

### 1.1. 장점

- 객체에 동적으로 기능 추가가 간단하게 가능하다.

### 1.2. 단점

- 자잘한 데코레이터 클래스들이 계속 추가되어 클래스가 많아질 수 있다.
- 겹겹이 애워싸고 있기 때문에 객체의 정체를 알기 힘들고 복잡해질 수 있다.

### 1.3. 활용 상황

- 객체가 상황에 따라 다양한 기능이 추가되거나 삭제되어야 할 때.

## 2. 구조

![class_diagram](img/class_diagram.png)

- **Component**
    - ConcreteComponent 과 Decorator 가 구현할 인터페이스다.두 객체를 동등하게 다루기 위해 존재함
- **ConcreteComponent**
    - Decorate 를 받을 객체다.즉, 기능 추가를 받을 기본 객체
- **Decorator**
    - Decorate 를 할 객체의 추상 클래스다.즉, 기능 추가를 할 객체는 이 객체를 상속받는다.
- **ConcreteDecorator**
    - Decorator 를 상속받아 구현할 다양한 기능 객체이다.이 기능들은 ConcreteComponent 에 추가되기 위해 만들어 진다.

## 3. 구현

크리스마스 트리에 다양한 장식을 하고싶다고 해보자.
기본 크리스마스 트리가 있고, 장식으로는 깜빡이는 불이나, 꽃들을 생각해 볼 수 있다.