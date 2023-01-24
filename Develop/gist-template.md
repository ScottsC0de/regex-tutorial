# Regex Email Verification Tutorial

Introductory paragraph (replace this with your text)

The following tutorial will be explaining how to use Regex to confirm a user's address. 

*Regex*, short for 'Regular Expression', is 

The tutorial is broken into sections, each of which can be found in the 'Table of Contents' section.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Regex's email validation code is used to ensure an email is valid to enter a site, complete a form, sign-up for site memberships, etc. It is crucial on the internet and in the world of Web Development. I have chosen this Regex expression because I feel it is the most important for user interaction. 

Snippet of Email Validation Code:

```js
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
The following sections will explain each part of the code...

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Grouping and Capturing](#grouping-and-capturing)
- [Quantifiers](#quantifiers)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Character Classes](#character-classes)

## Regex Components

The following sections explain each part of the Regex with code snippets included

### Anchors

To begin explaining our Regex expression, we can start by looking at what are called the *Anchors*

Before that, note the forward / at the beginning and end.

Anchors: ^ and $

### Bracket Expressions

The brackets indicate the range of characters included in the email. 

[a-z0-9_\.-] [\da-z\.-] [a-z\.] and talk about the plus sign

### Grouping and Capturing

**Grouping** is the way a Regex is organized into *subexpressions*, grouped by ()

([a-z0-9_\.-]+) @ ([\da-z\.-]+) \. ([a-z\.]{2,6})

**Capturing** is grouping into a single unit

### Quantifiers

Sets the character limit

{2,6}

### Greedy and Lazy Match

Quantifiers are inherently *greedy*

### Character Classes and Escapes

Character *Escapes* are a backslash \ that escapes a character used for Regex commands and instead interprets it as a string. It is a way for it to be rendered not literally. For example, in the email Regex, the backslash escapes the .

Character *Classes* defines a set of characters in a string of input. For example, the . we talked on above matches any character except the newline character (/n)

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)