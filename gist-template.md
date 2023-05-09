# Title (replace with your title)

Oftentimes in coding, we come across situations that require a specific type of input to function. If the information supplied by the user is in an incorrect format, it can cause failures in the application. To verify that the information provided in an application follows the correct format, we use regular expressions (RegEx for short). They are a sequence that looks like jibberish at first glance, but actually contain all of the guidance an application needs to check the format of a sequence.

## Summary

The RegEx we're covering in this document is for email address validation. The RegEx is used in situations where you require a user to provide an email address (when signing up for an account, enrolling in a mailing list, etc). If the response from the user did not follow the specific format of an email address (username|separator|domain name), using that email address would be possible.

For this tutorial, we will be using the following RegEx to verify an email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Here's a diagram of this RegEx broken down into more digestible chunks, but we'll go into each one of the complnents in more detail below:
![diagram of parts of email address RegEx](./Screenshot%202023-05-09%20152727.png)

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

In short, anchors signal the start and end of the regex. 

- `^` signals the beginning. Literally it is saying "the following characters are the first characters you will be seeing in the string." 
- `$` signals the end. Literally, it is saying "the previous set of characters are the last characters you will be seeing in the string."


### Quantifiers

Quantifiers identify any instances where a specific number of characters should be used in a group. In our email address example:

- `+` signals that AT LEAST 1 character should be present in the group
- `{2,6}` signals that 2-6 characters should be present in the group.


### Grouping Constructs

Grouping Constructs help break down the string we are validating into small chunks to validate piece by piece. These groups are separated by placing them in (parentheses). Each group can have its own allowable characters, displayed in `[brackets]` (see Bracket Expressions below). Some examples of groups from our email address RegEx are `([\da-z\.-]+)` or `([a-z\.]{2,6})`.


### Bracket Expressions

Bracket Expressions -- displayed inside `[brackets]` -- signify the allowable types of characters that may be used in that group. Examples would be `[a-z]`, `[0-9]`, `[_-.]`, or even a combination such as `[a-z0-9]`. Some examples from our email address RegEx:

- `_\.-` means the group may contain a limited set of special characters
- `a-z`  means the group may contain alpha characters 
- `0-9`  means the group may contain numeric characters 

### Character Classes

Another way to set limitations on what characters may be used in a group are Character Classes. These are preset definitions of what characters a group may contain. Some examples are `\w` to allow any alphanumeric character or underscore, or `\s` to include a space. In our email address example: 

- `\d` means that the group may contain any numeral digit (same as saying [0-9]).


### The OR Operator

The OR Operator (|) allows you to set specified allowable characters, while offering the flexibility of what order those characters are presented in. The email address RegEx does not use the OR Operator, but an example would be (P|S|U). This is saying that the letters P, S, and U will be present, but the order isn't important.


### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
