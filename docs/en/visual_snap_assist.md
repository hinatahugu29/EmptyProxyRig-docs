# VisualSnapAssist (v4)

**VisualSnapAssist (VSA)** brings geometric constraint solving and CAD-like snapping to Blender's 3D Viewport. It works seamlessly within the `Interactive Empty Dropper` but can also be used as a standalone logic later (future integration).

## Core Concept: "Source Pick"

Unlike Blender's standard snap which snaps the *cursor* or *selection center*, VSA defines a **Source** (Context) first.

*   **Ctrl**: Vertex Context (Cyan)
*   **Shift**: Edge Context (Magenta)
*   **Alt**: Volume Context (Blue/Teal)

## Modes

### 1. Circle Snap (Key: `C`)
Define a virtual circle from 3 points and snap to its center.

1.  Press `C` to enter Circle Mode.
2.  Click **3 points** on the mesh.
    *   These points define a unique circle.
3.  The tool automatically calculates the **Center Point** and visualizes the circle.
4.  Standard Left Click to place the Empty at the calculated center.

> [!TIP]
> Useful for finding the center of fragmented cylindrical geometry where no single face or loop exists.

### 2. Rotation Snap (Key: `R`)
Perform a precision rotation around a pivot point, aligning a "Start Point" to an "End Point".

**Workflow:**
1.  Press `R` to enter Rotation Mode.
2.  **Step 1: Pick Pivot**. Click to set the center of rotation.
3.  **Step 2: Pick Start**. Click the point you want to move (the handle).
4.  **Step 3: Pick End**. Move mouse to the target direction.
    *   The preview shows the rotation arc (Drift-Free).
    *   **Intersection Snap**: If the arc intersects a face or edge, it snaps to the intersection point (Orange dot).
    *   **Tangent Snap (`T`)**: Press `T` to toggle Tangent Mode. Snaps the rotation so the line from Pivot is tangent to the target circle/curve.

### 3. Edge Loop / Ring Logic (Volume Snap)
When holding `Alt` (Volume Mode) + `Ctrl` (Loop) or `Shift` (Ring):

*   **Logic Switching**: Hold `Alt` and scroll **Mouse Wheel** to change the calculation logic.
    *   **Smart**: Angle-weighted + Area-weighted (Default).
    *   **Linear**: Pure average regardless of topology.
    *   **Topology**: Follows quad flow (experimental).

## Visual Feedback
*   **Cyan**: Vertex
*   **Magenta**: Edge center

## Command Reference

### Main Panel (Rig Mechanist Tab)

*   **Start Visual Snap**: Activates the modal tool.
    *   *Icon*: `RESTRICT_SELECT_OFF`
    *   *Operator*: `vsa.visual_snap`

