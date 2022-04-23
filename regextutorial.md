#  Regular Expressions

Introductory paragraph (replace this with your text)

## Summary

This tutorial to give specific examples for how the components of regex can be used. The following code can be used for matching emails. One use for this code is that it can be used to validate to make sure that an email follows the correct format.

Matching Email-

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
The anchor is what starts and ends the regular expression. In the matching email code,

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/,

the anchors are the ^ and the $. This code specifically is saying that we are looking for something that starts with
^([a-z0-9_\.-]+) and ends with ([\da-z\.-]+)\.([a-z\.]{2,6})$

what the anchor means is that if we are to find a match it has follow those initial guidelines.

So, it must start and end with the given parameters within the code. If it does not, then it is not a match.

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For instance, if we used the following code in our regex, xyz+ then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

([a-z0-9_\.-]+)

this will match any string that contains a-z, 0-9, _, ., or -. The quantifier + means that it has to contain at least one of this in order to have a match.

### Grouping Constructs
Contininuing with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can talk about grouping and capturing.

([a-z0-9_\.-]+) is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. ([\da-z\.-]+) is the second group that appears in our regex. ([a-z\.]{2,6}) is the third group that appears in our regex.

When matching, we have to make sure we are following the guidelines of the group before moving on to the next group. So, if we look at our code for matching the email: ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$ then we have to make sure that the first group is a-z, 0-9, _, ., or -. The second group is a-z, 0-9, _, ., or -. The third group is a-z, 0-9, _, ., or -. The fourth group is a-z, 0-9, _, ., or -. The fifth group is a-z, 0-9, _, ., or -. 

### Bracket Expressions

Contininuing with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can talk about grouping and capturing.

[a-z0-9_\.-]

The guidelines for matching the group. For this code snippet, it can contain letters a-z, numbers 0-9, an underscore, hyphen, or period.

The period is an escaped character, so it required the backslash in order to be able to be matched.

### Character Classes

\d is present in the given matching email code and what it will match a single letter character, a-z, after the @ sign in the email address. Basically ensuring that a letter is matched after the @ in the email and not a number or special character. 

### The OR Operator

It is not present in the code for the given matching email code, but in order to talk about the OR Operator, we will look at the following code for matching a hex code.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/ 

### Flags

Flags
A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression typically comes in the form:

/regex/ [flags]

where the flags are optional. The flags are used to specify how the regex should be used. For instance, the i flag is used to ignore case.



## Author

This tutorial was created by Michael Russiffilli 

Github: https://github.com/AllDeus
