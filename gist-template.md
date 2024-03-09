# Reg Ex Email Validation

This document is a tutorial explaining a regular expression used for email validation:
`/^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/`

## Summary

A regex, or regular expression is an array of characters that allows us to find matching patterns in a given code/data.
The regex I will be describing is a regular expression used to validate an email: `/^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/`
We will go through each elements of the expression explains what they mean.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

A reg ex is written between two `/` It allows anyone to know when does a reg ex start and when does it ends.

### Anchors

Regular expressions contains two anchors: a caret `^` and a dollar sign `$`.
The caret `^` indicates the beginning of the string and `$` the end of it.

### Quantifiers

A quantitfier indicates how many times the preceding element must appear in the tested string.
`+` indicates that the preceding elements, in this example `[\w-\.]` and `[\w-]` can appear once or more in the tested string.
Another quantifier identified in this regex is {2,4}, which will allow a match of 2 to 4 characters for the character set of `[\w-]`.

### Character Classes

Character classes, are groups of characters you want to match in the tested string. Thoses characters are writting between square brackets.
`\w` is also a character class that represents any word characters alphanumeric and underscore. `\w` is the equivalent of `[A-Za-z0-9_]`.
In this email validator regex, the character set `[\w-\.]` includes all word characters alphanumeric, underscore and hypen as well as `.`.
The character set `[\w-]` includes all word characters alphanumeric, underscore as well as hyphens.

### Grouping and Capturing

We can create characters groups to be treated as sungle unit using parenthesis `()`.
The following group `([\w-]+\.)` wnats the fist unit after the symbol `@` to only contains alphanumeric, underscore and hyphens and to finish with a dot `.`.

### Bracket Expressions

Brackets in a regular expression encloses characters to match. As seen above, the following brackets expressions found in the studied regex are:
`[\w-\.]` and `[\w-]`.

## Author

Magali Lebon, Coding Bootcamp student
https://github.com/maglb