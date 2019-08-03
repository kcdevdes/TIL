## 속정 옵저버란?

---

속성의 값이 바뀔 때 반응하는 객체이다. 

새로운 값이 속성에 할당되면 자동으로 호출된다. Swift에서는 2가지 타입이 있는데 willSet과 didSet이 있다.

#### willlSet

---

속성에 값이 할당되기 바로 전에 호출됩니다.

#### didSet

---

속성에 값이 할당된 직후에 호출됩니다.

```swift
import cocoa

class Person {
  var name : String?
  var height : Float?
  var weight : Float?
  
  init(name:String, height:Float, weight:Float){
    self.name = name
    self.height = height
    self.weight = weight
  }
  
  var bmi : Float = 0.0 {
    willSet(bmi) {
      print ("BMI 변수 호출됨 -> willSet")
    } didSet {
			print ("BMI 변수 호출됨 -> didSet")
  }
}
```



## Type Property

---

static 키워드를 사용하며 선언을 할 시 해당 클래스를 참조하는 모든 곳에서 해당 static 값에 접근이 가능해진다.

```swift
class Person {
  static var total : Int = 0
  
  class var halfTotal : Int {
    get {
      return total / 2
    } set (newValue) {
      total = newValue * 2
    }
  }
}

var ps1 = Person(name:"철수")
print("만들어진 사람 객체 수 -> \(Person.total)")

Person.halfTotal = 10
print("만들어진 사람 객체 수 -> \(Person.total)")
```





