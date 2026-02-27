### Blender Keybindings

Blender is a free, open-source 3D creation suite. It uses a heavily keyboard-driven workflow. These shortcuts cover the most commonly used operations across the major editors. Blender 2.8+ keybindings are used below (the modern default).

#### **General (All Editors)**

*   **Undo (Ctrl+Z):** Undo the last action.
*   **Redo (Ctrl+Shift+Z):** Redo the last undone action.
*   **Search/Command Menu (F3):** Search for any operator or command by name.
*   **Preferences (Edit > Preferences):** Open Blender preferences (no default shortcut).
*   **Save (Ctrl+S):** Save the current file.
*   **Save As (Ctrl+Shift+S):** Save as a new file.
*   **Open (Ctrl+O):** Open a file.
*   **Quit (Ctrl+Q):** Quit Blender.
*   **Toggle Fullscreen Area (Ctrl+Space):** Maximize the current editor area. Press again to restore.
*   **Toggle System Fullscreen (Alt+F11):** Toggle Blender window fullscreen.
*   **Quick Favorites (Q):** Open the quick favorites menu (add items via right-click > Add to Quick Favorites).

#### **3D Viewport -- Navigation**

*   **Orbit (Middle Mouse Drag):** Rotate the viewport.
*   **Pan (Shift+Middle Mouse Drag):** Pan the viewport.
*   **Zoom (Scroll Wheel):** Zoom in/out.
*   **Zoom to Selection (Numpad .):** Center and zoom the view on the selected object.
*   **View All (Home):** Zoom to show all objects.
*   **Front View (Numpad 1):** Front orthographic view.
*   **Side View (Numpad 3):** Right orthographic view.
*   **Top View (Numpad 7):** Top orthographic view.
*   **Opposite View (Ctrl+Numpad 1/3/7):** Back, left, and bottom views respectively.
*   **Toggle Perspective/Orthographic (Numpad 5):** Switch between perspective and orthographic projection.
*   **Camera View (Numpad 0):** Look through the active camera.
*   **Focus Object (Numpad .):** Frame the selected object in the viewport.
*   **Local View (Numpad /):** Isolate the selected object. Press again to return to full scene.
*   **Toggle X-Ray (Alt+Z):** See through objects (toggle transparency).
*   **Viewport Shading (Z):** Open the shading pie menu (wireframe, solid, material preview, rendered).

#### **3D Viewport -- Selection**

*   **Select (Left Click):** Select an object or element.
*   **Extend Selection (Shift+Click):** Add to the selection.
*   **Select All (A):** Select all. Press again to deselect all (or `Alt+A`).
*   **Box Select (B):** Draw a rectangle to select objects.
*   **Circle Select (C):** Paint to select. Scroll to resize brush. Right-click or `Esc` to exit.
*   **Lasso Select (Ctrl+Right Mouse Drag):** Freehand selection.
*   **Select Linked (Ctrl+L):** Select all connected geometry (Edit Mode).
*   **Select More/Less (Ctrl+Numpad +/-):** Grow or shrink the selection.
*   **Invert Selection (Ctrl+I):** Invert the current selection.

#### **3D Viewport -- Transforms**

*   **Grab/Move (G):** Move the selected object. Then:
    *   `X/Y/Z`: Constrain to an axis.
    *   `Shift+X/Y/Z`: Constrain to a plane (exclude that axis).
    *   Type a number for precise movement (e.g., `G Z 5 Enter` moves 5 units on Z).
    *   `Right-click` or `Esc`: Cancel.
*   **Rotate (R):** Rotate the selection. Same axis constraints apply.
*   **Scale (S):** Scale the selection. Same axis constraints apply.
*   **Confirm Transform (Enter or Left Click):** Apply the transformation.
*   **Cancel Transform (Right Click or Esc):** Cancel the transformation.
*   **Apply Transforms (Ctrl+A):** Apply location/rotation/scale so the object's transforms become its new rest state.
*   **Clear Location (Alt+G):** Reset location to origin.
*   **Clear Rotation (Alt+R):** Reset rotation.
*   **Clear Scale (Alt+S):** Reset scale.

#### **3D Viewport -- Object Mode**

*   **Add Object (Shift+A):** Open the Add menu (mesh, light, camera, etc.).
*   **Delete (X or Delete):** Delete the selected object (prompts for confirmation).
*   **Duplicate (Shift+D):** Duplicate the selected object.
*   **Duplicate Linked (Alt+D):** Duplicate with linked data (instances share the same mesh).
*   **Join Objects (Ctrl+J):** Merge selected objects into one.
*   **Set Parent (Ctrl+P):** Parent the selected objects to the active object.
*   **Clear Parent (Alt+P):** Remove parenting.
*   **Snap Menu (Shift+S):** Snap cursor or selection to grid, origin, etc.
*   **Set Origin:** Right-click > Set Origin (to geometry, to 3D cursor, etc.).
*   **Hide Selected (H):** Hide the selected object. `Alt+H` to unhide all.

#### **3D Viewport -- Edit Mode**

*   **Toggle Edit Mode (Tab):** Switch between Object Mode and Edit Mode.
*   **Vertex Select (1):** Switch to vertex selection mode.
*   **Edge Select (2):** Switch to edge selection mode.
*   **Face Select (3):** Switch to face selection mode.
*   **Extrude (E):** Extrude selected geometry.
*   **Inset Faces (I):** Inset the selected faces.
*   **Loop Cut (Ctrl+R):** Add a loop cut. Scroll to add more cuts.
*   **Knife Tool (K):** Cut new edges into geometry.
*   **Fill/Create Face (F):** Create a face or edge from selected vertices.
*   **Merge (M):** Merge selected vertices (at center, at cursor, by distance, etc.).
*   **Separate (P):** Separate selected geometry into a new object.
*   **Proportional Editing (O):** Toggle proportional editing (soft selection falloff).
*   **Edge/Face Menu (Ctrl+E / Ctrl+F):** Open the edge or face operations menu.
*   **Subdivide:** Right-click > Subdivide.
*   **Bevel (Ctrl+B):** Bevel the selected edges. Scroll to add segments.
*   **Bridge Edge Loops:** Select two edge loops, then use Edge menu > Bridge Edge Loops.

#### **Sculpt Mode**

*   **Toggle Sculpt Mode:** Switch via the mode dropdown or `Ctrl+Tab` pie menu.
*   **Brush Size (F):** Adjust the brush radius.
*   **Brush Strength (Shift+F):** Adjust the brush strength.
*   **Smooth Brush (Shift hold):** Temporarily switch to the smooth brush while holding Shift.
*   **Invert Brush (Ctrl hold):** Invert the brush effect (e.g., push instead of pull).
*   **Remesh (Ctrl+R):** Remesh the object for uniform topology.

#### **Animation**

*   **Play/Pause (Space):** Play or pause the animation.
*   **Next Frame (Right Arrow):** Advance one frame.
*   **Previous Frame (Left Arrow):** Go back one frame.
*   **Jump to Start (Shift+Left):** Go to the first frame.
*   **Jump to End (Shift+Right):** Go to the last frame.
*   **Insert Keyframe (I):** Insert a keyframe for the selected properties.
*   **Delete Keyframe (Alt+I):** Delete the keyframe at the current frame.
*   **Set Start/End Frame:** In the Timeline, set the playback range.

#### **Rendering**

*   **Render Image (F12):** Render the current frame.
*   **Render Animation (Ctrl+F12):** Render the animation.
*   **View Render (F11):** Open the render result window.

#### **Useful Pie Menus**

*   **Mode Pie Menu (Ctrl+Tab):** Switch between modes (Object, Edit, Sculpt, etc.).
*   **Shading Pie Menu (Z):** Switch viewport shading.
*   **Pivot Point Pie Menu (.):** Change the pivot/origin point for transforms.
*   **Snap Pie Menu (Shift+S):** Snap cursor and selection options.
*   **Orientation Pie Menu (,):** Change the transform orientation (global, local, normal, etc.).

#### **Customization**

*   **Keymap:** Edit via **Edit > Preferences > Keymap**. You can switch to legacy Blender (2.7x) keybindings or create a custom keymap.
*   **Industry Compatible Keymap:** Blender ships with an "Industry Compatible" keymap that uses shortcuts similar to Maya, 3ds Max, and other DCC tools.
*   **Add-ons:** Enable built-in add-ons or install third-party ones via **Edit > Preferences > Add-ons**.
