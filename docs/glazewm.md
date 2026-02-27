### GlazeWM Keybindings

GlazeWM is a tiling window manager for Windows inspired by i3. It runs on top of the standard Windows desktop, adding tiling layouts, workspaces, and keyboard-driven window management. All default keybindings use `Alt` as the modifier. Configuration lives in `~/.glaze-wm/config.yaml`.

#### **The Most Important Shortcuts**

*   **Open Terminal (Alt+Enter):** Launches the default terminal.
*   **Close Window (Alt+Shift+Q):** Closes the currently focused window.
*   **Reload Config (Alt+Shift+R):** Reloads the GlazeWM configuration file.
*   **Exit GlazeWM (Alt+Shift+E):** Exits GlazeWM.
*   **Toggle Floating (Alt+Shift+Space):** Toggles the focused window between tiling and floating mode.
*   **Fullscreen (Alt+F):** Toggles fullscreen for the focused window.

#### **Focus & Movement**

*   **Move Focus (Alt+H/J/K/L):** Move focus left/down/up/right.
*   **Move Window (Alt+Shift+H/J/K/L):** Move the focused window in the given direction.
*   **Focus Next/Previous (Alt+J/K):** Cycle focus through windows in the current workspace.

#### **Layout**

*   **Vertical Split (Alt+V):** Sets the tiling direction to vertical for the next window.
*   **Horizontal Split (Alt+B):** Sets the tiling direction to horizontal for the next window.
*   **Toggle Tiling Direction (Alt+E):** Toggles between horizontal and vertical tiling.

#### **Resizing**

*   **Resize Mode (Alt+R):** Enters resize mode. Then:
    *   `H` or `Left`: Shrink width.
    *   `L` or `Right`: Grow width.
    *   `K` or `Up`: Shrink height.
    *   `J` or `Down`: Grow height.
    *   `Escape`: Exit resize mode.
*   **Grow Window (Alt+= ):** Increase the size of the focused window.
*   **Shrink Window (Alt+-):** Decrease the size of the focused window.

#### **Workspaces**

*   **Switch Workspace (Alt+1-9):** Switch to workspace 1 through 9.
*   **Move Window to Workspace (Alt+Shift+1-9):** Move the focused window to workspace 1 through 9.
*   **Next/Previous Workspace (Alt+Period/Comma):** Cycle through workspaces.

#### **Multi-Monitor**

*   **Focus Monitor (Alt+Ctrl+H/L):** Move focus to the monitor in the given direction.
*   **Move Window to Monitor (Alt+Ctrl+Shift+H/L):** Move the focused window to another monitor.

#### **Customization**

*   **Config File:** `~/.glaze-wm/config.yaml`
*   **Example Keybinding:**
    ```yaml
    keybindings:
      - command: "exec explorer"
        bindings: ["Alt+E"]
      - command: "focus left"
        bindings: ["Alt+H"]
      - command: "move left"
        bindings: ["Alt+Shift+H"]
    ```
*   **Gaps:**
    ```yaml
    gaps:
      inner_gap: "10px"
      outer_gap: "10px"
    ```
*   **Bar Configuration:** GlazeWM includes a built-in status bar that can be customized:
    ```yaml
    bar:
      position: "top"
      height: "30px"
      components_left:
        - type: "workspaces"
      components_right:
        - type: "clock"
          time_formatting: "HH:mm"
    ```
