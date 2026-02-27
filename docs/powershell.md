### PowerShell Keybindings

PowerShell uses the PSReadLine module for command-line editing. These shortcuts work in PowerShell 5.1+ and PowerShell 7+ (cross-platform). The default editing mode is Windows-style; Emacs and Vi modes are also available.

#### **Movement**

*   **Beginning of Line (Home):** Move cursor to the start of the line.
*   **End of Line (End):** Move cursor to the end of the line.
*   **Forward One Word (Ctrl+Right):** Jump to the start of the next word.
*   **Backward One Word (Ctrl+Left):** Jump to the start of the previous word.
*   **Forward One Character (Right):** Move cursor forward.
*   **Backward One Character (Left):** Move cursor backward.

#### **Editing**

*   **Delete Character (Delete):** Delete the character under the cursor.
*   **Backspace (Backspace):** Delete the character before the cursor.
*   **Delete Word Forward (Ctrl+Delete):** Delete from the cursor to the end of the current word.
*   **Delete Word Backward (Ctrl+Backspace):** Delete the word before the cursor.
*   **Delete to End of Line (Ctrl+End):** Delete from the cursor to the end of the line.
*   **Delete to Beginning of Line (Ctrl+Home):** Delete from the cursor to the beginning of the line.
*   **Cut Selection (Ctrl+X):** Cut the selected text.
*   **Copy Selection (Ctrl+C):** Copy the selected text (when text is selected; otherwise sends break).
*   **Paste (Ctrl+V):** Paste from the clipboard.
*   **Select All (Ctrl+A):** Select the entire command line.
*   **Undo (Ctrl+Z):** Undo the last edit.
*   **Redo (Ctrl+Y):** Redo the last undone edit.

#### **History**

*   **Previous Command (Up):** Scroll to the previous command in history.
*   **Next Command (Down):** Scroll to the next command in history.
*   **Search History (Ctrl+R):** Reverse incremental search through history.
*   **Search History Forward (Ctrl+S):** Forward incremental search through history.
*   **History by Prefix (F8):** Search history for commands starting with the current input.
*   **Previous History by Prefix (Shift+F8):** Search backward by prefix.
*   **First Command (Alt+<):** Go to the first command in history.
*   **Last Command (Alt+>):** Go to the last (most recent) command in history.

#### **Completion**

*   **Tab Completion (Tab):** Auto-complete the current word. Press repeatedly to cycle through options.
*   **Reverse Tab (Shift+Tab):** Cycle backward through completion options.
*   **Show All Completions (Ctrl+Space):** Display a menu of all possible completions.
*   **Menu Complete (Tab in MenuComplete mode):** Show completions in a menu you can navigate with arrow keys.

#### **Prediction & IntelliSense**

*   **Accept Prediction (Right Arrow):** Accept the inline prediction (PSReadLine 2.1+).
*   **Accept Next Word (Ctrl+F):** Accept the next word from the prediction.
*   **Show Tooltip (F1):** Show the full help for the current command.
*   **Show Parameter Help (Alt+H):** Display parameter information for the current command.

#### **Control**

*   **Cancel (Ctrl+C):** Cancel the current command (when no text is selected).
*   **Clear Screen (Ctrl+L or `cls`):** Clear the terminal.
*   **Exit (exit or Ctrl+D):** Close the PowerShell session.
*   **Abort Line (Esc):** Clear the current line.

#### **Selection**

*   **Select Forward (Shift+Right):** Extend selection one character to the right.
*   **Select Backward (Shift+Left):** Extend selection one character to the left.
*   **Select Word Forward (Ctrl+Shift+Right):** Extend selection to the next word.
*   **Select Word Backward (Ctrl+Shift+Left):** Extend selection to the previous word.
*   **Select to End (Shift+End):** Select from cursor to end of line.
*   **Select to Start (Shift+Home):** Select from cursor to start of line.

#### **Multiline Editing**

*   **New Line (Shift+Enter):** Insert a new line without executing.
*   **Execute (Enter):** Execute the command (if the syntax is complete).

#### **Customization**

*   **Config File:** Edit your PowerShell profile (`$PROFILE`).
*   **View Current Bindings:** `Get-PSReadLineKeyHandler`
*   **Switch Edit Mode:**
    ```powershell
    Set-PSReadLineOption -EditMode Emacs   # Emacs-style
    Set-PSReadLineOption -EditMode Vi       # Vim-style
    Set-PSReadLineOption -EditMode Windows  # Default
    ```
*   **Custom Keybinding:**
    ```powershell
    # Bind Ctrl+D to delete character (Unix-like behavior)
    Set-PSReadLineKeyHandler -Key Ctrl+d -Function DeleteChar

    # Bind F2 to switch between prediction sources
    Set-PSReadLineKeyHandler -Key F2 -Function SwitchPredictionView

    # Enable prediction from history
    Set-PSReadLineOption -PredictionSource History
    Set-PSReadLineOption -PredictionViewStyle ListView
    ```
*   **Profile Location:** `$PROFILE` typically points to:
    *   Windows: `~\Documents\PowerShell\Microsoft.PowerShell_profile.ps1`
    *   Linux/macOS: `~/.config/powershell/Microsoft.PowerShell_profile.ps1`
