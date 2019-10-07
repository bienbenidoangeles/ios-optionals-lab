# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"
```

My code:

```swift
var userNameOne: String? = "Test User"
if let validString = userNameOne {
    print("The username is \(validString)")
} else {
    print("String, \(userNameOne), is unvailable")
}
```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil
```

My code:
```swift
var userNameTwo: String? = nil
print(userNameTwo ?? "the username is undefined")
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
```
```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
if let validDoubleWidth = rectOneWidth, let validDoubleHeight = rectOneHeight {
    print("The area of rectOne is: \(validDoubleWidth * validDoubleHeight)")
} else {
    print("The area of rectOne is unavailble")
}
```


b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
```

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil

if let validDoubleWidth = rectTwoWidth, let validDoubleHeight = rectTwoHeight {
    print("The area of rectTwo is: \(validDoubleWidth * validDoubleHeight)")
} else {
    print("The area of rectTwo is not able to be calculated")
}
```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
```

My code:
```swift
 var userOneName: String? = "Anne"
 var userOneAge: Int? = 15
 var userOneHeight: Double? = 70

 if let validName = userOneName, let validAge = userOneAge, let validHeight = userOneHeight {
     print("Hello \(validName)!  You are \(validAge) years old and \(validHeight/12) feet tall")
 }
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
```
My code:
```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil

if let validName = userTwoName, let validAge = userTwoAge, let validHeight = userTwoHeight {
    print("Hello \(validName)!  You are \(validAge) years old and \(validHeight/12) feet tall")
} else if let validAge = userTwoAge{
    print("Hello user!  You are \(validAge) years old and I don't know how tall you are")
}
```

## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
```
My code:
```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil

if let validFavNum = favoriteNumber {
    print("Your favorite number is \(validFavNum)")
} else {
    print("I don't know what your favorite number is")
}
```

## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil

let sum = (numOne ?? 0) + (numTwo ?? 0) + (numThree ?? 0)
print("The sum is: \(sum)")
```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```

My code:
```swift
var numbers1 = [Int?]()
var sum1 = 0

for _ in 0..<10 {
    numbers1.append(Bool.random() ? Int.random(in: 0...100) : nil)
}

for num in numbers1 {
    sum1 += num ?? 0
}

print("The sum of all numbers is: \(sum1)")

```

b. Using the same variable, find the average of all non-nil values.

My code:
```swift
var numbers1 = [Int?]()
var sum1 = 0
var iterations = 0

for _ in 0..<10 {
    numbers1.append(Bool.random() ? Int.random(in: 0...100) : nil)
}

for num in numbers1 {
    sum1 += num ?? 0
    iterations += 1
}

let avg1 = sum1 / iterations
print("The average of all numbers is: \(avg1)")
```

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
