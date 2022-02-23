REGEX: matching an email made easy

The purpose of this tutorial is to provide a breakdown of various regex expressions to help you with disecting these expressions for yourself and eventually using them in your own future code.

## Summary

The email matching Regex is useful in many cases. The main purpose of such regular expression is for validation of emails, to ensure that such an address can be used to contact the individual to whom it belongs.

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Author](#author)

## Regex Components

### Anchors

- An Anchor is a used to begin and end a string. in this case everything within the regex's ^ and $ anchors is applied to a singular email
- If you noticed additionally the '@' symbol is present in the regular expression, this is used to assure that following the initial conditions within the first set of brackets we see an @ symbol to verify that it is infact in complacency with our email standards.

### Quantifiers

- Quantifiers have a simple purpose. Match strings that fit the quantifiers alphabetical range. In all 3 instances that we see the ranges in the email regex our range is from a-z, meaning any letter of the alphabet is available for use in the email
- following the first capturing group we see a '+' symbol, this is used to match one or more of the preceding conditions we have specified in the capturing group (this is where the matching part comes in)
- In the end of the regex the final capturing group has {2,3} written just outside of the square brackets/ this is essentially meant to put a range on the length of that specific capturing group from a minimum of 2 characters to a maximum of 6

### Character Classes

- We're given a range in our first capturing group and it's 0-9. the purpose of this is to limit a user to an email address that can only be 9 characters long before the @ and email tag
- In the email regex we are also allowing for the use of characters such as and underscore (\_), and a dash (-) in the first capturing group. And a dash (-) in the second capturing group. The last capturing group cannot have additional characters because, as with all emails the last capturing group is always .com, .ca .org or .gov. Neither of these instances have any other characters.
- You may have also noticed a strange backslash followed by a dot, that is the reserved character symbol. The backslash is used to give new meaning to any character that follows it. In this case the backslash followed by the dot matches any character except for the newline symbol.
- the \d symbol is a digit character class used to match any digit character from a range of (0-9)

## Author

Vladimir Starchenko is a 19 year old coder who loves to learn more about the languages that make up the internet. He hopes to one day be working as full stack web developer preferably in Florida 😊.

Vladimir's Github: [Vladimir Starchenko's Github](#https://github.com/VladimirStarchenko)
