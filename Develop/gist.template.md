# Regex Tutorial - Validating Email Addresses

In this tutorial, I'll break down how a regex pattern can validate an email address. Regex, short for regular expressions, is a tool that matches patterns within text. This pattern checks if a string follows the correct email format, including a username, the "@" symbol, a domain name, and a top-level domain like .com.

## Summary

This regex pattern is used to validate email addresses, ensuring they follow the format `username@domain.com`. It verifies that a username appears before the "@" symbol, followed by a valid domain and top-level domain.

**Regex Pattern**: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


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

- **`^` and `$`**:
   - `^` is the start anchor, ensuring the string starts with the specified pattern.
   - `$` is the end anchor, ensuring the string ends with the specified pattern.
   - These ensure the pattern matches the entire email, with no extra characters at the beginning or end.

### Quantifiers

- **`+`**:
   - In `([a-z0-9_\.-]+)`, `+` means "one or more of these characters."
   - This applies to the username part, so it can be any length, as long as it has at least one character.

### OR Operator

This regex doesn’t use the OR operator (`|`), which would allow for alternatives.

### Character Classes

- **`[a-z0-9_\.-]`**:
   - This part allows lowercase letters (`a-z`), digits (`0-9`), underscore (`_`), period (`.`), and hyphen (`-`) in the username section.
- **`[\da-z\.-]`**:
   - This part allows digits (`\d`), lowercase letters (`a-z`), period (`.`), and hyphen (`-`) in the domain section.

### Flags

- This regex has no flags. Flags are optional parameters that change the behavior of the regex (e.g., case insensitivity), but this pattern does not need them.

### Grouping and Capturing

- **`()`**:
   - This regex has three groups, one for each main section of the email (username, domain, and top-level domain).
   - Each set of parentheses `()` captures a specific part of the email, which can be useful if you need to extract these parts individually.

### Bracket Expressions

- **`[a-z0-9_\.-]`** and **`[a-z\.]`**:
   - Bracket expressions allow a range of characters to be matched.
   - `[a-z0-9_\.-]` matches lowercase letters, numbers, `_`, `.`, or `-`.
   - `[a-z\.]` matches lowercase letters and `.` for the top-level domain.

### Greedy and Lazy Match

- **Greedy Match**:
   - This regex is greedy by default, as it doesn’t use a lazy quantifier like `?`.
   - `+` is a greedy quantifier, so it tries to match as many characters as possible within the specified set.

### Boundaries

- There are no specific boundaries (like word boundaries `\b`) in this regex because it’s designed to match the entire string with `^` and `$`.

### Back-references

- This regex does not use back-references, which refer to previously matched groups.

### Look-ahead and Look-behind

- This regex does not use look-ahead or look-behind assertions, which match patterns based on surrounding text without including it in the match.

## Author

Hi, I’m Maleeha! I’m a web development student learning regex and other programming concepts. Check out more of my work on [GitHub](https://github.com/maleehali).

## Gist Link: https://gist.github.com/maleehali/a85e02e360f79c75daf1cab68f2a1
