**Tags**: #Linux #CommandLine #Shell #CLI

---

### Definition

**Linux Command Line Basics** involve understanding and using the shell interface to interact with the Linux operating system. The command line allows users to perform tasks such as file manipulation, program execution, and system administration by typing commands.

### Essential Commands

- **Navigation**:
    - `ls`: Lists files and directories.
    - `cd`: Changes the current directory.
    - `pwd`: Displays the present working directory.
- **File Operations**:
    - `cp`: Copies files or directories.
    - `mv`: Moves or renames files or directories.
    - `rm`: Removes files or directories.
    - `mkdir`: Creates a new directory.
- **File Viewing**:
    - `cat`: Concatenates and displays file content.
    - `less`: Views file content page by page.
    - `head`/`tail`: Displays the beginning or end of a file.
- **System Information**:
    - `uname -a`: Shows system information.
    - `df -h`: Displays disk space usage.
    - `top`: Monitors system processes.
- **Permissions**:
    - `chmod`: Changes file permissions.
    - `chown`: Changes file ownership.

### Command Structure

- **Syntax**:
    
    bash
    
    Copy code
    
    `command [options] [arguments]`
    
- **Options**:
    - Modify the behavior of commands (e.g., `-l` for long format in `ls -l`).
- **Arguments**:
    - The targets on which the command operates (e.g., filenames).

### Shortcuts and Tips

- **Tab Completion**:
    - Press `Tab` to auto-complete commands or filenames.
- **Command History**:
    - Use the up/down arrow keys to navigate through previous commands.
- **Piping and Redirection**:
    - `|`: Sends the output of one command as input to another.
    - `>`/`>>`: Redirects output to a file (overwrite/append).
- **Wildcards**:
    - `*`: Represents any number of characters.
    - `?`: Represents a single character.

### Personal Insight

**Mastering the Linux command line enhances efficiency and opens up powerful system capabilities**. It is an indispensable skill for developers, system administrators, and power users working within Unix-like environments.

### Related Notes

- [[Shell Scripting Basics]]
- [[Linux File System]]
- [[Text Processing Utilities]]
- [[Package Management with APT]]