# Email matching regular expressions

Regex, or 'regular expression', is a sequence of characters that specifies a search pattern within text. These are typically used by searching algorithms to 'find' or 'find and replace' text. You will typically find regular expressions in search engines used to narrow down searches in a more timely fashion.

## Summary

This document will explain the basics of email matching regular expressions. With this knowledge, you can continue research and learn about the intricacies of regular expressions. 

Email matching regular expression example: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

### Anchors
The "^" tag can be used to search for character(s) where a line or string begin with that character. Given the line of code "There is an orange on the table", using "^T" will highlight the character "T", which indicates that this line of code starts with the character "T".

The "$" anchor tag is effectively the opposite. This is used to search for character(s) at the end of a line of code or string. If I were searching for an email, "testemail@gmail.com" I would use ".com$" in order to search for an email.

### Quantifiers
Quantifiers can only be used with other tags. They are used to narrow your search down..

The "{}" tags with two numbers separated by a comma is used to define a range you wish to search for. In our example, `{2,6}` searches for digits between 2 and 6.

The "+" is used to iterate a match more than once. In our case, our first query, `[a-z0-9_\.-]`, is being iterated an additional one time and our second search, `[\da-z\.-]`, is as well.

### Grouping Constructs
The "()" tag is used to group your string for one single search. In our example, `[a-z0-9_\.-]+)@([\da-z\.-]+` and `[a-z\.]{2,6}` are single searches with multiple parameters.

### Bracket Expressions
The "[]" tag is used to gather small groups of queries. In our example, `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` are held within bracket expressions to query within the brackets simulataneously.

### Character Classes
"." is like an all search, searching for a period. It will highlight anything except for a line break.

"\d" refers to digit. It will search for a number value 0-9.

### The OR Operator
The "|" tag is used as an OR operator, meaning that it will take "A" OR "B".

Our example expression does not utilize this.

### Flags
There are many flags that can be used in regular expressions, below are a few that are commonly used.

"g" is a global search, meaning it will try every character within a string to see if it matches the constraints.

"i" makes your search case-insensitive, so even if you search for "THE", "the" will still highlight.

"m" is a multi-line search.

### Character Escapes
The "\" tag is known as an escape code, this can be used to restore the original meaning to a character that might mean something else in a regular expression.

In our example, `\.` is used a couple of times. This takes a period, which would typically be an all search, and restores it to mean a period as a character within our search.

## Author

This was created by Nicholas Bales, full stack developer student with The Ohio State University. 
[Here is my GitHub](https://github.com/chaoskills08?tab=repositories) if you want to see more!
