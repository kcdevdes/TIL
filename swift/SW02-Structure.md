## Structure

---

클래스처럼 틀을 만들어 사용할 수 있는 또 다른 방법입니다. 키워드는 struct입니다.

```swift
struct Rectangle {
    var width = 0
    var height = 0
    
    func toString() -> String {
        return "width : \(width) || height : \(height)"
    }
}

var rect = Rectangle()
var rect2 = Rectangle(width:200, height: 200)

var desc = rect2.toString()
print(desc)
```

여기서 신기한 점은 var rect2 = Rectangle(width:200, height:200) 부분입니다. 클래스에서는 init함수(생성자)가 존재해야지만 가능하지만, struct는 memberwise 형식을 취하기 때문에 이러한 타입이 가능합니다

* 여러가지의 데이터를 묶는데 좋습니다.
* 상속이 필요없는 틀을 제작하는 데 좋습니다.

이러한 특징이 structure에 존재합니다.



## Enumeration(열거혐)

---

열거형은 데이터의 집합을 열거해둔 형태를 의미한다. C언어 Java에도 모두 존재하는 기능이다.

```swift
enum computerManufacturer : Int {
    case microsoft = 0
    case apple
    case hp
    
    var name : String {
        if self == .microsoft {
            return "MicroSoft"
        } else if self == .apple {
            return "Apple"
        } else {
            return "HP"
        }
    }
    
    func toString() -> String {
        return self.name
    }
}

var case1 = computerManufacturer.microsoft
print(case1.name)

var case2 = computerManufacturer.apple
print(case2.name)

```

Enum 형이 다른 언어에 비해 상당히 폭 넓게 활용이 되는 것을 알 수 있다.

