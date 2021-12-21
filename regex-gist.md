# Regex Tutorial

Regex is short for regular expressions. They are used to identify particular characters and patterns through a coded search query. This search method has a specific syntax, and, once implemented, has powerful abilities to validate and identify complex structures within your code that typical search options couldn't achieve.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

Regular expressions have multiple components that can be utilized to analyze strings/pieces of strings.

### Anchors

Anchors are ways matching at a particular point in the string.

- **^** :
  This denotes 'Beginning of string' at that current position. When multiline is on, this will match at the beginning of each line as well.
- **$** :
  This denotes that it is at the 'End of the string' .
- **/A** :
  This asserts that the position is the beginning of the string, and does not match other phrases that may be later in the string but separated through line breaks.
- **\z** :
  Does not exist in javascript or python, but will match with the very end of the string and will not match any at the end of line breaks within that string.
- **\Z** :
  This will match with the end of the string but will also match with the end of line breaks. In python, however, it will act as the above (/z)
- **\b** :
  Matches with positions where one side is a word character, and the other side is not a word character. If "\b" comes before the word, it will match with strings that have a non-word character before the word. If "\b" comes after the word, it will match with strings that have a non-word character after that word.

> 1.  \bdog will match with dog, doggo, doggie
> 2.  dog\b will match with catdog, dog
> 3.  \bdog\b will only match with dog

- **\B** :
  In comparison to "/b", "/B" will do the opposite. It will find the word with the "\B" component and it will not recognize a match if there is a non-word character in the position it is referring to.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
