i# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)
```
var rangeN = 1...10
var emptyString = ""
for i in rangeN {
emptyString += String(i)
}
print(emptyString)

```

## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

```
var rangeN = 5...51
var emptyString = ""

for i in rangeN where i % 2 == 0{
emptyString  += "\(i) "
}
print(emptyString)
```
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.
```
var rangeN = 1...60
var emptyString = ""

for i in rangeN where i % 10 == 4{
emptyString  += "\(i), "
}
print(emptyString)

```

## Question 4

Print each character in the string `"Hello world!"`
```
var stringN = "Hello world"
for c in stringN {
print(c)
}
```
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).
```
let myStringSeven = "Hello world!"

print(myStringSeven.last!)
```
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

```
var myString = "Fredlyne num 44"
var newString = ""

if myString.count % 2 == 0 {
print(myString)
}else {
for (a,b) in myString.enumerated() {
if a % 2 != 0 {
print(b)
}
}}
```
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

```var meOneOne: Character = "f"
(meOneOne == "f")
```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.
```
let precomposed: Character =   "\u{00CB}"
let decomposed: Character = "\u{0045}\u{0308}"
print(decomposed == precomposed)

let precomposed: Character = "\u{00CD}"
let decomposed: Character = "\u{0049}\u{0301}"
print(decomposed == precomposed)

let precomposed: Character = "\u{00D1}"
let decomposed: Character = "\u{004E}\u{0303}"
print(decomposed == precomposed)

let precomposed: Character =   "\u{00E5}"
let decomposed: Character = "\u{0061}\u{030A}"
print(decomposed == precomposed)

let precomposed: Character =   "\u{010d}"
let decomposed: Character = "\u{0063}\u{030c}"
print(decomposed == precomposed)
```
***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`
```
let pComp = "\u{0048}\u{0045}\u{004c}\u{004c}\u{004f} \u{0057}\u{004f}\u{0052}\u{004c}\u{0044}\u{01c3}"
print(pComp)
```
## Question 10

**Using only Unicode**, print out your name.
```
let myName = "\u{0046}\u{0052}\u{0045}\u{0044}\u{0044}\u{0049}"
print(myName)
```
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.
```
let myName = "\u{48}\u{4f}\u{4c}\u{41} \u{4d}\u{55}\u{4e}\u{44}\u{4f}"
print(myName)
```
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -

let outLine = String(repeating: "\u{2d} ", count: 11)
print(outLine)
let bodyGarden = String(repeating:"\u{2f} \u{2698} ", count: 5) + "\u{2f}"
var emptyString = ""
for _ in 1...7 {
print(bodyGarden)
}
print(outLine)

```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜

let rowWhBck = "\(wR) \(wKn) \(wB) \(wQ) \(wK) \(wB) \(wK) \(wR)"
print(rowWhBck)
let rowWhfrt = String(repeating: wP , count: 8)
print(rowWhfrt)
for _ in 1...5 {
print("")
}
let rowBlfrt = String(repeating: bP , count: 8)
print(rowBlfrt)
let rowBlBck = "\(bR) \(bKn) \(bB) \(bQ) \(bK) \(bB) \(bK) \(bR)"
print(rowBlBck)
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"*"`.

```swift
var aString = "Replace the letter e with *"
// var aString = "Replace the letter e with *"
print(aString.replacingOccurrences(of: "e", with: "*"))

or

var aString = "Replace the letter e with *"
var replacedString = ""
for scalar in aString.unicodeScalars {
let char = "\(scalar)"
if char == "e" {
replacedString = replacedString + "*"
} else {
replacedString = replacedString + char
}
}
print(replacedString)

 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var newReverse = ""

var aString = "this string has 29 characters"
var newReversed = ""
for l in aString {
newReversed = "\(l)" + newReversed
}
print(newReversed)
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// let aString = "anutforajaroftuna"
print(aString == String(aString.reversed()))

```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"


print(problem.replacingOccurrences(of:" ", with: "\n"))

```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// var problem = "find the longest word in the problem description"
var wordArray = problem.components(separatedBy: " ")
var maxWord = ""

for word in wordArray {
if word.count > maxWord.count {
maxWord = word
}
}
print(maxWord)
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift


let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"

var inputTuple = (a: "\(vowels.count)", b: "\(consonants.count)")
print(inputTuple)

// prints (a)
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

```
var myString = "How are you doing this Monday?"
var eachWord = myString.components(separatedBy: " ")

if eachWord.count > 0 {
print(eachWord.last!.count)
} else {
print("no last word")
}

```
***
