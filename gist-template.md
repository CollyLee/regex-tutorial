# Title (replace with your title)

Oftentimes in coding, we come across situations that require a specific type of input to function. If the information supplied by the user is in an incorrect format, it can cause failures in the application. To verify that the information provided in an application follows the correct format, we use regular expressions (RegEx for short). They are a sequence that looks like jibberish at first glance, but actually contain all of the guidance an application needs to check the format of a sequence.

## Summary

The RegEx we're covering in this document is for email address validation. The RegEx is used in situations where you require a user to provide an email address (when signing up for an account, enrolling in a mailing list, etc). If the response from the user did not follow the specific format of an email address (username|separator|domain name), using that email address would be possible.

For this tutorial, we will be using the following RegEx to verify an email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

### Quantifiers

### Grouping Constructs

Grouping Constructs help break down the string we are validating into small chunks to validate piece by piece. These groups are separated by placing them in (parentheses). Each group can have its own allowable characters, displayed in `[brackets]` (see Bracket Expressions below).

### Bracket Expressions

Bracket Expressions -- displayed inside `[brackets]` -- signify the allowable types of characters that may be used in that group. Examples would be `[a-z]`, `[0-9]`, `[_-.]`, or even a combination such as `[a-z0-9]`.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
