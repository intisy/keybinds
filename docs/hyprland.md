### Hyprland Keybindings

Hyprland is a dynamic tiling Wayland compositor with smooth animations and extensive customization. All default keybindings use `$mainMod`, which is set to the **Super** (Windows) key by default. Configuration lives in `~/.config/hypr/hyprland.conf`.

#### **The Most Important Shortcuts**

*   **Open Terminal ($mainMod+Q):** Launches the default terminal (typically `kitty`).
*   **Application Launcher ($mainMod+R):** Opens the app launcher (typically `wofi`, `rofi`, or `tofi`).
*   **Close Window ($mainMod+C):** Closes the currently focused window.
*   **Exit Hyprland ($mainMod+M):** Exits the Hyprland session.
*   **Toggle Floating ($mainMod+V):** Toggles the focused window between tiling and floating mode.
*   **Fullscreen ($mainMod+F):** Toggles fullscreen for the focused window.

#### **Focus & Movement**

*   **Move Focus ($mainMod+H/J/K/L):** Move focus left/down/up/right. Arrow keys also work.
*   **Move Window ($mainMod+Shift+H/J/K/L):** Move the focused window in the given direction. Arrow keys also work.
*   **Swap Window ($mainMod+Ctrl+H/J/K/L):** Swap the focused window with the window in the given direction.
*   **Cycle Focus ($mainMod+Tab):** Cycle focus through open windows.

#### **Layout & Splits**

*   **Toggle Split ($mainMod+T):** Toggles the split direction (horizontal/vertical) for the `dwindle` layout.
*   **Pseudo Tiling ($mainMod+P):** Toggles pseudo-tiling, where a window retains its floating size but occupies a tiling slot.
*   **Toggle Layout ($mainMod+Space):** Switches between configured layouts (e.g., `dwindle` and `master`).
*   **Pin Floating Window ($mainMod+Shift+P):** Pins a floating window so it appears on all workspaces.

#### **Workspaces**

*   **Switch to Workspace ($mainMod+1-9, 0):** Switches to workspace 1 through 10.
*   **Move Window to Workspace ($mainMod+Shift+1-9, 0):** Moves the focused window to workspace 1 through 10.
*   **Move Window Silently ($mainMod+Ctrl+1-9, 0):** Moves the focused window to a workspace without switching to it.
*   **Scroll Through Workspaces ($mainMod+Scroll):** Scroll the mouse wheel while holding `$mainMod` to cycle through workspaces.
*   **Previous Workspace ($mainMod+Comma):** Switch to the previous workspace.
*   **Next Workspace ($mainMod+Period):** Switch to the next workspace.

#### **Resizing Windows**

*   **Resize Mode ($mainMod+S):** Enter resize submap. Then use:
    *   `H/Left`: Shrink width.
    *   `L/Right`: Grow width.
    *   `K/Up`: Shrink height.
    *   `J/Down`: Grow height.
    *   `Escape`: Exit resize mode.
*   **Mouse Resize ($mainMod+Right Click Drag):** Resize a window by dragging its edge.
*   **Mouse Move ($mainMod+Left Click Drag):** Move a floating window by dragging it.

#### **Special Workspaces (Scratchpad)**

*   **Toggle Special Workspace ($mainMod+Grave):** Shows or hides the special (scratchpad) workspace.
*   **Move to Special Workspace ($mainMod+Shift+Grave):** Sends the focused window to the special workspace.

#### **Groups (Tabbed Windows)**

*   **Toggle Group ($mainMod+G):** Groups or ungroups the focused window with adjacent windows into a tabbed group.
*   **Switch Group Tab ($mainMod+Tab):** Cycle through tabs in a group.
*   **Move in Group ($mainMod+Ctrl+H/L):** Move the active tab left/right within the group.
*   **Lock Groups ($mainMod+Shift+G):** Lock all groups, preventing accidental changes.

#### **Multi-Monitor**

*   **Focus Monitor ($mainMod+Comma/Period):** Move focus to the previous/next monitor.
*   **Move Window to Monitor ($mainMod+Shift+Comma/Period):** Move the focused window to the previous/next monitor.
*   **Swap Active Workspaces ($mainMod+Ctrl+Comma/Period):** Swap the active workspaces between monitors.

#### **Screenshots & Media**

*   **Screenshot (Print):** Take a full screenshot (requires `grim` or `hyprshot`).
*   **Screenshot Region ($mainMod+Shift+S):** Select an area to capture (requires `grim` + `slurp` or `hyprshot`).
*   **Volume Up/Down (XF86AudioRaiseVolume/LowerVolume):** Adjust volume (requires `wpctl` or `pactl`).
*   **Mute (XF86AudioMute):** Toggle audio mute.
*   **Brightness (XF86MonBrightnessUp/Down):** Adjust screen brightness (requires `brightnessctl`).

#### **Customization**

*   **Config File:** `~/.config/hypr/hyprland.conf`
*   **Example Keybinding:**
    ```bash
    # Launch Firefox
    bind = $mainMod, F1, exec, firefox

    # Lock screen
    bind = $mainMod, X, exec, hyprlock

    # Screenshot a region to clipboard
    bind = $mainMod SHIFT, S, exec, grim -g "$(slurp)" - | wl-copy
    ```
*   **Bind Flags:**
    ```bash
    bind  = ...     # Standard keybind
    binde = ...     # Repeats when held down (useful for resize/volume)
    bindm = ...     # Mouse bind (for move/resize with mouse)
    bindl = ...     # Locked bind (works even when input is locked)
    ```
*   **Window Rules:** Control per-window behavior:
    ```bash
    windowrulev2 = float, class:^(pavucontrol)$
    windowrulev2 = size 800 600, class:^(pavucontrol)$
    windowrulev2 = opacity 0.9, class:^(kitty)$
    ```
*   **Animations:** Hyprland features smooth animations that can be configured:
    ```bash
    animations {
        enabled = true
        bezier = myBezier, 0.05, 0.9, 0.1, 1.05
        animation = windows, 1, 7, myBezier
        animation = workspaces, 1, 6, default
    }
    ```
