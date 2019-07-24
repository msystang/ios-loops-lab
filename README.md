# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1 DONE

Write code that prints all the numbers from 1 to 150, **inclusive.**

Answer:
```swift
let range = 1...150

for i in range {
print(i)
}
```

***
## Question 2 DONE

Write code that prints all the numbers from 142 to 159, **exclusive.**

Answer:
```swift
let range = 142..<159

for i in range {
print(i)
}
```

***
## Question 3 DONE

Write code that prints only the even numbers from 15 to 80, **inclusive.**

Answer:
```swift
let range = 15...80

for number in range where number % 2 == 0 {
print(number)
}
```

***
## Question 4 DONE

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

Answer:
```swift
let range = 19...51

for number in range where number % 2 == 1 {
print(number)
}
```

***
## Question 5 DONE

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

Answer:
```swift
let range = 1..<100

for number in range where number % 10 == 5 {
print(number)
}
```

***
## Question 6 DONE

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

Answer:
```swift
let range = 1...40

for number in range where number % 10 == 7 {
print(number)
}
```

***
## Question 7 DONE

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`

Answer:
```swift
let range = 20...150

for number in range where number % 3 == 0 {
print(number)
}
```

***
## Question 8 DONE

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

Answer:
```swift
let range = 20...150

for number in range where number % 3 == 0 && number % 2 == 0 {
print(number)
}
```

***
## Question 9 DONE

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

Answer:
```swift
let range = 20...150

for number in range where number % 10 == 4 {
print(number)
}
```

***
## Question 10 DONE

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

Answer:
```swift
let range = 20...150

for i in range where i == 31 || i == 35 || (i >= 40 && i <= 60) {
print(i)
}
```

***
## Question 11 DONE

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
```
Answer:
The loop will run indefinitely. The while loop condition indicates that the variable "i" must be greater than 3 to run. The variable "i" starts at 5 and is greater than 3, so it will initiate the while loop. Since the operation "i += 1" continues to add 1 to "i", the variable will always be larger than 3 and will continue to run indefinitely.


***
## Question 12 DONE

Change the code below to make the loop stop executing when it reaches 9.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```

Answer:
```swift
var i = 5

while (i > 3) && (i <= 9) {
print(i)
i += 1
}
```

***
## Question 13 DONE

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i > 3) {
    i += 1
}
```

Answer:
```swift
var i = 5
var counter = 0

while (i > 3) && (counter < 1000) {
counter += 1
i += 1
print(i)
}
```

***
## Question 14 DONE

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i > 3) {
    i += 1
}
```

Answer:
```swift
var i = 5
var counter = 0

while (i > 3) && (counter < 1000) {
counter += 1
i += 1
if i % 2 == 0 {
print(i)
}
}
```

***
## Question 15 DONE

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10
```
Answer: 
Loop one uses a while loop stating that while the variable "i" is less than or equal to 10, it will print the string with string interpolation "i = \(i)" and loops the operation "i += 1". The output will print on loop until i = 10. Loop two uses a repeat loop with a while condition indicating that the loop repeats printing "i = \(i)" the the operation "i += 1". The while condition indicates that the repeat loop runs as long as i is less than or equal to 10. Both loops will produce the same output because both are loops that increase i by 1, the conditions that i is less than or equal to 10 is the same, and the printed language remains the same.

***
## Question 16 DONE

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

Answer:
A break statement completely stops a loop or switch statement if the break statement condition is met. A continue statement will stop a statement within a loop or switch statement but will continue to run the loop or switch statements for other conditions after the continue statement.

```swift
// Example of a break statement:
var breakAtSix = 2

for numInRange in 1...10 {
if numInRange == 6 {
break
} else {
breakAtSix += numInRange
}
}

// Example of a continue statement:
for iDontWantFour in 1...5 {
if iDontWantFour == 4 {
continue
}
print("This number is not 4: \(iDontWantFour).")
}

```


***
## Question 17 DONE

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```

[]1
[]2
[]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10


Answer: 
1, 2, 3, 8, 9, 10
***
## Question 18 DONE

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[]1
[]2
[]3
[]4
[]5
[]6
[]7
[]8
[]9
[]10

Answer: 
1, 2, 3

***
## Question 19 DONE

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}

```
Answer:
x = 1, y = 1
x = 2, y = 1
x = 3, y = 1

For x = 1 in the outerloop, the innerloop assigns y = 1 then prints "x = \(x), y = \(y)", which is x = 1, y = 1. The program runs in the next number in the range for the innerloop while x is still 1. Since y = 2, the program continues (stops running after the continue) and returns back to the start of the program where the outerloop is x = 2 and the innerloop where y = 1 and prints "x = \(x), y = \(y)", which is x = 2, y = 1. Since y = 2 again within x = 2, the program continues and goes back to the outerloop where x = 3. The program goes into the innerloop, assigning y = 1, and  prints "x = \(x), y = \(y)", which is x = 3, y = 1. The program continues at y = 2 but since the range ends at 3, the program stops.


***
## Question 20 DONE

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

Answer:
```swift
let range = 0...10

outer: for x in range {
inner: for y in range {
print("(\(x),\(y))", terminator:" ")
}
print("")
}

//or using tuples
let range = 0...10

for x in range {
for y in range {
let tuple = (x,y)
print(tuple)
}
}
```

***
## Question 21 DONE

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

Answer:
```swift
let range = 0...10

outerloop: for x in range {
innerloop: for y in range {
if abs(y - x) < 5 {
continue outerloop
}
print("(\(x), \(y))")
}
}
```

***
## Question 22 DONE

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25
```

Answer:
```swift
var N = 5
let range = 1...N

for squareNum in range {
print(squareNum*squareNum)

}
```

***
## Question 23 DONE

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

Answer:
```swift
var N = 3

let numberOfRows = 1...N
let numberofColumns = 1...N

outer: for _ in numberOfRows {
inner: for _ in numberofColumns {
print("*", separator:"", terminator: " ")
}
print("") //new line
}
```

***
