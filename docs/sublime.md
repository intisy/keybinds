### Sublime Text Keybindings

Sublime Text is a fast, lightweight code editor with powerful multi-cursor editing and a command palette. Keybindings shown use `Ctrl` for Windows/Linux; substitute `Cmd` on macOS.

#### **General**

*   **Command Palette (Ctrl+Shift+P):** Access any command by name. The most important shortcut.
*   **Quick Open File (Ctrl+P):** Fuzzy-find and open any file in the project.
*   **Go to Symbol (Ctrl+R):** Jump to a function, class, or heading in the current file.
*   **Go to Symbol in Project (Ctrl+Shift+R):** Jump to a symbol across the entire project.
*   **Go to Line (Ctrl+G):** Jump to a specific line number.
*   **Toggle Sidebar (Ctrl+K, Ctrl+B):** Show or hide the file sidebar.
*   **Console (Ctrl+`):** Open the built-in Python console.

#### **Editing**

*   **Duplicate Line (Ctrl+Shift+D):** Duplicate the current line or selection.
*   **Delete Line (Ctrl+Shift+K):** Delete the entire current line.
*   **Move Line Up/Down (Ctrl+Shift+Up/Down):** Move the current line up or down.
*   **Join Lines (Ctrl+J):** Join the current line with the line below.
*   **Toggle Comment (Ctrl+/):** Comment or uncomment the current line or selection.
*   **Block Comment (Ctrl+Shift+/):** Toggle a block comment around the selection.
*   **Indent (Ctrl+]):** Indent the current line or selection.
*   **Unindent (Ctrl+[):** Unindent the current line or selection.
*   **Sort Lines (F9):** Sort the selected lines alphabetically.
*   **Upcase (Ctrl+K, Ctrl+U):** Convert selection to uppercase.
*   **Downcase (Ctrl+K, Ctrl+L):** Convert selection to lowercase.
*   **Undo (Ctrl+Z):** Undo.
*   **Redo (Ctrl+Y or Ctrl+Shift+Z):** Redo.
*   **Soft Undo (Ctrl+U):** Undo the last cursor movement or selection change.

#### **Multi-Cursor & Selection**

*   **Add Cursor (Ctrl+Click):** Place an additional cursor.
*   **Add Cursor Above/Below (Ctrl+Alt+Up/Down):** Add a cursor on the line above or below.
*   **Select Word (Ctrl+D):** Select the current word. Press again to select the next occurrence.
*   **Skip Occurrence (Ctrl+K, Ctrl+D):** Skip the current occurrence and select the next.
*   **Select All Occurrences (Alt+F3):** Select all occurrences of the current word.
*   **Split Selection into Lines (Ctrl+Shift+L):** Add a cursor to the end of each selected line.
*   **Expand Selection to Line (Ctrl+L):** Select the entire current line. Repeat to add more lines.
*   **Expand Selection to Brackets (Ctrl+Shift+M):** Expand the selection to the enclosing brackets.
*   **Expand Selection to Scope (Ctrl+Shift+Space):** Expand selection to the current scope.

#### **Search & Replace**

*   **Find (Ctrl+F):** Open the find bar.
*   **Find and Replace (Ctrl+H):** Open find and replace.
*   **Find in Files (Ctrl+Shift+F):** Search across all files in the project.
*   **Find Next (F3 or Enter):** Jump to the next match.
*   **Find Previous (Shift+F3):** Jump to the previous match.
*   **Use Selection for Find (Ctrl+E):** Use the current selection as the search term.
*   **Toggle Regex (Alt+R):** Toggle regex mode in the search bar.

#### **Tabs & Panes**

*   **New Tab (Ctrl+N):** Open a new tab.
*   **Close Tab (Ctrl+W):** Close the current tab.
*   **Reopen Tab (Ctrl+Shift+T):** Reopen the last closed tab.
*   **Next Tab (Ctrl+Page Down):** Switch to the next tab.
*   **Previous Tab (Ctrl+Page Up):** Switch to the previous tab.
*   **Go to Tab (Alt+1-9):** Jump to tab 1 through 9.
*   **Split into 2 Columns (Alt+Shift+2):** Split the editor into two panes.
*   **Split into 3 Columns (Alt+Shift+3):** Split into three panes.
*   **Split into 2 Rows (Alt+Shift+8):** Split into two rows.
*   **Grid (Alt+Shift+5):** Split into a 2x2 grid.
*   **Single Pane (Alt+Shift+1):** Return to a single pane.
*   **Move File to Group (Ctrl+Shift+1-4):** Move the current file to pane 1-4.

#### **Code Navigation**

*   **Go to Definition (F12):** Jump to the definition of the symbol under the cursor.
*   **Go to Reference (Shift+F12):** Find all references to the symbol.
*   **Go Back (Alt+-):** Navigate back after a jump.
*   **Go Forward (Alt+Shift+-):** Navigate forward.
*   **Fold (Ctrl+Shift+[):** Fold the current code block.
*   **Unfold (Ctrl+Shift+]):** Unfold the current code block.
*   **Fold All (Ctrl+K, Ctrl+0):** Fold all code blocks.
*   **Unfold All (Ctrl+K, Ctrl+J):** Unfold all code blocks.

#### **Build & Run**

*   **Build (Ctrl+B):** Run the current build system.
*   **Build With... (Ctrl+Shift+B):** Choose a build system and run.
*   **Cancel Build (Ctrl+Break):** Cancel a running build.

#### **Customization**

*   **Keybindings File:** Open via `Preferences > Key Bindings`. User keybindings go in the right pane.
*   **Example Keybinding:**
    ```json
    [
        { "keys": ["ctrl+shift+r"], "command": "reveal_in_side_bar" },
        { "keys": ["f5"], "command": "build" }
    ]
    ```
*   **Package Control:** Install via `Ctrl+Shift+P` > "Install Package Control", then `Ctrl+Shift+P` > "Package Control: Install Package" to browse thousands of extensions.
