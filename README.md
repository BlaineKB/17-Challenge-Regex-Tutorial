# Regex Tutorial for Matching a URL
Regular expressions or regex is a string of text characters that specifies a search pattern for matching,
locating, and managing text or validating input. This tutorial will cover the use of regex for matching a URL.

## Summary
` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `
This regex expression can be used to match and/or validate a URL. It can be broken down into separate components which are
defined below.

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [OR Operator](#or-operator)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
### Anchors
In this regex example the two anchors are `^` and `$` .
Anchors specify a position in the string where a match must occur. This typically signifies the beginning and the end of an expression.
`^` signifies the beginning of the expression and `$` signifies the end.

### Quantifiers
In this regex example the quantifiers are `?` and `*` .
Quantifiers will specify how many instances of a character, group, or character class must be in the input for a match to be found.
`?` refers to creating a single instance of the character(s) preceding the quantifier optional, and `*` refer to creating multiple instances of the character(s) preceding the quantifier optional.

### Bracket Expressions
In this regex example the bracket expressions are `[\da-z\.-]` `[a-z\.]` and `[\/\w \.-]` .
The bracket expressions are identified in the above regex by `[]`. The example expression will match or validate characters or character classes that are included inside of those brackets.

### Character Classes
In this regex example the main character classes to observe are `\d` and `\w` .
A character class defines a series of characters, which any one can occur in an input string in order for a match to be successful.
`\d` character class searches for any digit and `\w` character class searches for alphanumeric characters.

### Grouping and Capturing
In this regex example the groups are ` (https?:\/\/)` `([\da-z\.-]+)` `([a-z\.]{2,6})` and `([\/\w \.-]*)`. 
Numerous components can be separated into groups of interest. In our example above these groups are separated by parantheses `()` to signify this grouping of components for input evaluation.

### OR Operator
In this regex example there is no OR operator.
Typically in regex the OR operator can be signified by a `|`. for example the `(x|X)` will match either x or X from that input string. OR operators can provide options to match where one of the options should match given the OR operator.

### Greedy and Lazy Match
In this regex example our greedy and lazy matches can be identified by `*`, `+` and `{}`.
Greedy match means your expression will match as large a group as it possibly can and lazy match means it will match the shortest possible group. `*` will match the previous grouped character(s) any number of times, `+` will match the previous grouped character(s) at least one more time, and `{}` can place a number of match limits on a previous group. In our example above, `[a-z.]{2-6}` will match any lowercase a-z character and period at least two times and six times at the most. So if searching cat{2,6}, then catcat would match because cat would be repeated twice. catcatcatcatcatcat would also match because it would be repeated six times, however cat would not match due to only appearing once.

## Author
Blaine Brady is a full stack web developer and can be contacted here: 
 [GitHub](https://github.com/BlaineKB)
