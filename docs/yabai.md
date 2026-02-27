### yabai Keybindings

yabai is a tiling window manager for macOS that works alongside **skhd** (Simple Hotkey Daemon) for keybindings. yabai itself does not bind keys -- skhd maps hotkeys to `yabai -m` commands. Configuration lives in `~/.yabairc` (yabai) and `~/.skhdrc` (skhd).

#### **The Most Important Shortcuts**

These are community-standard skhd bindings. `Alt` is typically used as the modifier.

*   **Open Terminal (Alt+Enter):** Launch the default terminal.
*   **Close Window (Alt+Shift+Q):** Close the focused window.
*   **Toggle Float (Alt+Shift+Space):** Toggle the focused window between tiling and floating.
*   **Toggle Fullscreen (Alt+F):** Toggle native macOS fullscreen for the focused window.
*   **Toggle Zoom (Alt+Shift+F):** Toggle zoom-fullscreen (fills the space without entering macOS fullscreen).
*   **Restart yabai (Alt+Shift+R):** Restart yabai to apply configuration changes.

#### **Focus**

*   **Focus West (Alt+H):** Focus the window to the left.
*   **Focus South (Alt+J):** Focus the window below.
*   **Focus North (Alt+K):** Focus the window above.
*   **Focus East (Alt+L):** Focus the window to the right.

#### **Moving Windows**

*   **Swap West (Alt+Shift+H):** Swap the focused window with the one to the left.
*   **Swap South (Alt+Shift+J):** Swap with the window below.
*   **Swap North (Alt+Shift+K):** Swap with the window above.
*   **Swap East (Alt+Shift+L):** Swap with the window to the right.
*   **Warp Window (Alt+Ctrl+H/J/K/L):** Re-insert the focused window at the given position in the tree.

#### **Layout**

*   **Toggle BSP Layout (Alt+B):** Switch to BSP (binary space partitioning) tiling layout.
*   **Toggle Stack Layout (Alt+S):** Switch to stacking layout.
*   **Toggle Float Layout (Alt+D):** Switch to floating layout.
*   **Rotate Tree Clockwise (Alt+R):** Rotate the window tree 90 degrees clockwise.
*   **Rotate Tree Counter-Clockwise (Alt+Shift+R):** Rotate the window tree 90 degrees counter-clockwise.
*   **Mirror X-Axis (Alt+X):** Flip the layout along the x-axis.
*   **Mirror Y-Axis (Alt+Y):** Flip the layout along the y-axis.
*   **Balance Windows (Alt+0):** Equalize the size of all windows in the space.

#### **Spaces (Workspaces)**

*   **Focus Space (Alt+1-9):** Focus space 1 through 9.
*   **Move Window to Space (Alt+Shift+1-9):** Move the focused window to space 1 through 9.
*   **Create Space (Alt+Shift+N):** Create a new space.
*   **Destroy Space (Alt+Shift+W):** Destroy the current space.

#### **Resizing**

*   **Resize Left (Alt+Ctrl+H):** Grow window to the left.
*   **Resize Down (Alt+Ctrl+J):** Grow window downward.
*   **Resize Up (Alt+Ctrl+K):** Grow window upward.
*   **Resize Right (Alt+Ctrl+L):** Grow window to the right.

#### **Displays (Monitors)**

*   **Focus Display (Alt+Comma/Period):** Focus the previous/next display.
*   **Move Window to Display (Alt+Shift+Comma/Period):** Move the focused window to the previous/next display.

#### **Customization**

*   **yabai Config:** `~/.yabairc`
*   **skhd Config:** `~/.skhdrc`
*   **Example skhd Bindings:**
    ```bash
    # Focus windows
    alt - h : yabai -m window --focus west
    alt - j : yabai -m window --focus south
    alt - k : yabai -m window --focus north
    alt - l : yabai -m window --focus east

    # Move windows
    shift + alt - h : yabai -m window --swap west
    shift + alt - j : yabai -m window --swap south

    # Switch spaces
    alt - 1 : yabai -m space --focus 1
    alt - 2 : yabai -m space --focus 2

    # Float / unfloat
    shift + alt - space : yabai -m window --toggle float
    ```
*   **Gaps & Padding:**
    ```bash
    yabai -m config top_padding    10
    yabai -m config bottom_padding 10
    yabai -m config left_padding   10
    yabai -m config right_padding  10
    yabai -m config window_gap     10
    ```
*   **Window Rules:**
    ```bash
    yabai -m rule --add app="System Preferences" manage=off
    yabai -m rule --add app="Calculator" manage=off
    yabai -m rule --add app="Finder" title="Info" manage=off
    ```
