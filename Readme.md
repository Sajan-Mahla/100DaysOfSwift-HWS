# 🚀 100 Days of Swift – Hacking with Swift

Welcome to my personal journey through the **#100DaysOfSwift** challenge by [Paul Hudson](https://www.hackingwithswift.com). This repository is my public commitment to becoming a top-tier iOS developer.

---

## 🛠 Tech Stack

* **Swift** – Core language
* **Xcode** – Development IDE
* **Git + GitHub** – Version control & daily logging
* **Markdown** – For readable progress tracking

---

## 🙏 Special Thanks

* [Paul Hudson](https://www.hackingwithswift.com) – for building this course and community ❤️
* Everyone silently cheering me on 🫶
* Me – for not giving up when it got tough 💪

---

## 📌 Why This Repo Matters

This is more than just code. It’s my **proof of discipline**.
Every day, one step closer to mastery.

> **"We don’t do it in one day. We do it every day."**

📆 Started on: **3rd July 2025**
🎯 Ending with: **a better version of me**
📍 *This README updates daily — stay tuned!*

---

## ✅ Daily Progress Tracker

| Day | Status    | Notes                      |
| --- | --------- | -------------------------- |
| 1   | ✅ Done    | Basics covered             |
| 2   | ✅ Done    | Strings & Integers         |
| 3   | ✅ Done    | Arrays, Dictionaries, Sets |
| 4   | ✅ Done    | Loops                      |
| 5   | ✅ Done    | Conditions                 |
| 6   | ✅ Done    | Switch & Ternary           |
| 7   | ✅ Done    | Functions                  |
| 8   | ✅ Done    | Default + Throwing         |
| 9   | ⏳ Pending | App Sunday: Quote App      |
| 10  | ✅ Done    | Classes & Objects          |
| 11  | ✅ Done    | Access Control + Static    |
| 12  | ✅ Done    | Structs Review             |

---

## 🧠 Extension Skills Tracker

> *1 hour/day outside HWS. Focused on real-world, interview-ready dev skills.*

| Skill Area        | Topics Covered                                 | Status         | Notes                         |
| ----------------- | ---------------------------------------------- | -------------- | ----------------------------- |
| Async Engineering | DispatchQueue, async/await, URLSession         | 🟢 In Progress | On Day 5                      |
| UIKit             | Views, constraints, view controllers           | 🔜 Upcoming    | After Quote App v2            |
| Git + GitHub      | Commits, branches, README, issues              | ✅ Completed    | Actively used daily           |
| Xcode Debugging   | Breakpoints, logs, runtime analysis            | ✅ Completed    | Covered in UIKit crash course |
| App Architecture  | MVC, MVVM basics                               | 🔜 Upcoming    | Start after UIKit             |
| Networking        | REST APIs, Codable, JSON decoding              | 🟢 In Progress | Quote App uses API            |
| Swift Packages    | Using and creating SwiftPM packages            | ⏳ Pending      | Needed for scaling projects   |
| Design Systems    | Apple HIG, light/dark mode, fonts, spacing     | ✅ Completed    | Used in Quote App             |
| Firebase Basics   | Auth, Firestore, real-time updates             | 🔜 Upcoming    | Planned for future apps       |
| App Store Prep    | Certificates, provisioning, TestFlight, upload | ✅ Completed    | Video watched 07/09/2025      |

---

## 🧪 Weekly Checkpoint Challenges

Each challenge helped sharpen my Swift knowledge:

### ✅ Q1 – Temperature Converter (5 July 2025)

```swift
let celsius = 30
let fahrenheit = (celsius * 9/5) + 32
print("\(celsius)°C is \(fahrenheit)°F")
```

### ✅ Q2 – Unique Array Count (8 July 2025)

```swift
let arr = ["Sajan", "Mahla", "Harsimranjeet", "Sam", "Sajan"]
let unique = Set(arr)
print("Total: \(arr.count), Unique: \(unique.count)")
```

### ✅ Q3 – FizzBuzz (10 July 2025)

```swift
for i in 1...100 {
    if i % 15 == 0 {
        print("\(i) is FizzBuzz")
    } else if i % 3 == 0 {
        print("\(i) is Fizz")
    } else if i % 5 == 0 {
        print("\(i) is Buzz")
    } else {
        print(i)
    }
}
```

### ✅ Q4 – Square Root with Error Handling (12 July 2025)

```swift
enum RootError: Error {
    case outOfBounds, noRoot
}

func integerSquareRoot(of number: Int) throws -> Int {
    guard number >= 1 && number <= 10_000 else { throw RootError.outOfBounds }
    for i in 1...number {
        if i * i == number { return i }
        if i * i > number { break }
    }
    throw RootError.noRoot
}
```

### ✅ Q5 – Lucky Numbers (14 July 2025)

```swift
let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]
let result = luckyNumbers.filter { $0 % 2 != 0 }.sorted().map { "\($0) is a lucky number" }
result.forEach { print($0) }
```

### ✅ Q6 – Car Model Struct (16 July 2025)

```swift
struct CarModel {
    enum Gear: Int { case reverse = -1, neutral, first, second, third, fourth, fifth, sixth }
    let name, model: String
    let seats: Int
    private(set) var currentGear: Gear = .neutral

    mutating func shiftUp() { currentGear = Gear(rawValue: currentGear.rawValue + 1) ?? currentGear }
    mutating func shiftDown() { currentGear = Gear(rawValue: currentGear.rawValue - 1) ?? currentGear }
}
```

### ✅ Q7 – Animal Class Hierarchy (17 July 2025)

```swift
class Animal { var legs: Int; init(legs: Int) { self.legs = legs } }
class Dog: Animal {
    func speak() { print("Dog barks") }
    init() { super.init(legs: 4) }
}
class Corgi: Dog { override func speak() { print("Yap yap") } }
class Cat: Animal {
    var isTame: Bool
    init(isTame: Bool) { self.isTame = isTame; super.init(legs: 4) }
    func speak() { print("Meow") }
}
```

### ✅ Q8 – Building Protocol (18 July 2025)

```swift
protocol Building {
    var rooms: Int { get }
    var buildingCost: Int { get }
    var agent: String { get }
    func buildingDescription() -> String
}

extension Building {
    func buildingDescription() -> String {
        return "\(rooms) rooms – $\(buildingCost), sold by \(agent)"
    }
}

struct House: Building { var rooms: Int; var buildingCost: Int; var agent: String }
struct Office: Building { var rooms: Int; var buildingCost: Int; var agent: String }
```

---

## 🧠 Final Reflection

> "A small-town boy wants to be heard, not to be herded."

From a second-hand laptop to chasing Apple-level dreams — this repo is my loud answer to the world: **I’m here. And I’m building.**

Feel free to ⭐ star the repo if it inspired you, or fork it to begin your own journey.

---

**Built with ❤️ by Harsimran Jeet Singh Mahla**
\[📍 Faridkot, Punjab – LPU CSE Student]

---

🍏 Let’s build apps. Let’s build ourselves.
