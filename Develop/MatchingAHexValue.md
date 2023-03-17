# Matching a Hex Value

Introductory paragraph

Regular expressions, also known as regex or regexp, are a powerful tool for matching and manipulating text. They are a sequence of characters that define a search pattern and are used to match and manipulate strings of text based on specific rules. Regex is a popular tool used in programming languages, text editors, and command-line tools for tasks such as search and replace, data validation, and data extraction. While regex can seem daunting at first, mastering its syntax and concepts can greatly improve your ability to work with text-based data.

## Summary

The pattern uses various regex concepts like anchors, quantifiers, character classes, grouping and capturing, bracket expressions, greedy and lazy matching, boundaries, and look-around assertions to achieve this.

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

Let's break this pattern down into its components:

The hex value starts with a '#' character.
The hex value contains either 3 or 6 hexadecimal digits.
The hexadecimal digits can be either uppercase or lowercase.
The regex should not match any non-hexadecimal characters.
The pattern matches the entire hex value and nothing else

### Anchors

We will use the '^' and '$' anchors to ensure that the regex matches the entire hex value and nothing else.

### Quantifiers

We will use the '{n}' quantifier to specify that the hex value must contain either 3 or 6 hexadecimal digits.

### OR Operator

We will use the '|' operator to specify that the hexadecimal digits can be either uppercase or lowercase.

### Character Classes

We will use the '\d' character class to match any digit and the '\p{L}' character class to match any letter.

### Flags

We will use the 'i' flag to make the regex case-insensitive, so that it matches both uppercase and lowercase hexadecimal digits.

### Grouping and Capturing

We will use parentheses to group the hexadecimal digits and capture them as a single entity.

### Bracket Expressions

We will use a bracket expression to specify the allowed hexadecimal digits. We will use 'a-fA-F0-9' to match any uppercase or lowercase letter 'a' through 'f', and any digit '0' through '9'.

### Greedy and Lazy Match

We will use a greedy match by default, but we can make it lazy by adding a '?' after the quantifier

### Boundaries

We will use a negative lookahead assertion to ensure that the hex value is not preceded by any non-hexadecimal character.

### Back-references

We will not use any back-references in this pattern.

### Look-ahead and Look-behind

We will use a negative lookahead assertion to ensure that the hex value is not preceded by any non-hexadecimal character.
Putting all these concepts together, the regex pattern to match a hex value
`^(?!.*[^a-fA-F0-9]).*(?:#[a-fA-F0-9]{3}(?:[a-fA-F0-9]{3})?$)`
'^' matches the start of the string.
'(?!.*[^a-fA-F0-9])' is a negative lookahead assertion that ensures that the string does not contain any non-hexadecimal characters before the hex value.
'.*' matches any number of characters.
'(?:#[a-fA-F0-9]{3}(?:[a-fA-F0-9]{3})?$)' matches the hex value, which starts with a '#' character, followed by either 3 or 6 hexadecimal digits (which can be either uppercase or lowercase). The '(?:...)?' construct makes the second group optional.

## Author

 <ul>
   <li>Francisco Muniz - <a href="https://github.com/FrankM89">FrankM89</a></li>
 </ul>
