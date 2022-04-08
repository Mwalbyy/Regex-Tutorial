# Title How does an Email regex work?

In this tutorial I will show you how to navigate this email regex while showing you what each character in it does.

## Summary

```text
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
```

The string above may look like a random mess of unrelated characters, but it is actually a search function for finding email addresses. In the following sections I will show you the roles of each of the characters in detail.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors in a regex are used to identify a position. The two anchors that can be found in the email regex are the "^" found after the first forward slash, and the "$" and right before the closing forward slash  

### Quantifiers

Quantifiers in a regex specify how many times a character or group of characters must be present in order for the input to register as a match. The quantifiers used in the email regex are the "+" and the "{2,6}". The + connects the groups with each other, while the {2,6} limits the range of the characters to 2-6 for everything after the last "."

### Grouping Constructs

Grouping constructs are sections of a regex separated from one another by the use of parentheses(). In the Email regex there are three groups, the first being ([a-z0-9_\.-]+) which identifies everything before the @ character in an email. The second group is ([\da-z\.-]+) which is where the name of the email service would go (Gmail, Hotmail, Mac, etc...). The last group is ([a-z\.]{2,6}), this group is what checks to see if the end of the email address is valid, examples include but are not limited to (.com and .)

### Bracket Expressions

Bracket expressions are what contain [character Classes](#character-classes) in a regex. Our Email regex contains three different bracket expressions The first of which being [a-z0-9_\.-]. This bracket expression checks for any lowercase characters from a-z , any digits 0-9, and the characters ("_","-","."). The second bracket expression looks for the same characters as the previous expression, but excludes underscores("_").

### Character Classes

Character classes distinguish what character the regex should look for. The character classes in this regex are the "a-z", "0-9", and "\d". The first two character classes are ranges that tell the regex to look for any lowercase characters between a-z and numbers between 0-9. \d is the short hand of [0-9]

### Character Escapes

Character escapes allow for certain characters that would usually have a function in a regex be taken for their character value. This is done by prefacing a character with a "\", an example of this can be found multiple times in the email regex where the character escape "\." is used.

## Author

This informative piece was written by [Marcus Walby](https://github.com/Mwalbyy)
