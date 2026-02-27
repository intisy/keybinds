### tmux Keybindings

tmux is a terminal multiplexer that lets you run multiple terminal sessions inside a single window, detach and reattach sessions, and split your terminal into panes. All tmux keybindings start with the **prefix key**, which is `Ctrl+b` by default. Press the prefix, release it, then press the next key.

#### **The Most Important Shortcuts**

*   **Prefix Key (Ctrl+b):** Must be pressed before every tmux command below.
*   **Create New Window (Prefix c):** Open a new window (like a tab).
*   **Detach Session (Prefix d):** Detach from the current session. The session keeps running in the background.
*   **Split Horizontally (Prefix "):** Split the current pane into top and bottom.
*   **Split Vertically (Prefix %):** Split the current pane into left and right.
*   **Command Prompt (Prefix :):** Open the tmux command prompt for running tmux commands directly.

#### **Sessions**

*   **New Session:** `tmux new -s name` (from the shell, not inside tmux).
*   **List Sessions:** `tmux ls` (from the shell) or `Prefix s` (inside tmux -- interactive session picker).
*   **Attach to Session:** `tmux attach -t name` (from the shell).
*   **Detach (Prefix d):** Detach from the current session.
*   **Rename Session (Prefix $):** Rename the current session.
*   **Switch Session (Prefix s):** Interactive session and window tree picker.
*   **Switch to Last Session (Prefix L):** Jump back to the previous session.

#### **Windows (Tabs)**

*   **New Window (Prefix c):** Create a new window.
*   **Next Window (Prefix n):** Switch to the next window.
*   **Previous Window (Prefix p):** Switch to the previous window.
*   **Select Window (Prefix 0-9):** Jump to window 0 through 9.
*   **Find Window (Prefix f):** Search for a window by name.
*   **Rename Window (Prefix ,):** Rename the current window.
*   **Close Window (Prefix &):** Close the current window (prompts for confirmation).
*   **Window List (Prefix w):** Interactive window picker (shows all sessions and windows).
*   **Move Window (Prefix .):** Move the current window to a new index.
*   **Last Window (Prefix l):** Switch to the last active window.

#### **Panes**

*   **Split Horizontal (Prefix "):** Split the pane top/bottom.
*   **Split Vertical (Prefix %):** Split the pane left/right.
*   **Navigate Panes (Prefix Arrow Keys):** Move focus to the pane in that direction.
*   **Cycle Panes (Prefix o):** Move to the next pane.
*   **Toggle Pane Zoom (Prefix z):** Zoom the current pane to fill the entire window. Press again to restore.
*   **Close Pane (Prefix x):** Close the current pane (prompts for confirmation). Or just type `exit`.
*   **Swap Pane (Prefix {):** Swap the current pane with the previous one.
*   **Swap Pane (Prefix }):** Swap the current pane with the next one.
*   **Rotate Panes (Prefix Ctrl+o):** Rotate panes within the window.
*   **Toggle Layouts (Prefix Space):** Cycle through pane layout presets (even-horizontal, even-vertical, main-horizontal, main-vertical, tiled).
*   **Resize Pane (Prefix Alt+Arrow Keys):** Resize the pane in 5-cell increments.
*   **Resize Pane (Prefix Ctrl+Arrow Keys):** Resize the pane in 1-cell increments.
*   **Display Pane Numbers (Prefix q):** Show pane numbers briefly. Press a number to jump to that pane.
*   **Break Pane (Prefix !):** Move the current pane into a new window.
*   **Convert Window to Pane (Prefix :join-pane -t [target]):** Join a window as a pane in another window.

#### **Copy Mode (Scrollback)**

*   **Enter Copy Mode (Prefix [):** Enter copy mode to scroll through history and copy text.
*   **Navigation (in copy mode):**
    *   Arrow keys, `Page Up/Down` for scrolling.
    *   If using vi mode: `h/j/k/l`, `w/b`, `0/$`, `gg/G`, `/` for search.
*   **Start Selection (Space):** Begin selecting text (in vi mode).
*   **Copy Selection (Enter):** Copy the selected text to the tmux buffer.
*   **Paste Buffer (Prefix ]):** Paste the most recently copied text.
*   **Exit Copy Mode (q or Esc):** Leave copy mode.
*   **Search Forward (Prefix /):** Search forward in the scrollback (in copy mode).
*   **Search Backward (Prefix ?):** Search backward (in copy mode).

#### **Miscellaneous**

*   **Show Clock (Prefix t):** Display a clock in the current pane.
*   **List Keybindings (Prefix ?):** Show all current key bindings.
*   **Reload Config (Prefix : then `source-file ~/.tmux.conf`):** Reload the tmux configuration.

#### **Customization**

*   **Config File:** `~/.tmux.conf`
*   **Common Customizations:**
    ```bash
    # Change prefix to Ctrl+a (more ergonomic)
    unbind C-b
    set -g prefix C-a
    bind C-a send-prefix

    # Split panes with | and -
    bind | split-window -h
    bind - split-window -v

    # Enable mouse support
    set -g mouse on

    # Vi-style copy mode
    setw -g mode-keys vi

    # Navigate panes with vim keys
    bind h select-pane -L
    bind j select-pane -D
    bind k select-pane -U
    bind l select-pane -R

    # Start window numbering at 1
    set -g base-index 1
    setw -g pane-base-index 1

    # Faster escape time (for Vim/Neovim users)
    set -sg escape-time 10

    # Increase scrollback buffer
    set -g history-limit 50000
    ```
