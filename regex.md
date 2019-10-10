# regular expressions


## Characters
| *symbol* | *description* | *remark* |
| -------------:|:--------- | ------ |
`.` | any character | 
`\d` | one digit character | 0-9
`\w` | one word character | letter, digit or underscore
`\s` | one whitespace character | space, tab, etc.
`\D` | character that is no digit character |
`\W` | character that is no word character |
`\S` | character that is no whitespace character |
`\` | escape a special character | `\.`, etc.

## Special Characters
| *symbol* | *description* | *remark* |
| -------------:|:--------- | ------ |
`\t` | tab |
`\r` | carriage return |
`\n` | line feed |
`\n` | line feed |   

## Characters Classes
| *symbol* | *description* | *remark* |
| -------------:|:--------- | ------ |
`[...]` | one of the characters in the brackets | `[ABC]` means one character A, B, or C
`-` | range indicator | `[0-5]` means one character from 0 to 5

## Quantifiers
| *symbol* | *description* | *remark* |
| -------------:|:--------- | ------ |
`?` | one or none (optional) |
`*` | zero or more times |
`+` | one or more times |
`{3}` | exactly three times |
`{2,4}` | two to four times |
`{3,}` | three or more times | 

## Logic
| *symbol* | *description* | *remark* |
| -------------:|:--------- | ------ |
&#124; | or operand | A&#124;B means one character that is A or B
`[^]` | not operand | `[^x]` is one character that is no x
`(...)` | define a group | groups are numbered from left to right
`\2` | repeat the content of group 2 |
  
## Anchors
| *symbol* | *description* | *remark* |
| -------------:|:--------- | ------ |
`^` | start of string or start of line (only outsinde if `[]`, inside it means not) | `^The` matches any string that starts with 'The'
`$` | end of string or end of line | `end$` matches any string that ends with 'end' 
