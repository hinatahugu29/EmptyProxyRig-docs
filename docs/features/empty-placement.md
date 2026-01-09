# Empty Placement

Functions for placing Empty objects on meshes.

---

## Interactive Dropper

The most powerful placement tool. Click on mesh surfaces to place Empties.

### Usage

1. Select a mesh object
2. Click **Start Empty Dropper**
3. Click anywhere on the mesh
4. Right-click or ++esc++ to exit

### Keyboard Shortcuts

| Key | Function |
|-----|----------|
| ++tab++ | Cycle through nearby Empties |
| ++ctrl+"Click"++ | Snap to nearest vertex |
| ++shift+"Click"++ | Snap to nearest edge midpoint |
| ++alt+"Click"++ | Volume Snap: Opposite point |
| ++alt+ctrl+"Click"++ | Volume Snap: Edge loop center |
| ++alt+shift+"Click"++ | Volume Snap: Edge ring center |
| ++right-button++ / ++esc++ | Exit |

---

## Volume Snap (v1.4.0+)

Advanced snapping for internal structures like pipes and tubes.

### Modes

| Modifier | Mode | Description |
|----------|------|-------------|
| ++alt++ | Opposite | Midpoint between front and back surfaces |
| ++alt+ctrl++ | Loop Center | Centroid of edge loop |
| ++alt+shift++ | Ring Center | Centroid of edge ring |

!!! tip "Use Cases"
    - **Opposite**: Perfect for placing joints inside pipes/tubes
    - **Loop Center**: Find center of circular cross-sections
    - **Ring Center**: Find center along the length of tubes

---

## Place at Selection

Place Empties at selected vertices or bone heads in Edit mode.

### Usage

1. Enter Edit mode and select vertices
2. Click **Place at Selection**
3. Empties are created at each selected vertex

---

## Place at Object Origin

Create an Empty at the origin of selected objects.

---

## Place & Move Origin

Place an Empty at selection center, move mesh origin there, and parent mesh to Empty.

---

## Place Empty at Selection Center

Place Empty at the center of selection (bounding box center) without moving the origin.
Useful when selecting multiple vertices.
