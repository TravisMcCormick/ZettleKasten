**Tags**: #Linux #FileSystem #Hierarchy #Unix

---

### Definition

The **Linux File System** is a hierarchical directory structure that organizes files and directories starting from the root directory `/`. It follows the Filesystem Hierarchy Standard (FHS), providing consistency across different Linux distributions.

### Directory Structure

- **`/` (Root)**:
    - The top-level directory from which all other directories branch.
- **`/bin`**:
    - Essential user binaries (e.g., `ls`, `cp`).
- **`/sbin`**:
    - System binaries for administration (e.g., `ifconfig`).
- **`/etc`**:
    - Configuration files for the system.
- **`/home`**:
    - User home directories.
- **`/var`**:
    - Variable files like logs and spools.
- **`/tmp`**:
    - Temporary files.
- **`/usr`**:
    - User-installed software and libraries.
- **`/lib`**:
    - Essential shared libraries.
- **`/opt`**:
    - Optional add-on applications.
- **`/dev`**:
    - Device files representing hardware components.

### File Types

- **Regular Files**:
    - Text, binary, or executable files.
- **Directories**:
    - Containers for other files and directories.
- **Symbolic Links**:
    - Shortcuts or references to other files.
- **Special Files**:
    - Device files, sockets, and named pipes.

### Permissions and Ownership

- **Permissions**:
    - Read (`r`), write (`w`), execute (`x`) permissions for user, group, and others.
- **Ownership**:
    - Each file is owned by a user and a group.
- **Changing Permissions**:
    - `chmod`: Modify file permissions.
- **Changing Ownership**:
    - `chown`: Change file owner and group.

### Mounting File Systems

- **Mount Points**:
    - Directories where additional file systems are attached.
- **Mount Command**:
    - `mount`: Attaches a file system.
- **Unmount Command**:
    - `umount`: Detaches a file system.

### Personal Insight

**Understanding the Linux file system hierarchy is crucial for effective system navigation and administration**, enabling users to manage files, troubleshoot issues, and configure the system efficiently.

### Related Notes

- [[Linux Command Line Basics]]
- [[System Maintenance]]