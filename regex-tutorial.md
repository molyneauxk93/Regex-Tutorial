# Regex for matching an Email

Welcome to my Regex Tutorial! The purpose of my tutorial is to research a specific Regex, take that information, and put it in a format that I think will help readers get a better understanding of it, and hopefully be able to apply this knowledge effectively in their personal endeavors. 

## Summary

The regex that I will be breaking down today is one that will match an email. Code snippet: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Since we consider a regex to be a literal, they are wrapped in slash characters (/). However, the first part of the regex I will be noting directly relates to it's function. These are the anchors.

The first anchor is the `^` anchor, this basically says that the string that is being searched for begins with a range of possible matches that can be found within the brackets that follow the anchor. I will go into more detail on this later in the tutorial.

The second anchor is the `$` anchor. This represents a string and will end with the characters that come before it in the regex, in this case that is a range possible matches identified in the regex as opposed to an exact string. Therefore, both of these anchors being used help to provide some structure to the regex. 

We can see in the match an email regex, based on the anchors the string being searched for must contain a match to the patterns: `[a-z0-9_\.-]` , `[\da-z\.-]` , `[a-z\.]`. 

### Quantifiers

The quantifiers in the match and email regex consist of the `+` symbol, this functions as the connector between the different parts that make up an email. This means the `+` symbol is connecting the portion before and after the `@` symbol as well as the portion before and after the `.` . The other quantifier that can be seen in our match email regex is the `{2,6}`, this represents a range starting at 2 and goes up to 6 for the preceding pattern search. 

So in this case we can see that `[a-z\.]` precedes `{2,6}`. So, this quantifier is allowing a match to that pattern that is between 2 and 6 characters. 

### Grouping Constructs

The grouping contructs in our email match regex are the parentheses `( )` found surrounding each bracket expression. When wrapped in these grouping constructs, the bracket expressions are considered as subexpressions which are basically just any valid regex pattern. 

When regex patterns utilize parentheses are grouping contructs they are automatically numbered left to right which is based on the order of the opening parentheses in the regex. This follows the flow of reading an email. 

### Bracket Expressions

Inside the brackets of the email match regex contain patterns that we would like to search by. This is where the term bracket expression comes into play, they can also because positive character groups which means that we want to include what is specified within to find a match. 

The first bracket expression in the match email regex is `[a-z0-9_\.-]`. This one is saying that we are looking for a pattern that includes lowercase letters between a to z, numbers between 0 and 9, underscores, a dot, or dashes. 

The second bracket expression in the regex is `[\da-z\.-]` . This is saying that we are looking for a pattern that includes any digits between 0 and 9, lowercase letters between a-z, a dot, or dashes. 

The third bracket expression `[a-z\.]` in the regex is saying that we are looking for any lowercase letters between a-z, or a dot.


### Character Classes

Character classes are known in the context of regex as characters that are found within brackets. When this is done it signifies that characters within this character class will match characters that are given to this regex to validate. So, we can see that in our email match regex our character classes are `[a-z0-9_\.-]` , `[\da-z\.-]` , `[a-z\.]` . 

### Character Escapes

In our email match regex we use escapes to help identify what we are looking for in the pattern. Since the `.` in the regex on its own means 'any one character' . We are utilizing escapes to  indicate that we are looking for the dot (.) character. escapes are identified by '\' and are used in our bracket expressions `[a-z0-9_\.-]` , `[\da-z\.-]` , and `[a-z\.]` . 


## Author

Kevin Molyneaux is the author of this email match regex tutorial. You can find their GitHub Profile here: https://github.com/molyneauxk93

