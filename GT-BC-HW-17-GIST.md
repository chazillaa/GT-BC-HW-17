# GT-BC-HW-17-GIST REGEX HEX VALUE TUTORIAL

A regular expression, or regex, is a string of characters that defines a pattern for a search. It is a power and versatile tool that can be used for matching and manipulating strings in programing. With it, you can search for specific text patterns and change them according to rules you set in place.

## Summary

In this tutorial we will be going over how to use regex for email matching. Email matching with regex uses a regex pattern to match and validate email addresses in a string. These patterns can be customized for specific requirements of the email that needs to be matched. We will be going over regex for emails using `/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`.

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
`/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

Anchors: `^` and `$`. You can use `^` to indicate the start of a string, and `$` to indicate the end of that string. It is important to note that there is no use of mulitline, which means that these two indicators will only match the start and end of the string, rather than the start and end of individual lines within a string. 

### Quantifiers
`/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

Quantifiers: `+` `{x,y}` `?` `*`. Quantifiers are used to specify how many times a particular character or group of character should occur. When it comes to email matching with regex, some of the common quantifiers include.

`+` is used to match characters or group of characters one or more times.

`?` is used to match characters or group of characters zero or one time.

`*` is used to match characters or group of characters zero or more times.

`{x,y}` is used to match characters or group of characters at least `x` times and at most `y` times.


### Grouping Constructs
`/^(user|admin)@[a-zA-Z0-9]+\.[a-zA-Z]+$/i`

Grouping constructs are used with regex to group multiple elements together, and apply a quantifier to the whole group. Some common examples for regex email matching include.

`()` which groups elements together to create sub-expressions.

`(x|y)` looks to match either x or y.

`?:` groups elemnts without creating a capturing group. 

In the example above `(x|y)` is used to match an email address that starts with either `user` or `admin` 


### Bracket Expressions
`[a-z0-9_\.-]`

Bracket Expressions: `[]`. A bracket expression can be used to represent an array of characters that we want to match. In the example, because `a-z` `0-9` `_` `\` `.` `-` are within `[]` meaning the user can use the letters, numbers, and symbols represented within the brackets. 

### Character Classes
`/^[a-zA-Z0-9]+@[a-zA-Z0-9]+\.[a-zA-Z]+$/i`

Character classes in regex, are used to match one character from a group of characters. These character classes can be used in regex to match email addresses. These character classes are defined by using `[]` whatever characters are defined with the brackets can be used to match a character in the string that is within the class. Some of the character classes include

`[a-z]` to match any lowercase letter from a to z.

`[A-Z]` to match any uppercase letter from A to Z.

`[0-9]` to match any number from 0-9.

`[/d]` to match any digit.

`[/D]` to match any non-digit.

`[/w]` to match any word character, including letters, digits, and underscores.

`[/W]` to match any non-word characters.


### The OR Operator
`[a-z|0-9|_|\.|-]`

OR Operator: `|`. The OR Operator `|` enables the matching of a pattern if one of multiple alternatives is present in the input string. Unlike a regex that has all its requirements specified, a bracket expression does not require the input string to meet all of the conditions in the pattern. The example above is `[a-z0-9_\.-]` written with the `|` OR Operator.

### Flags

Flags are used to alter the default search behavior of the regex. A flag is placed at the end of a regex, after the second `/` Flags can be used to modify various aspects of regex matching. 

`i` makes the regex matching case-insensitive, meaning that uppercase and lowercase characters are treated the same. 

`g` enables global matching, which allows the regex to find all matche sin the input string instead of just the first match. 

`m` multiline mode, enables the regex to match aptterns across multiple lines of text. 

`s` or dotall mode allows the `.` character to match newline characters as well. 

`u` the unicode flag allows the regex to handel unicode characters propery. 

`y` sticky mode allows users to force the regex to start matching at a the current position in the string.

### Character Escapes
`/^[a-z0-9\.]+@[a-z0-9]+\.[a-z]+$/i`

Character escapes are used to represent special characters within the regex syntax. Some of the common character escapes include `.` and `@` for matching emails.

`.` is used for a `period` character in emails the `period` is used to seperate the domain and subdomains.

`@` is used for the `at` character in emails the `at` is used to seperate the username and domain. 

## Author

GT-BC-HW-17-GIST-REGX-EMAIL was created by [Chazillaa](https://github.com/chazillaa)
