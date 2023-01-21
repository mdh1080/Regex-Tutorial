# Regex Tutorial
Regex or regular expressions are a sequence of characters used to define a search pattern. They can be used to search and edit data. This tutorial will explain the components of a regex using an email address for an example.

## Summary
The regex used in this tutorial is for an email address. The regex is as follows:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Escape Characters](#escape-characters)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
A regex always begins and ends with the / character. All characters, except those having special meaning in regex, matches itself. In this email address example, the @ matches "@". The components of this regex email address example are anchors, quantifiers, character classes, bracket expressions, escape characters, grouping and capturing, and greedy matches.

### Anchors
The characters ^ and $ are anchors. The ^ character begins the string. In this case, the ^ signifies a range of possible matches due to the brackets which follow it. 
The $ character ends the string. Like the ^ character, the $ character signifies a range of possible matches due to the brackets which precede it. The ^ string must be at the beginning of the email address and the final string preceded by $ must be at the end of the email address. These characters can also be  used as boundaries. 

### Quantifiers
Quantifiers are used to specify how many times a character or group of characters can be repeated. In this example, the quantifiers are + and {2,6}. Within the parenthesis is the + character seen here ([a-z0-9_\.-]+) and ([\da-z\.-]+). The + after the brackets means the characters within the brackets can be matched 1 or more times. There can be unlimited multiples of characters as long as the characters are allowed within the brackets.
The {2,6} in the email example is within the last parenthesis; ([a-z\.]{2,6}). The curly brackets around 2,6 or {2,6} mean that the precending pattern, in this case, [a-z\.] must have at least 2 character matches, but no more than 6 characters. Any characters allowed within the brackets count as a match. It doesn't have to be the exact same characters. For instance, "aa" would be a match, but so would "ab". 

### Character Classes
A character class is a set of characters to be matched. A character class matches any one of the enclosed characters. You can specify a range of characters by using a hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character. In this example, the character classes include the following:
  a-z = any lowercase letter from a to z
  0-9 = any number from 0 to 9

### Bracket Expressions
This email code contains 3 bracket expressions. The characters for bracket expressions are []. The brackets contain characters that are wanted in the email address. This is also known as a positive character group. 
The first bracket expression is [a-z0-9_\.-]. Within the brackets are a-z representing any lowercase letter from a to z, 0-9 representing any number from 0 to 9, and the special characters _, ., and - mean that those characters can be included. 
The second set of brackets is [\da-z\.-]. Inside these brackets are \d which has the same meaning as 0-9 which represents any number 0-9. Next is a-z, meaning any lowercase letter in the alphabet. And special characters . and - which are literal matches. Note that the - character is literal in this case because it is the last character within the brackets.
The last set of brackets is [a-z\.]. Within the brackets, a-z mean any lowercase letter. Followed by the special character   ".". Any or all of these characters will be searched for in the email address. So it could include just one of the characters or all of the characters. See below for the meaning of the backslash "\".

### Escape Characters
The escape character is the backslash  or \. The backslash is used to escape characters that would otherwise be interpreted as a special character. In this example, the backslash is used as an escape 4 times. All used as "\.". This means that the period or "." is a match. The \ does not match in this case and is used only as an escape character. The \ within the brackets are listed above for this email address. In between that last 2 parenthesis is another \. meaning a period will be matched in between these sets of characters. 

### Grouping and Capturing
The parenthesis or () are used to group characters within an expression. This is known as a subexpression. The subexpression looks for an exact match. In this email address there are 3 sets of parenthesis. All are surrounding a bracket expression. The first ([a-z0-9_\.-]+) and second ([\da-z\.-]+) set both have the character + within the parenthesis, but outside the brackets. The + meaning was discussed in the quantifier section.  
The third parenthesis is ([a-z\.]{2,6}). The {2,6} is outside of the brackets, but within the parenthesis. This meaning was also discussed in the quantifiers section. 

### Greedy and Lazy Match
The repetition operators are greedy operators, and by default grasp as many characters as possible for a match. In this email address the greedy operators are the + and {2,6}. 
Lazy operators are the opposite. They match as few characters as possible. In this example there are no lazy operators. 

## Author
Megan Stanton is a beginner coder. She is learning to code in the full-stack web development program at UNC Chapel Hill.   
