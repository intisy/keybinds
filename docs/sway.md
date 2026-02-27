### Sway Keybindings

Sway is a tiling Wayland compositor and a drop-in replacement for i3. It uses nearly identical configuration and keybindings to i3 but runs natively on Wayland. All default keybindings use `$mod`, typically set to the **Super** key. Configuration lives in `~/.config/sway/config`.

#### **The Most Important Shortcuts**

*   **Open Terminal ($mod+Enter):** Launches the default terminal emulator.
*   **Application Launcher ($mod+d):** Opens the application launcher (typically `dmenu`, `wofi`, or `rofi`).
*   **Kill Focused Window ($mod+Shift+q):** Closes the currently focused window.
*   **Reload Config ($mod+Shift+c):** Reloads the sway configuration file.
*   **Exit Sway ($mod+Shift+e):** Exits sway. Prompts for confirmation.

#### **Focus & Movement**

*   **Move Focus ($mod+h/j/k/l):** Move focus left/down/up/right. Arrow keys also work.
*   **Move Focused Window ($mod+Shift+h/j/k/l):** Move the focused window in the given direction.
*   **Focus Parent Container ($mod+a):** Move focus to the parent container.
*   **Focus Child Container ($mod+d):** Move focus to the first child container.

#### **Layout & Splits**

*   **Horizontal Split ($mod+b):** Next window opens to the right.
*   **Vertical Split ($mod+v):** Next window opens below.
*   **Toggle Split Direction ($mod+e):** Switch between horizontal and vertical splitting.
*   **Stacking Layout ($mod+s):** Stack windows with title bars.
*   **Tabbed Layout ($mod+w):** Arrange windows as tabs.
*   **Toggle Floating ($mod+Shift+Space):** Toggle between tiling and floating.
*   **Focus Floating/Tiling ($mod+Space):** Switch focus between floating and tiling layers.
*   **Fullscreen ($mod+f):** Toggle fullscreen for the focused window.

#### **Workspaces**

*   **Switch Workspace ($mod+0-9):** Switch to workspace 1 through 10.
*   **Move Window to Workspace ($mod+Shift+0-9):** Move the focused window to workspace 1 through 10.

#### **Resizing**

*   **Resize Mode ($mod+r):** Enter resize mode. Then:
    *   `h` or `Left`: Shrink width.
    *   `l` or `Right`: Grow width.
    *   `k` or `Up`: Shrink height.
    *   `j` or `Down`: Grow height.
    *   `Escape` or `Enter`: Exit resize mode.

#### **Scratchpad**

*   **Move to Scratchpad ($mod+Shift+-):** Sends the focused window to the scratchpad.
*   **Show Scratchpad ($mod+-):** Shows/cycles through scratchpad windows.

#### **Multi-Monitor**

*   **Focus Output ($mod+Ctrl+h/j/k/l):** Move focus to the monitor in the given direction.
*   **Move Workspace to Output ($mod+Ctrl+Shift+h/j/k/l):** Move the current workspace to another monitor.

#### **Wayland-Specific Features**

*   **Input Configuration:** Sway natively handles input devices (touchpads, keyboards, tablets):
    ```bash
    input "type:touchpad" {
        tap enabled
        natural_scroll enabled
        dwt enabled
    }
    ```
*   **Output Configuration:** Monitor setup is handled in the config:
    ```bash
    output HDMI-A-1 resolution 1920x1080 position 0,0
    output eDP-1 resolution 2560x1440 position 1920,0 scale 1.5
    ```
*   **Screenshots:** Sway uses `grim` and `slurp` instead of X11 screenshot tools:
    ```bash
    # Full screenshot
    bindsym Print exec grim ~/Pictures/screenshot-$(date +%Y%m%d-%H%M%S).png

    # Region screenshot
    bindsym $mod+Shift+s exec grim -g "$(slurp)" - | wl-copy
    ```

#### **Customization**

*   **Config File:** `~/.config/sway/config`
*   **Status Bar:** Sway uses `swaybar` with `i3status`, `i3status-rs`, or `waybar`:
    ```bash
    bar {
        position top
        status_command i3status
    }
    ```
*   **Wallpaper:**
    ```bash
    output "*" bg ~/Pictures/wallpaper.jpg fill
    ```
*   **Autostart:**
    ```bash
    exec --no-startup-id mako          # Notification daemon
    exec --no-startup-id waybar        # Status bar
    exec --no-startup-id nm-applet     # Network manager
    ```
*   Sway is nearly config-compatible with i3. Most i3 configs work in sway with minimal changes (mainly replacing X11-specific commands with Wayland equivalents).
