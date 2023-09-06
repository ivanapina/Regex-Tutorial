# Regex Tutorial

A regex, or "regular expression," is a versatile way of defining specific search patterns. Regular expressions are sequences of characters that, with a few language-specific adjustments to the syntax, can be used in most programming languages to find characters, sequences and patterns within strings. In addition to executing "find" or "find and replace" functions in search algorithms, regular expressions are also frequently used for input validation.

## Summary

In this tutorial, we'll employ a regex that can be used to validate to make sure that an email follows the correct format.

Matching Email-

```sh 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
```

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

The anchor is what starts and ends the regular expression. In the matching email code.

the anchors are the `^` and the `$`. This code specifically is saying that we are looking for something that starts with 

```sh
^([a-z0-9_\.-]+)
```

we will define what everything inside the parentheses later in this tutorial, but what the anchor means is that if we are to find a match it has follow those initial guidelines. It also has to end with 
```sh
.([a-z\.]{2,6})$
```

So, it must start and end with the given parameters within the code. If it does not, then it is not a match.

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For instance, if we used the following code in our regex, `xyz+` then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

```sh
([a-z0-9_\.-]+)
```
this will match any string that contains a-z, 0-9, _, ., or -. The quantifier `+` means that it has to contain at least one of this in order to have a match.


### OR Operator

It is not present in the code for the given matching email code, but in order to talk about the OR Operator, we will look at the following code for matching a hex code.

```sh
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```
This is a regex for matching a hex code that uses the OR Operator. What this will do is it will match where it starts with the # and that has to come first followed by one of the following:

```sh
[a-f0-9]{6}
```
which will match a 6 character long string that contains a combination of a-f letters and 0-9 numbers.

`|` OR Operator

```sh
[a-f0-9]{3}
```
it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers.

### Character Classes

`\d` is present in the given matching email code and what it will match a single letter character, a-z, after the `@` sign in the email address. Basically ensuring that a letter is matched after the `@` in the email and not a number or special character.

### Flags

A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression typically comes in the form:

```sh
/regex/
```
Where the slashes denote where the regular expresssion starts and ends. A flag can be used after the slash to give more guidelines for our matching. The flags are:

g which stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.
m which stands for "multiline" which will search line by line rather than searching through a string as a whole.
i which stands for "insensitive" will make the regular expression case-insensitive, so capitals and lower-case letters will not deture the matching.

### Grouping and Capturing

Contininuing with the code for matching an email:

```sh
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
We can talk about grouping and capturing.

`([a-z0-9_\.-]+)` is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. `([\da-z\.-]+)` is the second group that appears in our regex. `([a-z\.]{2,6})` is the third group that appears in our regex.

When matching, we have to make sure we are following the guidelines of the group before moving on to the next group.

### Bracket Expressions

Contininuing with the code for matching an email:

```sh
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

We can talk about grouping and capturing.

```sh
[a-z0-9_\.-]
```
The guidelines for matching the group. For this code snippet, it can contain letters a-z, numbers 0-9, an underscore, hyphen, or period.

The period is an escaped character, so it required the backslash in order to be able to be matched.

### Boundaries

If in a string, we are looking for for specific words. Boundaries are not used in the given matching an email code.

## Author

This tutorial was created by Ivana Pina
[GitHub](https://github.com/ivanapina/)
[Email](ivanapina@gmail.com)