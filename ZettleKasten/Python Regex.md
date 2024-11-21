**Tags**: #Python #RegularExpressions #TextProcessing #DataParsing

---

### Definition

**Python Regex (Regular Expressions)** are sequences of characters that define search patterns, mainly used for string matching and manipulation in Python using the `re` module.

### Basic Syntax

- **Literal Characters**:
    
    - Matches the exact character (e.g., `a` matches 'a').
- **Metacharacters**:
    
    - **.**: Any character except newline.
    - **^**: Start of string.
    - **$**: End of string.
    - *****: Zero or more repetitions.
    - **+**: One or more repetitions.
    - **?**: Zero or one repetition.
    - **[]**: Matches any character inside the brackets.
- **Special Sequences**:
    
    - **\d**: Digit character.
    - **\w**: Alphanumeric character.
    - **\s**: Whitespace character.

### Common Functions

- **re.match()**:
    
    - Checks for a match only at the beginning of the string.
- **re.search()**:
    
    - Searches the string for a match anywhere.
- **re.findall()**:
    
    - Returns all non-overlapping matches in the string.
- **re.sub()**:
    
    - Replaces occurrences of the pattern with a substitute.
- **re.compile()**:
    
    - Compiles a regex pattern for reuse.

### Flags

- **re.IGNORECASE (re.I)**:
    
    - Case-insensitive matching.
- **re.MULTILINE (re.M)**:
    
    - `^` and `$` match the start and end of each line.
- **re.DOTALL (re.S)**:
    
    - The dot `.` matches all characters, including newline.

### Examples

- **Email Validation**:
    
``` python
    `pattern = r'^\w+@[a-zA-Z_]+?\.[a-zA-Z]{2,3}$'`
```
    
- **Extracting Numbers**:
    
``` python
    `numbers = re.findall(r'\d+', text)`
```
    

### Best Practices

- **Raw Strings**:
    
    - Use raw string notation (e.g., `r'\n'`) to avoid unintended escape sequences.
- **Testing Patterns**:
    
    - Use tools like regex101.com for testing and debugging.
- **Readability**:
    
    - Comment complex regex patterns for clarity.

### Personal Insight

**Mastering regular expressions in Python enhances your ability to handle text data effectively**, enabling powerful search, replace, and parsing capabilities essential in data processing tasks.

### Related Notes

- [[Text Processing Utilities]]
- [[Data Parsing Techniques]]
- [[String Manipulation in Python]]
- [[Regex Testing Tools]]