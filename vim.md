## The Ultimate Vim Keyboard Reference

Vim's philosophy is based on **modal editing** and **composable commands**. This means you combine operators with motions to perform complex tasks efficiently. Mastering this concept is the key to unlocking Vim's power.

#### **Core Concepts**

*   **Modes:**
    *   **Normal:** The default mode for navigation, manipulation, and entering other modes. **Press `Esc` to return here.**
    *   **Insert:** For typing new text.
    *   **Visual:** For selecting text (character, line, or block).
    *   **Command-Line:** For running commands that start with `:` (e.g., save, quit), `/` (search), or `?` (search).

*   **The Command Structure: `[operator][count][motion]`**
    *   **Operator:** An action, like `d` (delete) or `y` (yank/copy).
    *   **Count:** A number to repeat the action/motion (e.g., `8`).
    *   **Motion:** A movement command (e.g., `k` for up, `w` for word).
    *   **Example:** `d2w` means **d**elete **2** **w**ords.

#### **The Absolute Essentials**

*   **Enter Insert Mode:**
    *   `i`: **i**nsert before the cursor.
    *   `a`: **a**ppend after the cursor.
    *   `I`: Insert at the beginning of the line.
    *   `A`: Append at the end of the line.
    *   `o`: Open a new line below and enter Insert mode.
    *   `O`: Open a new line above and enter Insert mode.
*   **Return to Normal Mode:** `Esc` or `Ctrl+[`
*   **Undo/Redo:** `u` (undo), `Ctrl+r` (redo).
*   **Saving & Quitting:**
    *   `:w`: **w**rite (save).
    *   `:q`: **q**uit.
    *   `:wq` or `:x`: Write and quit.
    *   `:q!`: Quit without saving changes.
    *   `:w [filename]`: Write to a new file (Save As).

#### **Movement (Normal Mode)**

*   **Basic:** `h` (left), `j` (down), `k` (up), `l` (right).
*   **With a Count:** `8k` (move up 8 lines), `4l` (move right 4 characters).
*   **Word:**
    *   `w`: Move to the start of the next **w**ord.
    *   `b`: Move **b**ack to the start of the previous word.
    *   `e`: Move to the **e**nd of the current word.
    *   `W`, `B`, `E`: Same as above, but for space-separated "WORDS".
*   **Line:**
    *   `0`: Move to the first column of the line.
    *   `^`: Move to the first non-whitespace character.
    *   `$`: Move to the end of the line.
*   **File & Screen:**
    *   `gg`: Go to the first line of the file.
    *   `G`: Go to the last line of the file.
    *   `[number]G`: Go to line `[number]` (e.g., `50G`).
    *   `H`: Move to the **H**igh/top of the screen.
    *   `M`: Move to the **M**iddle of the screen.
    *   `L`: Move to the **L**ow/bottom of the screen.
*   **Paging:**
    *   `Ctrl+d` / `Ctrl+f`: Move **d**own/ **f**orward a half/full page.
    *   `Ctrl+u` / `Ctrl+b`: Move **u**p/ **b**ackward a half/full page.
*   **Text Objects:**
    *   `(` / `)`: Move to the previous/next sentence.
    *   `{` / `}`: Move to the previous/next paragraph.
    *   `%`: Jump to a matching bracket, parenthesis, or brace (`[]`, `()`, `{}`).

#### **Editing Text (Normal Mode)**

*   **Delete/Cut (`d`):**
    *   `dd`: Delete the current line. `5dd` deletes 5 lines.
    *   `dw`: Delete one word.
    *   `d$`: Delete to the end of the line.
    *   `x`: Delete character under the cursor. `5x` deletes 5 characters.
    *   `X`: Backspace (delete character before the cursor).
    *   `"_d`: Delete without copying (black hole register).
*   **Yank/Copy (`y`):**
    *   `yy`: Yank the current line. `2yy` yanks 2 lines.
    *   `yw`: Yank one word.
    *   `y$`: Yank to the end of the line.
*   **Paste (`p`):**
    *   `p`: **p**aste after the cursor.
    *   `P`: **P**aste before the cursor.
*   **Change (`c`):** Deletes text and enters Insert Mode.
    *   `cc` or `S`: Change the entire line.
    *   `cw`: Change word.
    *   `c$`: Change to the end of the line.
    *   `s`: Substitute one character and enter Insert mode.
*   **Replace (`r`):**
    *   `r[char]`: **r**eplace the character under the cursor with `[char]`.
    *   `R`: Enter **R**eplace mode, overwriting text until `Esc` is pressed.
*   **Indentation:**
    *   `>>` / `<<`: Indent / un-indent the current line.
    *   `=motion`: Auto-indent a range (e.g., `=G`, `=}`).
*   **Case Changing:**
    *   `~`: Toggle case of the character under the cursor.
    *   `g~motion`: Toggle case over a range.
    *   `gu[motion]`: Lowercase over motion.
    *   `gU[motion]`: Uppercase over motion.
*   **Other:**
    *   `.`: **Repeat the last single change**.
    *   `J`: **J**oin the line below to the current one.

#### **Registers (Clipboards)**

*   `"*` / `"+`: System clipboard (copy/paste between Vim and OS).
*   `"0`: Default yank register.
*   `"a`–`"z`: Named registers.
*   `"_`: Black hole register (delete without yanking).
*   Use `"` + `[register]` with any command:
    *   Example: `"ap` pastes from register `a`, `"_dd` deletes without overwriting yank.

#### **Visual Mode (Selecting Text)**

Enter from Normal Mode, then use a motion to select, and an operator (`d`, `y`, `c`, `>`) to act on the selection.

*   **Enter Modes:**
    *   `v`: Start **v**isual mode (character-wise).
    *   `V`: Start line-wise **V**isual mode.
    *   `Ctrl+v`: Start block-wise (column) Visual mode.
*   **Example (Block Mode):**
    1.  Go to the first character of a block of lines you want to comment out.
    2.  Press `Ctrl+v`.
    3.  Press `j` several times to select down the column.
    4.  Press `I` (Insert at beginning of line selection).
    5.  Type your comment character (e.g., `# `).
    6.  Press `Esc`. The character will be inserted on all selected lines.

#### **Command-Line Mode**

*   **Search (`/`, `?`):**
    *   `/pattern`: Search forward.
    *   `?pattern`: Search backward.
    *   `n` / `N`: Go to the next / previous occurrence.
    *   `*` / `#`: Search forward / backward for the word currently under the cursor.
*   **Search and Replace:**
    *   `:%s/old/new/g`: In the whole file (`%`), **s**ubstitute all (`g`) occurrences of `old` with `new`.
    *   Flags: Add `c` for **c**onfirm each replacement (`/gc`). Add `i` for case-**i**nsensitive (`/gi`).
*   **Shell Commands:** `:! [command]` (e.g., `:!ls -la`).
*   **Read File:** `:r [filename]` (reads content of `[filename]` into the buffer).
*   **Help:** `:help [topic]` (e.g., `:help motion`).
*   **Repeat Last Command:** `@:` re-runs the last command-line command.

#### **Window & Tab Management**

*   **Window Splits:**
    *   `:split` or `Ctrl+w s`: Horizontal split.
    *   `:vsplit` or `Ctrl+w v`: Vertical split.
    *   `Ctrl+w` + `h/j/k/l`: Move between splits.
    *   `Ctrl+w w`: Cycle through windows.
    *   `Ctrl+w q`: Close the active window. `:qa` to quit all.
*   **Tabs:**
    *   `:tabnew` or `:tabe [filename]`: Open a new tab.
    *   `gt`: Go to the next tab.
    *   `gT`: Go to the previous tab.
    *   `[number]gt`: Go to tab number `[number]`.
    *   `:tabc`: Close the current tab.

#### **Advanced & Miscellaneous**

*   **Macros:**
    *   `q[register]`: Start recording a macro into a register (e.g., `qa`).
    *   `q`: Stop recording.
    *   `@[register]`: Execute the macro (e.g., `@a`). `@@` to repeat the last executed macro.
*   **Marks:**
    *   `m[char]`: Create a **m**ark named `[char]` at the cursor position (e.g., `ma`).
    *   `` `[char] ``: Jump to the exact position of the mark.
    *   `'[char]`: Jump to the beginning of the line containing the mark.
*   **Repeat Tools:**
    *   `.`: Repeat the last change.
    *   `@@`: Repeat the last macro.
    *   `@:`: Repeat the last command-line command.
    *   `gv`: Reselect the last visual selection.

#### **Customization**

*   **Your Config File:**
    *   Vim: `~/.vimrc`
    *   Neovim: `~/.config/nvim/init.vim`

*   **Recommended Settings:**
    ```vim
    set number              " Show line numbers
    set relativenumber      " Relative line numbers
    set tabstop=4           " Display width of tab character
    set shiftwidth=4        " Indent size
    set expandtab           " Convert tabs to spaces
    set clipboard=unnamedplus " Use system clipboard
    syntax on               " Enable syntax highlighting
    ```

*   **Example Mappings:**
    ```vim
    nnoremap <Space> :nohlsearch<CR>   " Clear search highlight
    nnoremap <leader>w :w<CR>          " Save with <leader>w
    ```
   Your personal settings and custom keybinds live in `~/.vimrc` (for Vim) or `~/.config/nvim/init.vim` (for Neovim). Here you can `set number` for line numbers, change color schemes, and remap any key to any action.