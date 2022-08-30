# Regex tutorial for email validation

Regex is shorthand for the term "regular expressions", which are a sequence of characters which can define and validate a specific pattern. Regular expressions can be a combination of letters, numbers, special characters, and quantifiers. 


## Summary

Today I will be explaining the components of regular expressions that are used to validate an email address.
This is the regex code that we will analyze today: `/^w+[+.w-]*@([w-]+.)*w+[w-]*.([a-z]{2,4}|d+)$/i`

## Table of Contents

- [Regex tutorial for email validation](#regex-tutorial-for-email-validation)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

### Anchors

The anchors that we use to contain this particular Regex are `^` to start and `$` to finish.

### Quantifiers

In the example regex in the summary, we used  `+` a few times. This is an example of a greedy quantifier, which just means it will attempt to match as many instances as possible. We also used `{2,4}` near the end of the expression, this is another greedy quantifier that specifies the input needs to be a minimum of 2 characters but no more than 4 characters.

### Character Classes

In our regex, the character class `\w` is used. Javascript classifies this as a use of any word (letters, digits, underscores).

### Grouping and Capturing

There are three groups being captured in our example. The first is: `/^w+[+.w-]*@`. This is the "user name" and it captures everything before the `@`. The second group is: `([w-]+.)*w+[w-]*.`. This is the "domain name" and it captures everything in between the `@` and the `.`. The third and final group: `([a-z]{2,4}|d+)$/i` captures the "extension", or everything that comes after the `.`. (i.e .com or .net)

### Bracket Expressions

We have four different bracket expressions in our example expression! The information inside of the bracket is held in open/close brackets like this `[]`. This identifies what information is matched.

### Greedy and Lazy Match

In our example we only have greedy matches, (ex. `+` and `{}`). This means that it will allow the match to expand as long as it needs to. If we were to have used lazy quantifiers, then they would look like `+?` and `{}?`. These would direct the system to make the shortest match it can. 

## Author

My name is Camilo Arango, here is my [GitHub](https://github.com/Camilo-Arango)