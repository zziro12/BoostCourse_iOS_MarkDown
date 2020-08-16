# ProjectB_SignUp
## 0. Hello
### 새로 배우는 내용   
- Design Patterns
    - Delegation Pattern
    - Singleton
    - Target-Action
- View Transition
    - Navigation Interface
    - Modality
- UIKit
    - UITextField
    - UIDatePicker
    - UIStackView
    - UIImagePickerController
    - UINavigationController
    - UIGestureRecognizer
    - View Controller States Methods
- Foundation
    - DateFormatter
- Swift
    - Dictionary의 활용
    - guard 구문의 활용
## 1. Human Interface Guidelines(H.I.G)

## 2. 화면의 전환
### 내비게이션 인터페이스란?

> iOS에서 내비게이션 인터페이스는 주로 계층적 구조의 화면전환을 위해 사용되는 드릴 다운 인터페이스(drill-down interface)입니다. 드릴 다운 인터페이스란 아래 그림과 같이 각 선택할 수 있는 항목에 대한 세부항목이 존재하는 인터페이스입니다.   

### 내비게이션 스택에서의 화면이동

> UINavigationController 클래스의 메서드 또는 <code>세그(segue)</code>를 사용하여 내비게이션 스택의 뷰 컨트롤러를 추가/삭제할 수 있습니다. 또한 애플리케이션 실행 중 사용자가 내비게이션 인터페이스의 뒤로가기(back) 버튼을 사용하거나 화면의 왼쪽 가장자리를 스와이프(swipe)하여 스택에 있는 최상위 뷰 컨트롤러를 삭제하고 그 아래에 가려져 있던 뷰 컨트롤러의 콘텐츠를 보여줄 수도 있습니다.   
> (*세그(segue)는 스토리보드에서 한 화면에서 다른 화면으로의 전환을 말합니다. 세그도 내부적으로 UINavigationController 클래스의 메서드를 사용합니다.)   
### UINavigationController 클래스 실습
### 모달이란?
> 모달(Modal)은 사용자의 이목을 끌기 위해 사용하는 화면전환 기법입니다. 사실, 화면을 전환한다기 보다는 이목을 집중해야 하는 화면을 다른 화면 위로 띄워(Presenting) 표현하는 방식입니다.   
> 모달로 보이는 화면을 사라지게 하려면 반드시 특정 선택을 해야한다는 특징이 있습니다. 예를 들어 얼럿을 통해 확인/취소 중 하나를 선택해야 한다거나 액션시트에서 무엇인가 선택을 해야한다.   
>  모달은 내비게이션 인터페이스와는 달리 정보의 흐름을 가지고 화면을 이동한다기 보다는 꼭 이목을 끌어야하는 화면에서 사용한다.     
> 내비게이션 인터페이스를 통해 화면을 표현하는 것과는 용도가 완전히 다르다고 볼 수 있다.   
> 그래서 모달로 보이는 화면은 되도록 단순하고 사용자가 빠르게 처리할 수 있는 내용을 표현하는 것이 좋습니다.   
### Presenting a View Controller

> 뷰 컨트롤러를 화면상에 나타내는 방법은 두 가지이다. 컨테이너뷰 컨트롤러에 임베드하거나, 프레젠테이션을 통해서 나타낼 수 있다.    
> 뷰 컨트롤러의 나타내기(present) 지원 기능은 `UIViewController` 클래스에 내장되어 있으며 모든 뷰 컨트롤러 객체에서 사용할 수 있다.     
> 뷰 컨트롤러를 나타내면 원래 뷰 컨트롤러(나타내는 뷰 컨트롤러 - presenting view controller)와 새롭게 나타나는 뷰 컨트롤러(나타나는 뷰 컨트롤러 - presented view controller) 간의 관계가 생성된다.   
> 이 관계를 뷰 컨트롤러 계층의 일부를 형성하며, 나타나는 뷰 컨트롤러(presented view controller)가 사라질(dismissed) 때까지 그대로 유지된다.   

### 프레젠테이션 및 전환 프로세스(The Presentation and Transition Process)

> 뷰 컨트롤러의 프레젠테이션은 새로운 콘텐츠를 화면에 애니메이션으로 표시할 수 있는 쉽고 빠른 방법이다.  `UIKit`에 내장된 프레젠테이션 기능은 내장 혹은 커스텀 애니메이션을 사용하여 새로운 뷰 컨트롤러를 표시할 수 있도록 한다.    
> 내장 프레젠테이션과 애니메이션은 `UIKit`이 모든 작업을 처리하기 때문에 아주 적은 코드로도 가능하다. 또한, 약간의 추가 코드를 이용해 커스텀 프레젠테이션 및 애니메이션을 사용할 수 있다. 
> 뷰 컨트롤러 프레젠테이션은 프로그래밍 방식 또는 세그(segues)를 사용하여 구현할 수 있습니다.   
## 3. 뷰의 상태변화 감지
### 뷰의 상태변화 감지 메서드

> 뷰가 화면에 보여지는 상태의 변화나 뷰의 레이아웃에 변화가 생기면 뷰 컨트롤러는 여러가지 메서드를 호출해 서브클래스가 적절한 대응을 할 수 있게 한다.     
- func viewDidLoad()
    - 뷰 계층이 메모리에 로드된 직후 호출되는 메서드
    - 뷰의 추가적인 초기화 작업을 하기 좋은 시점
    - 메모리에 처음 로딩 될때 1회 호출되는 메서드로, 메모리 경고로 뷰가 사라지지 않는 이상 다시 호출되지 않음
- func viewWillAppear(_ animated: Bool)  
    - 뷰가 뷰 계층에 추가되고 화면이 표시되기 직전에 호출되는 메서드
    - 뷰의 추가적인 초기화 작업을 하기 좋은 시점
    - 다른 뷰로 이동했다가 되돌아오면 재호출되는 메서드로, 화면이 나타날때마다 수행해야하는 작업을 하기 좋은 시점
- func viewDidAppear(_ animated: Bool)  
    - 뷰가 뷰 계층에 추가되어 화면이 표시되면 호출되는 메서드
    - 뷰를 나타내는 것과 관련된 추가적인 작업을 하기 좋은 시점
- func viewWillDisappear(_ animated: Bool) 
    - 뷰가 뷰 계층에서 사라지기 직전에 호출되는 메서드
    - 뷰가 생성된 뒤 발생한 변화를 이전상태로 되돌리기 좋은 시점
- func viewDidDisappear(_ animated: Bool)
    - 뷰가 뷰 계층에서 사라진 후 호출되는 메서드
    - 뷰를 숨기는 것과 관련된 추가적인 작업을 하기 좋은 시점
    - 시간이 오래 걸리는 작업은 하지 않는 것이 좋음
## 4. Delegation

## 5. Singleton

## 6. Target-Action

## 7. Gesture Recognizer

## 8. Summary
