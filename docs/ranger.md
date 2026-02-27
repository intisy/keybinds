### ranger Keybindings

ranger is a terminal file manager with Vim-style keybindings and a three-column layout (parent directory, current directory, file preview). It supports file previews, bookmarks, tabs, and bulk operations.

#### **Navigation**

*   **Move Down (j):** Move the cursor down.
*   **Move Up (k):** Move the cursor up.
*   **Enter Directory (l or Enter):** Open the selected directory or file.
*   **Go to Parent (h):** Navigate to the parent directory.
*   **Go to Top (gg):** Jump to the first item.
*   **Go to Bottom (G):** Jump to the last item.
*   **Half Page Down (Ctrl+d):** Scroll half a page down.
*   **Half Page Up (Ctrl+u):** Scroll half a page up.
*   **Go Home (~):** Navigate to the home directory.
*   **Go to Root (/):** Not a navigation shortcut; this opens search. Use `cd /` via `:cd /`.
*   **Jump Back (H):** Go to the previous directory in history.
*   **Jump Forward (L):** Go to the next directory in history.

#### **File Operations**

*   **Copy/Yank (yy):** Mark the current file for copying.
*   **Cut (dd):** Mark the current file for moving.
*   **Paste (pp):** Paste (copy or move) the marked files to the current directory.
*   **Paste Overwrite (po):** Paste and overwrite existing files.
*   **Delete (dD):** Delete the selected files (prompts for confirmation).
*   **Rename (cw):** Rename the current file.
*   **Rename Append (A):** Rename, placing the cursor at the end of the filename.
*   **Rename Insert (I):** Rename, placing the cursor at the beginning of the filename.
*   **Create Directory (:mkdir name):** Create a new directory.
*   **Create File (:touch name):** Create a new file.
*   **Change Permissions (chmod):** Via `:chmod` command.

#### **Selection**

*   **Toggle Selection (Space):** Select or deselect the current file and move down.
*   **Select All (V or :mark_all):** Mark all files in the current directory.
*   **Invert Selection (v):** Invert the current selection.
*   **Unselect All (uv):** Deselect all files.

#### **Tabs**

*   **New Tab (Ctrl+n or :tab_new):** Open a new tab.
*   **Close Tab (Ctrl+w or :tab_close):** Close the current tab.
*   **Next Tab (Tab):** Switch to the next tab.
*   **Previous Tab (Shift+Tab):** Switch to the previous tab.
*   **Go to Tab (Alt+1-9):** Jump to tab 1 through 9.

#### **Bookmarks**

*   **Set Bookmark (m + key):** Create a bookmark with the given key.
*   **Go to Bookmark (' + key):** Jump to a bookmarked directory.
*   **Delete Bookmark (um + key):** Remove a bookmark.

#### **Search & Filter**

*   **Search (/):** Search for a file by name in the current directory.
*   **Next Match (n):** Jump to the next search match.
*   **Previous Match (N):** Jump to the previous search match.
*   **Filter (zf):** Filter the visible files by a pattern.
*   **Find (f + chars):** Quickly jump to files starting with the given characters.

#### **Sorting**

*   **Sort Menu (o):** Open the sort menu, then:
    *   `n`: Sort by name.
    *   `s`: Sort by size.
    *   `m`: Sort by modification time.
    *   `t`: Sort by type (extension).
    *   `r`: Reverse the sort order.

#### **View & Display**

*   **Toggle Hidden Files (zh or Ctrl+h):** Show or hide hidden (dot) files.
*   **Toggle Preview (zp):** Toggle the file preview column.
*   **Reload (Ctrl+r or R):** Refresh the directory listing.
*   **View File (i):** Open the file in the pager (full preview).
*   **Edit File (E):** Open the file in `$EDITOR`.
*   **Open With (r):** Open the file with a specific program.

#### **Shell Integration**

*   **Shell Command (!):** Run a shell command. `%s` is replaced with the selected files.
*   **Shell in Directory (S):** Open a shell in the current directory.
*   **Console Command (:):** Open the ranger command console.

#### **Customization**

*   **Config Files:**
    *   `~/.config/ranger/rc.conf` -- Key bindings and settings.
    *   `~/.config/ranger/rifle.conf` -- File opener rules.
    *   `~/.config/ranger/scope.sh` -- File preview script.
*   **Generate Default Configs:** `ranger --copy-config=all`
*   **Example Keybinding:**
    ```python
    # In rc.conf
    map DD shell mv %s ~/.local/share/Trash/files/
    map X shell extract %s
    map Z shell tar -czf %f.tar.gz %s
    ```
