# Regex-Tutorial

Hello, my name is Omar and today we will be breaking down a Regular Expression Pattern, or Regex for short, to better understand the purpose of utilizing the code structure to 
break patterns or matches within strings so that we can better regulate data coming within our database or moving throughout the internet! 

## Summary

The choice for todays Regex tutorial is going to be one that matches an email to ensure that there is upper or lower case characters within the string, '@' symbol, email of choice (gmail), and .com to end the string. 

The Regex Pattern is as follows:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components
Regex is considered a literal statement to break down a string but there a specific components of Regex that allow us to dissect a pattern! The list as follows:

1. Anchors
2. Quantifiers 
3. Grouping Constructs
4. Bracket Expressions
5. Character Classes
6. The OR Operator
7. Flags

### Anchors
Anchors component of Regex is represented by '^' and '$'!

'^' signifies a string that begins with the characters that follow. 

'$' signifies the end the check of the string of characters.

Essentially A regex starts with ^ and ends with $.

### Quantifiers

Quantifiers are responsible for setting a limit of the string that your regex matches.
There are different quantifiers that represent different outcomes. 

* - Matches the pattern zero or more times

+ - Matches the pattern one or more times

? - Matches the patter zero or one times

{} - can provide three different ways to set limits for string match

    1. {n } | Matches the pattern exactly [n] number of times

    2. {n, } | Matches the pattern at least [n] number of times

    3. {n, x} | Matches the pattern from a minimum of n times and maximum of x times

For our example we quantify the characters of the string 2 to 6 times! 

While in between each check we do the search one time!

### Grouping Constructs

You would group different subsections of the regex for a check for different parts of the string!

Since for our case we are checking for different aspects of an email to ensure that it contains characteristics of emails we would use the () to create subexpressions
such as: 

'([a-z0-9_\.-]+)' '([\da-z\.-]+)' '([a-z\.]{2,6})'

There are two aspects of grouping constructs capturing and non-capturing!
Capturing means to capture the matched character sequence for possible re use. 
Non-capturing essentially does the opposite and can be instantiated with '?:' a common use of this concept would be for matching URL for the 'https' since you only wanna capture it once

### Bracket Expressions

Anything within the [] bracket represents a range of characters that we want to match. We would than utilize a letter, number, or special characters follow by a hyphen to check the string for a value between that range. 

In our example that could be seen as: [a-z] (check for a range of characters in the alphabet) or [0-9] (checks for range of numbers from 0-9) [_-] (checks for hyphens or underscores)

Initially bracket expressions are positive character groups but can bet turned into a negative character group by implement a ^ within the bracket expression [^].

### Character Classes

Character classes define a set of characters, any one of which can occur in an input string to fulfill a match. 

For example some character classes are as follows: 

- . | Matches any character except the newline character (\n)
- \d | Match any arabic numeral digit (equivalent fo the bracket expression [0-9])
- \w | Matches any alphanumeric character from the basic Latin alphabet, including underscore (_). Class equivalent to the bracket expression [A-Za-z0-9_].
- \s | Matches a single whitespace character, including tabs and line breaks. 

In our example Character classes can be represented within the second subsection ([\da-z\.-]+).

### The OR Operator

The OR operator allows you to add same logic inside the bracket expression to the outside. Works best with grouping construct or between two different grouping constructs.

You use the '|' expression to use the OR operator for example (a|b|c)

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for regex.
There are 6 operational flags but the most commonly used ones are as follows:

- g | Global Search: the regex should be tested against all possible matches in a string.

- i | Case-insensitive search: case should be ignored while attempting a match in a string. 

- m | Multi-line search: a multi-line input string should be treated as multiple lines.

### Character Escapes

By utilizing the '\' you allow the regex to force the component to escape rather than be interpreted literally. 
Commonly used when looking for strings with special characters that are the same as a particular component of a regex.  

## Author

[Github Profile](https://github.com/omousa98)

