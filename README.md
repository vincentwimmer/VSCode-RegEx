# VSCode-RegEx

## Word Searches

* ### Find lines NOT containing a word
```
^(?!.*\bword\b).*\n
```

* ### Find lines containing any two specific words in any order
```
^(?=.*\bword1\b)(?=.*\bword2\b).*$
```

* ### Swap around two words separated by a space
```
Find: (\w+)\s(\w+)
Replace: $2 $1
```

## Line Manipulation and Formatting

* ### Select everything past "The" on all lines
```
The (.*)
```

* ### Select last 8 characters of all lines
```
.{8}$
```

* ### Select last 8 characters of all lines (Only Numbers)
```
.[0-9]{8}$
```

* ### Find all double or more spaces
```
\s{2,}
```

* ### Find whitespace at the beginng of lines
```
^\s+
```

* ### Remove blank lines
```
Find: ^\n|\r
Replace:
```

## Data Specific

* ### Find Emails
```
[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}
```

* ### Find Emails with a specific domain
```
[a-zA-Z0-9._%+-]+@(example\.com|anotherdomain\.org)
```

* ### Find IP Addresses
```
\b(?:[0-9]{1,3}\.){3}[0-9]{1,3}\b
```

* ### Find non-ASCII characters
```
[^\x00-\x7F]+
```

* ### Find Hex color codes
```
#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})\b
```

* ### Find UUIDs
```
\b[0-9a-fA-F]{8}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{4}\b-[0-9a-fA-F]{12}\b
```
