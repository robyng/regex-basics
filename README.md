# Regex Basics

Introductory paragraph (replace this with your text)

## Summary

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

A url is made up of differnet parts. 
1. Protocol: http:// 
2. Sub Domain: www or dev, the text that comes before the main domain and after the protocol
3. Domain: your main level domain name, which can include numbers and dashes
4. Domain extension
5. Path
6. Search

https://www.dynadot.com/community/blog/domain-name-rules.html 
domains 63 char limit

## Table of Contents

- [Regex Basics](#regex-basics)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
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
  - [Author](#author)

## Regex Components

### Anchors

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
     
Anchors help deliminate what you are searching for. Just like how forward slashs open and enclose a regex, the ^ symbol means to look for matches after this point. The $ symbol means to find matches before this point. When ^ and $ are used together they mean look for whats in between them.

In this case of matching a URL regex, the ^ is right after the opening / and the $ is at the end before the closing slash. It means to find a match within these points.

### Quantifiers

  /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

? quantifier is used 3 times in this example.
Quantifiers specify a match a certain number of times. 

The first quantifier used in this regex is ? before the https. It is saying look for matches with https OR http. The ? quantifier spcifies a match or 0 or 1 times for the characters preceeding it. 

The ? is used again after (https://)? so it is saying to look for matches of https:// or http:// or none. So it's saying a url be valid with or withou the http://

The + symbol is next quantifier. It matches once or many times, but not zero. So there must be numbers, or characters, or dashes, or dots to match. This is to cover all ranges of sub domains included www, www-2, dev, and dev.www for example.

Another quantifier is used to identify the domain extension: ([a-z\.]{2,6}) 
The quantifier here is {2,6} and it is saying any 2 characters minimun and up to 6 characters match. This will cover extensions com, co, info, biz etc PLUS the additional country codes extensions for example com.dz, info.us


### OR Operator

  /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

The OR operator is represented by |
  /(fab|t)/

Find fab or fat.

### Character Classes

  /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

Character Classes are also known as Character Sets. They search for a single diget or character. It is useful for finding commonly misspelled words or British spelling version. For example gr[ea]y will look for gray and grey.

If the character class uses ^ symbol after the first bracket it means don't match what's in the brackets. It is similar to how ! is used in javascripto to say NOT. [^0-9] means don't match single number 0 through 9. If it was [^09] means don't match 0 or 9.

Our example uses shorthand character classes.

([\da-z\.-]+)

\d means 0-9

([\/\w \.-]*)

\w means word character and is very broad. It matches single character of any the following:[A-Za-z0-9_]




### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

https://github.com/robyng
