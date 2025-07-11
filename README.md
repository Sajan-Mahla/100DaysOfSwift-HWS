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

## 📆 Progress Tracker – Hacking With Swift (100 Days) (THIS WILL UPDATE EVERYDAY SO KEEP YOUR EYE THERE. STARTED FROM 3-7-25. GOING TO END WITH ME..)
| Day | Topic Covered                                   | Status               |
| --- | ----------------------------------------------- | -------------------- |
| 1   | Variables, Constants, Strings                   | ✅ Completed          |
| 2   | Ints, Doubles, Type Inference                   | ✅ Completed          |
| 3   | Arrays, Sets, Dictionaries Intro                | ✅ Completed          |
| 4   | Sets, Dictionaries, Enums                       | ✅ Completed          |
| 5   | `if` / `else`, `switch`, ternary operator       | ✅ Completed          |
| 6   | Loops (`for`, `while`, `repeat-while`)          | ✅ Completed          |
| 7   | Loop control (`break`, `continue`, loop labels) | ✅ Completed          |
| 8   | Functions (basic)                               | ✅ Completed           |
| 9   | Functions (parameters, return)                  | ⏳ Pending            |
| …   | …                                               | 🔒 Will Unlock Daily |





 
### 🔧 Extension Skills Tracker – Bonus Modules Alongside 100 Days

| #   | Skill / Topic                                              | Status        | Notes / Purpose                                                                 |
|-----|-------------------------------------------------------------|---------------|----------------------------------------------------------------------------------|
| 1   | Xcode Mastery                                               | ✅ Completed  | Installed, configured, breakpoints, build system                                |
| 2   | Git & GitHub Workflow                                       | ✅ Completed  | Daily commits, clean logs, Markdown usage                                       |
| 3   | Interview Preparation (Tech + HR)                           | 🟨 Ongoing    | Daily Q&A, real-case logic + Apple-style answers                                |
| 4   | UIKit Crash Course                                          | ✅ Completed  | Watched + Practiced setup + basic layout                                        |
| 5   | Asynchronous Programming (async/await, DispatchQueue)       | ⏳ Pending    | Will begin post-Day 10 (app building starts)                                    |
| 6   | AutoLayout & Interface Builder (Storyboard mastery)         | ⏳ Pending    | UIKit deep layout + constraints for custom UI                                   |
| 7   | App Store + Deployment Basics                               | ⏳ Pending    | Learn RouteNote, TestFlight, App Store Connect                                 |
| 8   | GitHub Readme + Branding                                    | ✅ Completed  | Clean Readme, branding, visual commitment                                      |
| 9   | Apple Careers / Office Research                             | ✅ Completed  | Researched Ottawa, Munich Apple offices                                        |
| 10  | Weekly App Challenge (Sunday builds)                        | 🔒 Starts Soon | One app every Sunday – scaling from simple to pro                              |
| 11  | **Soft Skills: Dev Communication & Tech Speak** 💬          | ✅ Completed  | Practiced Swift explanations, metaphors, interview-style answers 🔥             |
| 12  | **Swift Extension Superpowers** 🧩                           | ✅ Completed  | Created extensions for String & Int, explained purpose + real-world use         |











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
    
    else{
        print(i)
    }
    }
_____________________________________________________________________________
    

 
