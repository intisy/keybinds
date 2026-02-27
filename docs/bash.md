### Bash / Readline Keybindings

These shortcuts work in Bash and any program using GNU Readline (most shells, Python REPL, etc.). They use Emacs-style bindings by default. Switch to vi mode with `set -o vi`.

#### **Movement**

*   **Move Forward One Character (Ctrl+f):** Move cursor forward.
*   **Move Backward One Character (Ctrl+b):** Move cursor backward.
*   **Move Forward One Word (Alt+f):** Jump to the end of the next word.
*   **Move Backward One Word (Alt+b):** Jump to the beginning of the previous word.
*   **Beginning of Line (Ctrl+a):** Move cursor to the start of the line.
*   **End of Line (Ctrl+e):** Move cursor to the end of the line.

#### **Editing**

*   **Delete Character Forward (Ctrl+d):** Delete the character under the cursor. Also sends EOF on an empty line.
*   **Delete Character Backward (Backspace or Ctrl+h):** Delete the character before the cursor.
*   **Kill to End of Line (Ctrl+k):** Cut from the cursor to the end of the line.
*   **Kill to Beginning of Line (Ctrl+u):** Cut from the cursor to the beginning of the line.
*   **Kill Word Forward (Alt+d):** Cut from the cursor to the end of the current word.
*   **Kill Word Backward (Ctrl+w):** Cut the word before the cursor.
*   **Yank (Paste) (Ctrl+y):** Paste the last killed text.
*   **Yank Pop (Alt+y):** After `Ctrl+y`, cycle through previous kills.
*   **Transpose Characters (Ctrl+t):** Swap the character under the cursor with the one before it.
*   **Transpose Words (Alt+t):** Swap the word under the cursor with the previous word.
*   **Upcase Word (Alt+u):** Uppercase from the cursor to the end of the word.
*   **Downcase Word (Alt+l):** Lowercase from the cursor to the end of the word.
*   **Capitalize Word (Alt+c):** Capitalize the current word.
*   **Undo (Ctrl+_ or Ctrl+x Ctrl+u):** Undo the last edit.

#### **History**

*   **Previous Command (Ctrl+p or Up):** Scroll to the previous command.
*   **Next Command (Ctrl+n or Down):** Scroll to the next command.
*   **Reverse Search (Ctrl+r):** Incrementally search backward through history. Press again to find the next match.
*   **Forward Search (Ctrl+s):** Search forward through history (may need `stty -ixon` first).
*   **Run Last Command (!!):** Execute the previous command.
*   **Run by Prefix (!prefix):** Run the most recent command starting with `prefix`.
*   **Last Argument (Alt+. or !$):** Insert the last argument of the previous command.
*   **Accept Line (Enter or Ctrl+j):** Execute the current command.
*   **Clear History Line (Ctrl+g):** Abort the current history search or editing.

#### **Control**

*   **Clear Screen (Ctrl+l):** Clear the terminal, keeping the current line.
*   **Interrupt (Ctrl+c):** Send SIGINT, cancelling the current command.
*   **EOF / Exit (Ctrl+d):** Send EOF. On an empty prompt, exits the shell.
*   **Suspend (Ctrl+z):** Suspend the current foreground process (resume with `fg`).
*   **Stop Output (Ctrl+s):** Pause terminal output.
*   **Resume Output (Ctrl+q):** Resume terminal output after `Ctrl+s`.

#### **Completion**

*   **Tab Completion (Tab):** Auto-complete the current word (file, command, variable).
*   **Show Completions (Tab Tab):** Press Tab twice to list all possible completions.
*   **List Completions (Alt+?):** Display all possible completions.
*   **Insert Completions (Alt+*):** Insert all possible completions.

#### **Customization**

*   **Config File:** `~/.inputrc` (Readline) and `~/.bashrc` (Bash).
*   **Switch to Vi Mode:**
    ```bash
    set -o vi    # In .bashrc
    # or
    set editing-mode vi  # In .inputrc
    ```
*   **Example .inputrc:**
    ```bash
    # Case-insensitive completion
    set completion-ignore-case on

    # Show all completions on first Tab
    set show-all-if-ambiguous on

    # Color completions by file type
    set colored-stats on

    # Custom binding
    "\e[A": history-search-backward   # Up arrow searches history
    "\e[B": history-search-forward    # Down arrow searches history
    ```
