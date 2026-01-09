# Getting Started

Installation and basic usage of Empty Proxy Rig.

---

## Installation

### 1. Download

Download the addon `.zip` file from Superhive or GitHub.

### 2. Install in Blender

1. Launch Blender
2. Go to **Edit → Preferences → Add-ons**
3. Click **Install...** button in the top right
4. Select the downloaded `.zip` file
5. Click **Install Add-on**

### 3. Enable

1. Type "Empty Proxy Rig" in the search bar
2. Check the box to enable

---

## Panel Location

Open the sidebar in 3D Viewport (press **N**) and select the **Empty Proxy Rig** tab.

---

## Basic Workflow

### Step 1: Place Empties

1. Select a mesh object
2. Click **Start Empty Dropper**
3. Click on joint positions on the mesh to place Empties
4. Right-click or press ++esc++ to exit

!!! tip "Keyboard Shortcuts"
    - ++tab++: Cycle through nearby Empties
    - ++ctrl+"Click"++: Snap to vertex
    - ++shift+"Click"++: Snap to edge
    - ++alt+"Click"++: Volume Snap (opposite point)

### Step 2: Set Chain Order

1. Select placed Empties
2. Click **Add Selected to Helper** to add to helper collection
3. Adjust order in **Chain Order Manager** panel

### Step 3: Generate Armature

1. Click **Create Armature from Empties**
2. Bone chain is automatically generated

### Step 4: Refine (Optional)

- **Adjust Mode**: Refine positions after armature generation
- **Empty Relocator**: Precise Empty position adjustment tool

---

## Next Steps

See detailed documentation for each feature:

- [Empty Placement](features/empty-placement.md)
- [Armature Tools](features/armature-tools.md)
- [Chain Manager](features/chain-manager.md)
- [IK Tools](features/ik-tools.md)
- [Command Reference](reference/commands.md)
