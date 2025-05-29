**Tags**: #TerminalMultiplexer #CommandLine #Productivity #Unix

---

### Definition

**tmux** (terminal multiplexer) is a command-line tool that allows users to run multiple terminal sessions within a single window or remote session. It enables session persistence, window management, and easy switching between tasks.

### Key Features

- **Session Management**:
    - Detach and reattach to sessions, keeping programs running in the background.
- **Window and Pane Splitting**:
    - Divide the terminal into multiple panes for multitasking.
- **Customization**:
    - Configure key bindings, color schemes, and status bars.
- **Scripting and Automation**:
    - Automate tasks using tmux commands and scripts.
- **Remote Work**:
    - Maintain persistent sessions over SSH connections.

### Basic Commands

- **Start tmux**:
    
    bash
    
    Copy code
    
    `tmux`
    
- **Create a New Session**:
    
    bash
    
    Copy code
    
    `tmux new -s session_name`
    
- **Detach from Session**:
    - Press `Ctrl + b`, then `d`.
- **List Sessions**:
    
    bash
    
    Copy code
    
    `tmux ls`
    
- **Attach to a Session**:
    
    bash
    
    Copy code
    
    `tmux attach -t session_name`
    
- **Split Pane Horizontally**:
    - `Ctrl + b`, then `"`
- **Split Pane Vertically**:
    - `Ctrl + b`, then `%`

### Configuration

- **tmux.conf**:
    - User-specific configurations stored in `~/.tmux.conf`.
- **Common Customizations**:
    - Change prefix key, set mouse support, customize status bar.

### Personal Insight

**tmux significantly enhances command-line productivity**, especially for developers and system administrators who rely on terminal-based workflows and need session persistence.

### Related Notes

- [[Shell Scripting Basics]]
- [[Remote Administration]]
- [[Neovim]]