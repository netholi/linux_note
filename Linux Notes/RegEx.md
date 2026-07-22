| Pattern | Matches | Example Match |
|---------|---------|---------------|
| `.` | Any character except newline | `a`, `1`, `@` |
| `^` | Start of line/string | `^Hello` |
| `$` | End of line/string | `world$` |
| `*` | Zero or more of the previous character | `ab*c` → `ac`, `abc`, `abbc` |
| `+` | One or more of the previous character | `ab+c` → `abc`, `abbc` |
| `?` | Zero or one of the previous character | `colou?r` → `color`, `colour` |
| `{n}` | Exactly `n` occurrences | `\d{4}` |
| `{n,}` | At least `n` occurrences | `a{2,}` |
| `{n,m}` | Between `n` and `m` occurrences | `\d{2,4}` |
| `[]` | Character class | `[abc]` |
| `[^]` | Negated character class | `[^0-9]` |
| `[a-z]` | Lowercase letters | `a`–`z` |
| `[A-Z]` | Uppercase letters | `A`–`Z` |
| `[0-9]` | Digits | `0`–`9` |
| `[A-Za-z]` | Any letter | `A`, `z` |
| `[A-Za-z0-9]` | Alphanumeric characters | `a`, `7`, `Z` |
| `\d` | Any digit | `5` |
| `\D` | Any non-digit | `a`, `#` |
| `\w` | Word character (`A-Z`, `a-z`, `0-9`, `_`) | `hello_123` |
| `\W` | Non-word character | `@`, `-` |
| `\s` | Whitespace | Space, Tab, Newline |
| `\S` | Non-whitespace | `a`, `1` |
| `\t` | Tab character | `\t` |
| `\n` | Newline | `\n` |
| `\r` | Carriage return | `\r` |
| `\b` | Word boundary | `\bcat\b` |
| `\B` | Not a word boundary | `\Bcat\B` |
| `()` | Capture group | `(abc)` |
| `(?:)` | Non-capturing group | `(?:abc)` |
| `|` | OR operator | `cat\|dog` |
| `\` | Escape special character | `\.` matches a literal `.` |
| `.*` | Any number of any characters | `abc.*xyz` |
| `.+` | One or more of any character | `.+` |
| `.*?` | Non-greedy match | `<.*?>` |
| `(?=...)` | Positive lookahead | `\d(?=px)` |
| `(?!...)` | Negative lookahead | `\d(?!px)` |
| `(?<=...)` | Positive lookbehind | `(?<=\$)\d+` |
| `(?<!...)` | Negative lookbehind | `(?<!\$)\d+` |

## Common Real-World Patterns

| Purpose                | Regex                                  |                   |
| ---------------------- | -------------------------------------- | ----------------- |
| Email                  | `^[\w.-]+@[\w.-]+\.[A-Za-z]{2,}$`      |                   |
| URL                    | `https?://\S+`                         |                   |
| IPv4 Address           | `^(\d{1,3}\.){3}\d{1,3}$`              |                   |
| MAC Address            | `^([0-9A-Fa-f]{2}:){5}[0-9A-Fa-f]{2}$` |                   |
| Date (YYYY-MM-DD)      | `^\d{4}-\d{2}-\d{2}$`                  |                   |
| Time (HH:MM)           | `^\d{2}:\d{2}$`                        |                   |
| 24-hour Time           | `^([01]\d                              | 2[0-3]):[0-5]\d$` |
| Hex Color              | `^#([A-Fa-f0-9]{6}                     | [A-Fa-f0-9]{3})$` |
| Integer                | `^-?\d+$`                              |                   |
| Decimal Number         | `^-?\d+(\.\d+)?$`                      |                   |
| Positive Integer       | `^[1-9]\d*$`                           |                   |
| Username               | `^[A-Za-z0-9_]{3,20}$`                 |                   |
| Linux Filename         | `^[^/]+$`                              |                   |
| HTML Tag               | `<[^>]+>`                              |                   |
| Quoted String          | `"(.*?)"`                              |                   |
| Multiple Spaces        | `\s+`                                  |                   |
| Blank Line             | `^\s*$`                                |                   |
| Starts with "foo"      | `^foo`                                 |                   |
| Ends with ".txt"       | `\.txt$`                               |                   |
| Only Letters           | `^[A-Za-z]+$`                          |                   |
| Only Digits            | `^\d+$`                                |                   |
| Only Alphanumeric      | `^[A-Za-z0-9]+$`                       |                   |
| Remove Leading Spaces  | `^\s+`                                 |                   |
| Remove Trailing Spaces | `\s+$`                                 |                   |