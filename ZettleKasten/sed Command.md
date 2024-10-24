**Tags**: #Linux #CommandLine #TextProcessing #sed

---

### Definition

**sed** is a stream editor for filtering and transforming text in Unix/Linux environments. It reads input line by line, applies editing commands, and outputs the result.

### Functions

- **Text Substitution**: Replace text patterns.
- **Deletion**: Remove lines or patterns.
- **Insertion**: Add text at specific locations.
- **Transformation**: Change character cases or content.
- **Scripting**: Execute complex edits using scripts.

### Common Usage

- **Substitute Text**: `sed 's/old/new/' filename`
- **Global Replacement**: `sed 's/old/new/g' filename`
- **Delete Lines**: `sed '/pattern/d' filename`
- **In-Place Editing**: `sed -i 's/old/new/g' filename`
- **Insert Line**: `sed '2i\Inserted line' filename`

### Regular Expressions

- **Basic**: Default regex syntax.
- **Extended**: Use `sed -E` for extended regex features.

### Scripting with sed

- **Multiple Commands**: Separate with `;` or use `-e`.
- **Script Files**: Use `-f script.sed` to execute a file containing sed commands.

### Security Considerations

- **Data Loss**: Backup files before in-place editing.
- **Command Injection**: Validate inputs when using user-supplied data.

### Personal Insight

**sed is a powerful tool for batch editing and text manipulation**, essential for processing large amounts of data efficiently.

### Related Notes

- [[grep Command]]
- [[awk Command]]
- [[Regular Expressions]]
- [[Linux Shell Scripting Basics]]
- [Text Processing Utilities](Text%20Processing%20Utilities.md)