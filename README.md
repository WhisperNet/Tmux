# TMUX: Terminal Multiplexer

TMUX is a powerful tool that allows you to manage multiple terminal sessions within a single window. This guide covers the basics and some customization tips to enhance your terminal experience.

## Getting Started

### Installation

On Debian-based systems, you can install tmux using:

```bash
sudo apt install tmux
```

### Basic Usage

1. **Start a new session:**
   ```bash
   tmux
   ```

2. **The Prefix Key:**
   - TMUX uses a prefix key to distinguish its commands from regular terminal input.
   - The default prefix is `Ctrl+b`. Press this before any TMUX command.


3. **Detach from a session:**
   - Press the prefix, then `d`

4. **List all sessions:**
   ```bash
   tmux list-sessions
   ```
   - Or use the shortcut: prefix + `s`

5. **Attach to a session:**
   ```bash
   tmux attach -t [session-name]
   # Shorthand version:
   tmux a -t [session-name]
   ```
   - To attach to the most recent session:
     ```bash
     tmux a
     ```

6. **Rename a session:**
   - prefix + `$`

## Managing Panes and Windows

### Panes

- **Split vertically:** prefix + `%`
- **Split horizontally:** prefix + `"`

- **Navigate panes:** prefix + arrow keys
- **Close a pane:** 
  - Type `exit` or
  - prefix + `x`

### Windows

- **Create a new window:** prefix + `c`
- **Navigate windows:** 
  - Previous: prefix + `p`
  - Next: prefix + `n`
- **Close a window:** prefix + `&`
- **Rename a window:** prefix + `,`

## Customization

While TMUX works great out of the box, customizing it can improve your workflow and aesthetics.

1. Create a config file:
   ```bash
   nano ~/.tmux.conf
   ```

2. Example customizations:
   ```
   # Use C-j and C-f as prefix keys
   set-option -g prefix C-j
   set-option -g prefix2 C-f

   # Easier window splitting
   bind-key v split-window -h
   bind-key h split-window -v
   ```

For a quick start with great customizations, check out this popular config: [gpakosz/.tmux](https://github.com/gpakosz/.tmux)

Remember, the beauty of TMUX lies in its flexibility. Experiment with different settings to find what works best for you. Happy multiplexing!
