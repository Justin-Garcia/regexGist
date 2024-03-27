# Regex Guidebook

Welcome to your RegEx guidebook to understanding the properties that go into matching a hex value. 

## Summary
What is RegEx? Simply put, it defines an object used to describe a pattern of characters. This object can then be used to pattern match, validate, search and more. 

Suppose we want to match hex codes like "1A2B3C" or "FF00FF". We can use the regular expression /^[0-9A-Fa-f]+$/.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
 We use ^ to indicate the start of the string and $ to indicate the end. For example:

/^hello/ matches strings that start with "hello".
/world$/ matches strings that end with "world".

### OR Operators
We use | to indicate "OR". For example:

/apple|banana/ matches either "apple" or "banana".

### Character Classes
We use brackets [ ] to specify a group of characters. For example:

/[aeiou]/ matches any vowel.
/[0-9]/ matches any digit.

### Flags
We can add flags like i for case-insensitive matching. For example:

/hello/i matches "hello", "Hello", "HELLO", etc.

### Grouping and Capturing
We use parentheses ( ) to group parts of the regex. For example:

/apple(s|d)?/ matches "apple", "apples", or "appled".

### Bracket Expressions
We use brackets [ ] to specify a range of characters. For example:

/[0-9]/ matches any digit.
/[a-zA-Z]/ matches any letter, regardless of case.

### Greedy and Lazy Match 
By default, regex is greedy, but we can make it lazy by adding ?. For example:

/a+/ matches one or more "a" characters greedily.
/a+?/ matches one or more "a" characters lazily.

### Boundaries
We use \b for word boundaries. For example:

/\bword\b/ matches "word" but not "words" or "sword".

### Back-References 
We use \1, \2, etc., to reference captured groups. For example:

/(a+) \1/ matches "aa", "aaa", etc.

### Look-Ahead and Look-Behind
We use (?= ) for look-ahead and (?<= ) for look-behind. For example:

/apple(?=pie)/ matches "apple" only if it's followed by "pie".
/(?<=\d)kg/ matches "kg" only if it's preceded by a digit.

## Author
GitHub: https://github.com/Justin-Garcia