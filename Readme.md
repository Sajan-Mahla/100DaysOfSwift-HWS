# 100DaysOfSwift-HWS

---

## 🛠 Tech Stack

- **Swift** – Core language  
- **Xcode** – Development IDE  
- **Git + GitHub** – Version control & public progress  
- **Markdown** – Clean daily logs

---

## 🙏 Special Thanks

- [Paul Hudson](https://www.hackingwithswift.com) for the amazing HWS course  
- Everyone cheering for me silently 🫶  
- Myself, for not giving up

---

## 📌 Final Note

This is more than a repo — it’s my **proof of discipline**.  
If you’re reading this and hustling too — keep going.  
**"We don’t do it in one day. We do it every day."**

📆 Progress Tracker – Hacking With Swift (100 Days)  
**(THIS WILL UPDATE EVERYDAY SO KEEP YOUR EYE THERE. STARTED FROM 3-7-25. GOING TO END WITH ME..)**



| Day | Status    | Notes                       |
|-----|-----------|-----------------------------|
| 1   | ✅ Done    | Basics covered              |
| 2   | ✅ Done    | Strings & Integers          |
| 3   | ✅ Done    | Arrays, Dictionaries, Sets  |
| 4   | ✅ Done    | Loops                       |
| 5   | ✅ Done    | Conditions                  |
| 6   | ✅ Done    | Switch & Ternary            |
| 7   | ✅ Done    | Functions                   |
| 8   | ✅ Done    | Default + Throwing          |
| 9   | ⏳ Pending | (App Sunday - Quote App)    |
| 10  | ✅ Done    | Classes & Objects           |
| 11  | ✅ Done    | Access Control + Static     |
| 12  | ✅ Done    | Structs Review (Your Notes) |






 
🚀 Extension Skill Tracker – Leveling Beyond Swift  
**(One hour daily commitment outside HWS. Builds real dev superpowers.)**

| Skill Area           | Topics Covered                                  | Status        | Notes                        |
|----------------------|--------------------------------------------------|----------------|-------------------------------|
| 1. Async Engineering | DispatchQueue, async/await, URLSession           | 🟢 In Progress | On Day 5                      |
| 2. UIKit             | Views, constraints, view controllers             | 🔜 Upcoming    | After Quote App v2            |
| 3. Git + GitHub      | Commits, branches, README, issues                | ✅ Completed   | Actively used daily           |
| 4. Xcode Debugging   | Breakpoints, logs, runtime analysis              | ✅ Completed   | Covered in UIKit crash course |
| 5. App Architecture  | MVC, MVVM basics                                 | 🔜 Upcoming    | Start after UIKit             |
| 6. Networking        | REST APIs, Codable, JSON decoding                | 🟢 In Progress | Quote App uses API            |
| 7. Swift Packages    | Using and creating SwiftPM packages              | ⏳ Pending     | Needed for scaling projects   |
| 8. Design Systems    | Apple HIG, light/dark mode, fonts, spacing       | ✅ Completed   | Used in Quote App             |
| 9. Firebase Basics   | Auth, Firestore, real-time updates               | 🔜 Upcoming    | Planned for future apps       |
| 10. App Store Prep   | Certificates, provisioning, TestFlight, upload   | ✅ Completed   | Watched video 07/09/2025      |










CHECKPOINT CODES 
Sat-5-july-2025
Q1 Your goal is to write a Swift playground that:

Creates a constant holding any temperature in Celsius.
Converts it to Fahrenheit by multiplying by 9, dividing by 5, then adding 32.
Prints the result for the user, showing both the Celsius and Fahrenheit values.



MY ANSWER: let Celsius = 30
var Fahrenheit = (Celsius * 9/5) + 32
print("it \(Celsius)° Celsius and \(Fahrenheit)° Fahrenheit")
____________________________________________________________________________
tue-8-july-2025
Q2 Create an array of strings, then write some code that prints the number of items in the array and also the number of unique items in the array.





MY ANSWER: var arr: Array = ["Sajan", "Mahla", "Harsimranjeet", "Sam","Sajan", "Mahla", "Harsimranjeet", "Sam",]
print(arr.count)
var uS = Set(arr)
print(uS)

here uS mean UniquesSet

_____________________________________________________________________________
thu-10-July-2025
Q3 The problem is called fizz buzz, and has been used in job interviews, university entrance tests, and more for as long as I can remember. Your goal is to loop from 1 through 100, and for each number:

If it’s a multiple of 3, print “Fizz”
If it’s a multiple of 5, print “Buzz”
If it’s a multiple of 3 and 5, print “FizzBuzz”
Otherwise, just print the number.


My ANSWER: for i in 1..<100{
    for i in 1..<100 {
    if i.isMultiple(of:3) && i.isMultiple(of: 5){
        print("\(i) is FizzBuzz")
    }
    else if i.isMultiple(of: 3){
        print("\(i) is Fizz")
    }
    else if i.isMultiple(of: 5){
        print("\(i) is Buzz")
    }
    else { print(i)
    }
    }
    }
_____________________________________________________________________________
Sat-12-july-2025
Q4 The challenge is this: write a function that accepts an integer from 1 through 10,000, and returns the integer square root of that number. That sounds easy, but there are some catches:

You can’t use Swift’s built-in sqrt() function or similar – you need to find the square root yourself.
If the number is less than 1 or greater than 10,000 you should throw an “out of bounds” error.
You should only consider integer square roots – don’t worry about the square root of 3 being 1.732, for example.
If you can’t find the square root, throw a “no root” error.


MY ANSWER: import UIKit




// 1. Define possible errors
enum RootError: Error, CustomStringConvertible {
    case outOfBounds
    case noRoot
    
    var description: String {
        switch self {
        case .outOfBounds: return "🚫 Number must be between 1 and 10,000."
        case .noRoot: return "❌ No integer square root found."
        }
    }
}

// 2. Function to calculate integer square root
func integerSquareRoot(of number: Int) throws -> Int {
    guard number >= 1 && number <= 10_000 else {
        throw RootError.outOfBounds
    }

    for i in 1...number {
        if i * i == number {
            return i
        } else if i * i > number {
            break
        }
    }
    
    throw RootError.noRoot
}

// 3. Try calling it and handle errors
do {
    let result = try integerSquareRoot(of: 10000)
    print("✅ Square root is \(result)")
} catch let error as RootError {
    print(error.description)
}

___________________________________________________________________________________
Mon-14-july-2025
Q5.Your input is this:

let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]
Your job is to:

Filter out any numbers that are even
Sort the array in ascending order
Map them to strings in the format “7 is a lucky number”
Print the resulting array, one item per line
So, your output should be as follows:

7 is a lucky number
15 is a lucky number
21 is a lucky number
31 is a lucky number
33 is a lucky number
49 is a lucky number



MyAnswer:let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]

let result = luckyNumbers
    .filter { $0 % 2 != 0 }
    .sorted()
    .map { "\($0) is a lucky number" }

for line in result {
    print(line)
}

___________________________________________________________________________________
 Wed-16-7-2025
 Q6. create a struct to store information about a car, including its model, number of seats, and current gear, then add a method to change gears up or down. Have a think about variables and access control: what data should be a variable rather than a constant, and what data should be exposed publicly? Should the gear-changing method validate its input somehow?

 MyAnswer: struct CarModel {
    enum Gear: Int {
        case reverse = -1, neutral, first, second, third, fourth, fifth, sixth
    }

    let name: String
    let model: String
    let seats: Int
    private(set) var currentGear: Gear = .neutral

    mutating func shiftUp() {
        if let next = Gear(rawValue: currentGear.rawValue + 1) {
            currentGear = next
        }
    }

    mutating func shiftDown() {
        if let prev = Gear(rawValue: currentGear.rawValue - 1) {
            currentGear = prev
        }
    }
}
var myCar = CarModel(name: "Tesla", model: "Model S", seats: 5)
print(myCar.currentGear)   // neutral

___________________________________________________________________________________
Thu 17-7-2025
Q7. make a class hierarchy for animals, starting with Animal at the top, then Dog and Cat as subclasses, then Corgi and Poodle as subclasses of Dog, and Persian and Lion as subclasses of Cat.

But there’s more:

The Animal class should have a legs integer property that tracks how many legs the animal has.
The Dog class should have a speak() method that prints a generic dog barking string, but each of the subclasses should print something slightly different.
The Cat class should have a matching speak() method, again with each subclass printing something different.
The Cat class should have an isTame Boolean property, provided using an initializer.

 MyAnswer: class Animal {
    var legs: Int

    init(legs: Int) {
        self.legs = legs
    }
}


class Dog: Animal {
    func speak() {
        print("Generic dog bark!")
    }

    init() {
        super.init(legs: 4)
    }
}

class Corgi: Dog {
    override func speak() {
        print("Corgi goes: Yap yap!")
    }
}

class Poodle: Dog {
    override func speak() {
        print("Poodle goes: Fancy bark!")
    }
}


class Cat: Animal {
    var isTame: Bool

    init(legs: Int = 4, isTame: Bool) {
        self.isTame = isTame
        super.init(legs: legs)
    }

    func speak() {
        print("Generic cat sound.")
    }
}

class Persian: Cat {
    override func speak() {
        print("Persian goes: Purrrrr~")
    }
}

class Lion: Cat {
    override func speak() {
        print("Lion roars: ROARRRR!")
    }
}


TBH THIS TOOK 1 HOUR TO SOLVE 😭
___________________________________________________________________________________
