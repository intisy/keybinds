## Emacs Keyboard Reference

Emacs is an extensible, self-documenting text editor with a philosophy of keeping your fingers on the home row. Keybindings use modifier key prefixes: **C-** means hold `Ctrl`, **M-** means hold `Alt` (Meta). Many commands use two-step key sequences called **prefix keys** (e.g., `C-x` followed by another key).

#### **The Absolute Essentials**

*   **Cancel Command (C-g):** Cancel whatever you're doing. The universal "get me out of here" key.
*   **Open File (C-x C-f):** Find/open a file.
*   **Save File (C-x C-s):** Save the current buffer.
*   **Save As (C-x C-w):** Write the buffer to a different file.
*   **Quit Emacs (C-x C-c):** Exit Emacs (prompts to save unsaved buffers).
*   **Undo (C-/):** Undo the last change. Also `C-_` or `C-x u`.
*   **Redo:** Undo the undo -- press `C-g` then `C-/` to start redoing.

#### **Movement**

*   **Character:** `C-f` (forward), `C-b` (backward).
*   **Word:** `M-f` (forward word), `M-b` (backward word).
*   **Line:** `C-a` (beginning of line), `C-e` (end of line).
*   **Sentence:** `M-a` (beginning of sentence), `M-e` (end of sentence).
*   **Paragraph:** `M-{` (backward paragraph), `M-}` (forward paragraph).
*   **Page:** `C-v` (scroll down), `M-v` (scroll up).
*   **Buffer:** `M-<` (beginning of buffer), `M->` (end of buffer).
*   **Go to Line (M-g g):** Jump to a specific line number.
*   **Recenter (C-l):** Center the screen on the cursor. Press again for top, then bottom.

#### **Editing**

*   **Kill (Cut) Line (C-k):** Kill from cursor to end of line. Repeat to kill the newline.
*   **Kill Word (M-d):** Kill forward one word.
*   **Kill Word Backward (M-Backspace):** Kill backward one word.
*   **Kill Region (C-w):** Kill the selected region (cut).
*   **Copy Region (M-w):** Copy the selected region without killing it.
*   **Yank (Paste) (C-y):** Paste the last killed text.
*   **Yank Pop (M-y):** After `C-y`, cycle through the kill ring (previous kills).
*   **Transpose Characters (C-t):** Swap the two characters around the cursor.
*   **Transpose Words (M-t):** Swap the two words around the cursor.
*   **Upcase Word (M-u):** Uppercase the current word.
*   **Downcase Word (M-l):** Lowercase the current word.
*   **Capitalize Word (M-c):** Capitalize the current word.

#### **Selection (Mark & Region)**

*   **Set Mark (C-Space):** Begin selecting text. Move the cursor to extend the selection.
*   **Select All (C-x h):** Select the entire buffer.
*   **Exchange Point and Mark (C-x C-x):** Swap cursor position with the other end of the selection.
*   **Rectangle Selection (C-x Space):** Start a rectangular region selection.

#### **Search & Replace**

*   **Incremental Search Forward (C-s):** Search forward. Press `C-s` again for next match.
*   **Incremental Search Backward (C-r):** Search backward.
*   **Regex Search (C-M-s):** Search forward with a regular expression.
*   **Query Replace (M-%):** Search and replace with confirmation for each match.
*   **Regex Replace (C-M-%):** Search and replace using regular expressions.

#### **Buffers & Windows**

*   **List Buffers (C-x C-b):** Show all open buffers.
*   **Switch Buffer (C-x b):** Switch to another buffer by name.
*   **Kill Buffer (C-x k):** Close a buffer.
*   **Split Horizontally (C-x 2):** Split the window into top and bottom.
*   **Split Vertically (C-x 3):** Split the window into left and right.
*   **Close Other Windows (C-x 1):** Make the current window the only one.
*   **Close This Window (C-x 0):** Close the current window (buffer stays open).
*   **Switch Window (C-x o):** Move cursor to the next window.
*   **Enlarge Window (C-x ^):** Make the current window taller.

#### **Help System**

*   **Help Prefix (C-h):** Opens the help system. Follow with:
    *   `t`: Tutorial.
    *   `k`: Describe what a key does.
    *   `f`: Describe a function.
    *   `v`: Describe a variable.
    *   `a`: Search for commands by keyword (apropos).
    *   `i`: Open the info manual.
    *   `m`: Describe the current mode.

#### **Modes & Commands**

*   **Execute Command (M-x):** Run any Emacs command by name (e.g., `M-x shell`, `M-x compile`).
*   **Shell Command (M-!):** Run a shell command and show output.
*   **Shell Command on Region (M-|):** Pipe the selected region through a shell command.
*   **Compile (M-x compile):** Run a compile command.
*   **Next Error (C-x `):** Jump to the next error in the compilation buffer.

#### **Dired (File Manager)**

*   **Open Dired (C-x d):** Open a directory listing.
*   **Inside Dired:**
    *   `Enter`: Open the file or directory.
    *   `d`: Mark for deletion.
    *   `x`: Execute deletions.
    *   `R`: Rename/move a file.
    *   `C`: Copy a file.
    *   `+`: Create a directory.
    *   `g`: Refresh the listing.
    *   `q`: Quit Dired.

#### **Customization**

*   **Config File:** `~/.emacs` or `~/.emacs.d/init.el`
*   **Example Keybinding:**
    ```elisp
    ;; Bind F5 to revert buffer
    (global-set-key (kbd "<f5>") 'revert-buffer)

    ;; Bind C-c c to compile
    (global-set-key (kbd "C-c c") 'compile)
    ```
*   **Popular Starter Kits:**
    *   **Doom Emacs**: Vim-style keybindings (Evil mode) with modern defaults.
    *   **Spacemacs**: Combines Emacs and Vim paradigms with a leader-key system.
    *   **Prelude**: Opinionated but lightweight Emacs starter kit.
