**Tags**: #RegularExpressions #Regex #TextProcessing #PatternMatching

---

### Definition

**Regular Expressions (Regex)** are sequences of characters defining search patterns, mainly used for string matching and manipulation. They are a powerful tool in programming and text processing.

### Functions

- **Searching**: Find patterns within text.
- **Validation**: Check if input matches a format.
- **Replacement**: Substitute parts of a string.
- **Parsing**: Extract information from text.

### Basic Syntax

- **Literals**: Exact characters to match (`cat` matches 'cat').
- **Character Classes**:
    - `[abc]`: Any character 'a', 'b', or 'c'.
    - `[^abc]`: Any character except 'a', 'b', or 'c'.
- **Quantifiers**:
    - `*`: Zero or more occurrences.
    - `+`: One or more occurrences.
    - `?`: Zero or one occurrence.
    - `{n}`: Exactly n occurrences.
- **Anchors**:
    - `^`: Start of a line.
    - `$`: End of a line.
- **Groups**:
    - `()` Captures a group.
    - `|` Logical OR between patterns.

### Examples

- **Email Pattern**: `^\S+@\S+\.\S+$`
- **Phone Number**: `^\d{3}-\d{3}-\d{4}$`
- **Whitespace Trimming**: `^\s+|\s+$` matches leading/trailing whitespace.

### Tools Supporting Regex

- **Command Line**: `grep`, `sed`, `awk`
- **Programming Languages**: Python (`re` module), JavaScript, Perl
- **Text Editors**: Vim, Sublime Text, VS Code

### Security Considerations

- **Injection Risks**: Validate inputs to prevent malicious patterns.
- **Performance**: Complex patterns may cause slow processing.

### Personal Insight

**Regular expressions are indispensable for efficient text processing**, but require careful crafting to avoid errors and ensure optimal performance.

### Related Notes

- [[grep Command]]
- [[awk Command]]
- [[sed Command]]
- [Python Regex](Python%20Regex.md)
- [Regex Testing Tools](Regex%20Testing%20Tools.md)