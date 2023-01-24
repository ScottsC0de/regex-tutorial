# Regex Email Verification Tutorial

The following tutorial will be explaining how to use an *Email Verification Regex* to confirm a user's email address

*Regex*, short for 'Regular Expression', is a pattern of characters used to define a specific search pattern 

They describe what is to be accepted in an inputted string

For example, we can use this an Regex to confirm a user's email address exists and follows the criteria of a website's log-in

This tutorial is broken into sections, each of which can be found and linked to in the 'Table of Contents' section

## Summary

This regex email verifiction code is used to ensure an email is valid to do things like enter a site, complete a form, sign-up for site memberships, etc 

It is crucial on the internet and in the world of Web Development and important for user interaction

At first glance, a regex might look like a bunch of random letters, numbers and symbols

But, by breaking down each part of the regex, we can come to understand the expression as a whole

Consider the code snippet here:

```js
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

This snippet of code describes the email address as a string and indicates what can be included in it for it to be accepted 

> Notice how it's actually shaped like an email address; the first part looks like it can accept letters, numbers, and symbols, followed by a typical @ symbol, and then a period

This is a common way to write an email  

Let's break down each part in the upcoming sections

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Quantifiers](#quantifiers)
- [Character Classes and Escapes](#character-classes-and-escapes)

## Regex Components

Before we begin with the components of a regex, it is important to note the `/` at the beginning and end of the regex
> The `/` are required to be at the very beginning and end of a regex

It makes our regex written in what is known as *literal notation*
> **Note**: You can also write a regex as a *constructor*, which uses `""` instead of `/`

### Anchors

We shall begin the breakdown of the Email Verification Regex by reading it from left to right
> Notice after the `/` there is a `^`

This is known as an *Anchor*
> Anchors indicate the **beginning and end of a Regex**

With the exception of the `/`, regex will begin with a `^` and end with a `&`

The characters that follow the `^` signify a string
> **Note**: Regex is case-sensitive. 

```js
Take Away:

`^` indicates the beginning of the expression
`$` indicates the end of the expression
```

### Bracket Expressions

If we look after the first Anchor in our regex, you will notice it is followed by `()` and `[]`
> We will explain the `()` in the next section

For now, what's inside `[]` in a regex are known as *Bracket Expressions*, which describe our range of characters

Bracket expressions can contain any of the following characters:
- letters
- numbers
- symbols
> **Note**: The symbols in our Regex (_\.-) are not written out with a hypen like the letters and numbers. This is because we want only to use those specific symbols

Our regex uses 3 seperate bracket expressions. This is because a common email is broken down into 3 parts:
> Consider the following email scott-5902@gmail.com 
- our email username `[a-z0-9_\.-]` can contain letters, numbers, and the specified symbols *(scott-5902)*
- our domain name `[\da-z\.-]` *(@gmail)*
- our domain suffix `[a-z\.]` *(.com)*
> **Note** the `\` scattered throughout the regex. We will cover those in 'Character Classes and Escapes'

```js
Take Away:

`[a-z0-9_\.-]` indicates the email name can include lowercase letters a-z, any number, and only the specified symbols
`[\da-z\.-]` indicates the email domain name can include lowercase letters a-z and only the specified symbols 
`[a-z\.]` indicates the email domain name suffix can include lowercase a-z and a period
```

### Grouping and Capturing

We mentioned before our 3 bracket expressions are broken into what characters are accepted in our username, domain name, and suffix

This is what's known as *Grouping*

**Grouping** organizes a regex into *subexpressions*, grouped by `()`

**Capturing** is grouping these subexpressions into a single unit so they can be accessed seperately

```js
Take Away:

Our snippet is 'grouped' into 3 subexpressions

SubEx 1 `([a-z0-9_\.-]+)` 
SubEx 2 `([\da-z\.-]+)` 
SubEx 3 `([a-z\.])`
```
>**Note** the `+` sign. We will go over that in the 'Greedy and Lazy Match' section

### Quantifiers

Most regex have a limit on how many times the pattern will attempted to be matched
> These limits are known as *Quantifiers* 

**Quantifiers** are written in `{}` at the end of the regex before the `$`, with the first number indicating the minimum attempts and the second indicating the maximum

```js
Take Away:

{2,6} means the minimum match attempt is 2 and the maximum is 6
```

### Greedy and Lazy Match

Quantifiers are inherently *greedy*, meaning they will try to match the pattern as many times as possible
> Look for the `+` sign in our code, written at the end of our first 2 subexpressions

The `+` sign is what's known as a *repetition* operator, in that it says the character class preceding it can be matched one or more times
> We go over character classes in the next section

The `+` sign is what makes our quantifiers greedy
> In contrast, quantifiers are *lazy* by adding a `?` symbol after it. However, this regex does not include it

### Character Classes and Escapes

We have covered all but two characters in our regex
- The `.`, a **Character Class**
- The `\`, a **Character Escape**

Character *Classes* define a set of characters in a string of input
> Character *Escapes* change a classes interpretation

For example, normally, a `.` would indicate our regex matches any character expect the newline character(`/n`)
> Using a Character Escape, the `.` is now interpreted as part of the string in what symbols are accepted

Our `\` appears 4 times, each located before `.`
> This escapes each `.` following so they are not taken literally, changing their role from character class to a normal period

## About The Author

The author is a developer and tutorial creator with a GitHub repo found here: https://github.com/ScottsC0de