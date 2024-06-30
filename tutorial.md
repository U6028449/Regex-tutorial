# Regex Tutorial: Matching an Email Address

In this tutorial, we'll explore how to use regular expressions (regex) to match email addresses. Understanding how to construct and interpret regex can be incredibly useful for validating user input, among other applications.

## Table of Contents

1. [Introduction](#introduction)
2. [Regex Explained](#regex-explained)
    - [Start of Line](#start-of-line)
    - [User Name](#user-name)
    - [Domain Name](#domain-name)
    - [Top-Level Domain](#top-level-domain)
3. [Examples](#examples)
4. [Conclusion](#conclusion)
5. [About the Author](#about-the-author)

## Introduction

Regular expressions are patterns used to match character combinations in strings. In web development, they're often used for data validation. Today, we'll break down a regex pattern designed to match email addresses.

## Regex Explained

The regex pattern for matching an email address looks like this:

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

Let's break down what each part of this pattern means.

### Start of Line

```regex
^
```

The `^` asserts the start of a line, ensuring the pattern matches from the beginning of the string.

### User Name

```regex
([a-z0-9_\.-]+)
```

This part matches the user name of the email. It includes:
- Lowercase letters (`a-z`)
- Digits (`0-9`)
- Underscores (`_`)
- Periods (`.`)
- Hyphens (`-`)

The `+` indicates that the preceding character set can appear one or more times.

### Domain Name

```regex
([\da-z\.-]+)
```

Following the `@` symbol, this section matches the domain name and includes:
- Digits (`\d`)
- Lowercase letters (`a-z`)
- Periods ([`.`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FUsers%2FLidia%2Fbootcamp%2Fregex%20tutorial%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\Lidia\bootcamp\regex tutorial"))
- Hyphens (`-`)

Like the user name, the `+` means this part can appear one or more times.

### Top-Level Domain

```regex
([a-z\.]{2,6})
```

This part matches the top-level domain (TLD) of the email address. It must be:
- Between 2 to 6 characters long (`{2,6}`)
- Composed of lowercase letters (`a-z`) and possibly periods (`.`)

## Examples

Valid email addresses that match our regex:

- `example@example.com`
- `user.name@domain.co.uk`
- `user-name@domain.com`

Invalid email addresses:

- `@example.com` (No user name)
- `example@.com` (No domain name)
- `example@domain` (No top-level domain)

## Conclusion

Regular expressions are a powerful tool for pattern matching and validation. By understanding the components of a regex pattern, you can tailor it to fit your specific needs, such as validating email addresses.

## About the Author

This tutorial was created by [Patrick Granger](https://github.com/U6028449). Feel free to connect with me on GitHub and check out my other projects.