### Zed Keybindings

Zed is a high-performance, GPU-accelerated code editor with built-in collaboration, AI assistance, and language server support. Keybindings shown use `Ctrl` for Linux; substitute `Cmd` on macOS.

#### **General**

*   **Command Palette (Ctrl+Shift+P):** Access any command by name.
*   **Quick Open File (Ctrl+P):** Fuzzy-find and open a file in the project.
*   **Toggle File Panel (Ctrl+Shift+E):** Show or hide the project panel sidebar.
*   **Toggle Terminal (Ctrl+`):** Open or close the integrated terminal.
*   **Toggle AI Panel (Ctrl+Shift+A):** Open the AI assistant panel.
*   **Settings (Ctrl+,):** Open the settings editor.

#### **Editing**

*   **Duplicate Line (Ctrl+Shift+D):** Duplicate the current line or selection.
*   **Delete Line (Ctrl+Shift+K):** Delete the entire current line.
*   **Move Line Up/Down (Alt+Up/Down):** Move the current line or selection up or down.
*   **Toggle Comment (Ctrl+/):** Comment or uncomment the current line or selection.
*   **Indent/Unindent (Tab/Shift+Tab):** Indent or unindent the selection.
*   **Join Lines (Ctrl+J):** Join the current line with the next.
*   **Undo (Ctrl+Z):** Undo.
*   **Redo (Ctrl+Shift+Z):** Redo.
*   **Format Document (Ctrl+Shift+I):** Format the current buffer using the language server.
*   **Rename Symbol (F2):** Rename the symbol under the cursor across the project.

#### **Multi-Cursor & Selection**

*   **Add Cursor (Ctrl+Click):** Place an additional cursor.
*   **Add Cursor Above/Below (Ctrl+Alt+Up/Down):** Add a cursor on the line above or below.
*   **Select Next Occurrence (Ctrl+D):** Select the next occurrence of the current word.
*   **Select All Occurrences (Ctrl+Shift+L):** Select all occurrences of the current selection.
*   **Expand Selection (Ctrl+Shift+Space):** Expand the selection to the enclosing syntax node.
*   **Select Line (Ctrl+L):** Select the entire current line.

#### **Navigation**

*   **Go to Definition (F12):** Jump to the definition.
*   **Go to Type Definition (Ctrl+F12):** Jump to the type definition.
*   **Go to References (Shift+F12):** Find all references.
*   **Go to Symbol (Ctrl+Shift+O):** Jump to a symbol in the current file.
*   **Go to Line (Ctrl+G):** Jump to a line number.
*   **Go Back (Ctrl+-):** Navigate back.
*   **Go Forward (Ctrl+Shift+-):** Navigate forward.
*   **Next Problem (F8):** Jump to the next diagnostic.
*   **Previous Problem (Shift+F8):** Jump to the previous diagnostic.
*   **Outline Panel (Ctrl+Shift+O):** View the document outline.

#### **Search & Replace**

*   **Find (Ctrl+F):** Search in the current file.
*   **Find and Replace (Ctrl+H):** Search and replace in the current file.
*   **Find in Project (Ctrl+Shift+F):** Search across all files.
*   **Next Match (Enter or F3):** Jump to the next match.
*   **Previous Match (Shift+Enter or Shift+F3):** Jump to the previous match.

#### **Panes & Tabs**

*   **Split Right (Ctrl+K, Ctrl+\):** Split the editor to the right.
*   **Close Tab (Ctrl+W):** Close the current tab.
*   **Reopen Tab (Ctrl+Shift+T):** Reopen the last closed tab.
*   **Next Tab (Ctrl+Tab):** Switch to the next tab.
*   **Previous Tab (Ctrl+Shift+Tab):** Switch to the previous tab.
*   **Focus Next Pane (Ctrl+K, Ctrl+Right):** Move focus to the next pane.
*   **Focus Previous Pane (Ctrl+K, Ctrl+Left):** Move focus to the previous pane.

#### **Collaboration**

*   **Share Project:** Invite collaborators to edit in real time via the collaboration panel.
*   **Follow Participant:** Click on a collaborator's avatar to follow their cursor.
*   **Unfollow (Escape):** Stop following a collaborator.

#### **Customization**

*   **Keymap File:** Open via `Ctrl+Shift+P` > "Open Key Bindings".
*   **Settings File:** `~/.config/zed/settings.json` (Linux) or `~/Library/Application Support/Zed/settings.json` (macOS).
*   **Example Keybinding:**
    ```json
    [
      {
        "bindings": {
          "ctrl-shift-r": "project_panel::RevealInFileManager"
        }
      }
    ]
    ```
