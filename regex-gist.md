# Regex Tutorial

Regex is short for regular expressions. They are used to identify particular characters and patterns through a coded search query. This search method has a specific syntax, and, once implemented, has powerful abilities to validate and identify complex structures within your code that typical search options couldn't achieve.

## Summary

Let's look at `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This is code for matching Hex Values that we will specifically look at in our code snipets.

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

regex = / ^The end$/; // exact string match starting with “The” and ending with “End”
/_ escape characters _/

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

HEX Values: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Code Snipet: `/^#`, `$.`

This asserts that this is the beginning and end of the string respectively.

### Quantifiers

This will regulate how many numbers of characters or expressions to match in a row. They modify how we interpret the searches such as \d, \w, \s etc.

- An asterisk or a "+" will be seen as greedy, and they will match with as much of the string as possible.
- - is at least 1 or more matches
- ? character will make it "non-greedy" and will stop when it has a match, but also accepts 0.
- Using bracket notation around a positive integer after a character will match with that character if it is used in that word for the amount of times the integer states, or add a comma between two integers to utilize a min max.

HEX Values: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Code Snipet: `#?`

This asserts that it could either contain a # or not.

Code Snipet: `{6}` and `{3}`

This asserts that the preceding classes will have the 'n' number of characters.

### Grouping Constructs

- x|y will match either "x" or "y"

### Bracket Expressions

### Character Classes

- [abc] will match one of the enclosed characters within the range. It will look for a, or b, or c.

HEX Values: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Code Snipet: `[a-f0-9]`

This combination implies that we will look for any character between a and f in the alphabet as well as any integer between 0 and 9 in the numeric.

### The OR Operator

HEX Values: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Code Snipet: `([a-f0-9]{6}|[a-f0-9]{3})`

This shows that it will either match the expression before or after the '|', in this case it would either be 6 or 3 characters.

## Author

My name is Chris Insignares. My goal is to learn to build my own effective websties in react and utilize databases to achieve speedy functionality to business data.

You will see new projects in the future at: https://github.com/ChrisIgg

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
