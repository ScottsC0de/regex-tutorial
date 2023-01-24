# Regex Email Verification Tutorial

The following tutorial will be explaining how to use Regex to confirm a user's address. 

*Regex*, short for 'Regular Expression', is a pattern of characters used to define a specific search pattern 

*Regex* describe what is to be accepted in a string

For example, we can use this an **Email Verification Regex** to confirm a user's email address exists and follows the criteria of a website's log-in.

The tutorial is broken into sections, each of which can be found and linked to in the 'Table of Contents' section.

## Summary

Regex's email validation code is used to ensure an email is valid to enter a site, complete a form, sign-up for site memberships, etc. It is crucial on the internet and in the world of Web Development and important for user interaction. At first glance, a Regex might look like a bunch of random letters, numbers and symbols. By breaking down each part of the Regex we can come to understand the expression as a whole. 

Consider the code snippet here:

```js
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

This snippet of code describes the email address as a string and indicates what can be included in it for it to be accepted. Notice how it's actually shaped like an email address; the first part looks like it can accept letters, numbers, and symbols, followed by a typical @ symbol, and then a period. This is a common way to write an email.  Now, let's break down each part in the upcoming sections.

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Quantifiers](#quantifiers)
- [Character Classes and Escapes](#character-classes-and-escapes)

## Regex Components

Before we begin with the components of a Regex, it's important to note the / at the beginning and end of the Regex

The / indicates 

### Anchors

We shall begin the breakdown of the Regex by reading it from left to right

Notice after the `/` there is a `^`

This is known as an *Anchor*

Anchors indicate the **beginning and end of a Regex**

With the exception of the `/`, Regex will begin with a `^` and end with a `&`

The characters that follow the `^` signify a string
> **Note**: Regex is case-sensitive. 

```js
Take Away:

`^` indicates the beginning of the expression
`$` indicates the beginning of the expression
```

### Bracket Expressions

If you look after the first Anchor in our Regex, you will notice it is followed by `()` and `[]`

We will explain the `()` in the next section

For now, what's inside `[]` in a Regex are known as *Bracket Expressions*, which describe our range of characters

Bracket expressions can contain any of the following characters:
- letters
- numbers
- symbols
> **Note**: The symbols in our Regex (_\.-) are not written out with a hypen like the letters and numbers. This is because we only want to use those specific symbols

Our Regex uses 3 seperate bracket expressions

This is because an email is broken down into 3 parts (with examples): 
- our email username [a-z0-9_\.-] can contain letters, numbers, and the specified symbols (Scott-5902)
- our domain name [\da-z\.-] (@gmail)
- our domain suffix  [a-z\.] (.com)
> **Note**: The `\` scattered throughout the Regex. We will cover that in 'Character Classes and Escapes'


```js
Take Away:

`[a-z0-9_\.-]` indicates the email name can include lowercase letters a-z, any number, and only the specified symbols
`[\da-z\.-]` indicates the email domain name can include lowercase letters a-z and only the specified symbols 
`[a-z\.]` indicates the email domain name suffix can include lowercase a-z and a period
```

### Grouping and Capturing

**Grouping** is the way a Regex is organized into *subexpressions*, grouped by ()

([a-z0-9_\.-]+) @ ([\da-z\.-]+) \. ([a-z\.]{2,6})

**Capturing** is grouping into a single unit

### Quantifiers

Sets the character limit

{2,6}

### Greedy and Lazy Match

Quantifiers are inherently *greedy*

The + sign is what's known as a *repetition* operator in that it says the character class preceding it can be repeated one or more times.

Quantifiers are 'lazy' by adding a ? symbol after it

### Character Classes and Escapes

Character *Escapes* are a backslash \ that escapes a character used for Regex commands and instead interprets it as a string. It is a way for it to be rendered not literally. For example, in the email Regex, the backslash escapes the .

Character *Classes* defines a set of characters in a string of input. For example, the . we talked on above matches any character except the newline character (/n)

## About The Author

Rookie programmer and tutorial creator with a GitHub repo found here: https://github.com/ScottsC0de