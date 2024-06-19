Regex Tutorial

Introductory paragraph 

what is REGEX? 
A regular expression "Regex" is a sequence of characters that specifies a match pattern in text. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation.


Summary

Regular expressions (regex) are powerful tools used in programming for pattern matching within strings. This tutorial will break down a specific regex used to match email addresses and explain each component in detail.
In this tutorial, we will explain the regex pattern used to validate email addresses - /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

Table of Contents

Anchors
Quantifiers
OR Operator
Character Classes
Flags
Grouping and Capturing
Bracket Expressions
Greedy and Lazy Match
Boundaries
Back-references
Look-ahead and Look-behind
Regex Components

Anchors
The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.

Quantifiers
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They match as many occurrences of particular patterns as possible. They include the following:


1. *—Matches the pattern zero or more times

2. +—Matches the pattern one or more times

3. ?—Matches the pattern zero or one time

4. {}—Curly brackets can provide three different ways to set limits for a match:

5. { n }—Matches the pattern exactly n number of times

6. { n, }—Matches the pattern at least n number of times

7. { n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

In our email regex, + is used to ensure that there is at least one character in the username and domain name parts.

OR Operator

Character Classes

Flags

Grouping and Capturing

Bracket Expressions

Greedy and Lazy Match

Boundaries

Back-references

Look-ahead and Look-behind

Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
