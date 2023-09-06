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

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author