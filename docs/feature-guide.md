# Empty Proxy Rig Suite v1.5.0 - Feature Details & Use Cases

This document outlines the role of each feature and provides specific use cases to help you understand how to best utilize the add-on.

---

## 🎯 Interactive Placement

### 1. Start Empty Dropper
**Function Role:**
A tool that allows you to continuously place Empties (anchor points) by intuitively clicking on mesh surfaces, vertices, or edges.

**Use Cases / When to Use:**
- **Mecha Articulation Setup:** When you want to place rig reference points at precise locations, such as robot joints or pistons.
- **Leveraging Volume Snap:** When you need to place a point in the center of a pipe or cylinder, which is difficult to achieve with standard Blender functions.
- **Rough Rigging:** When you want to quickly place points that will become the basis for bones based on visual judgment, rather than strict numerical input.

### 2. Relocate Empty
**Function Role:**
Moves an already placed and configured Empty to a new location while retaining its attributes (name, parent-child relationships, etc.).

**Use Cases / When to Use:**
- **Fine-tuning:** When you decide to shift a joint position slightly after assembling a rig, you can correct just the position without breaking the rig structure.
- **Trial and Error:** Allows you to test multiple pivot positions without restarting the setup from scratch, increasing iteration speed.

---

## 📍 Empty Placement & Origin Management

### 3. Place at Selection / Origin
**Function Role:**
Instantly creates an Empty at the selected vertex or the origin of an object.

**Use Cases / When to Use:**
- **Precise Centering:** When you want to place it exactly at the center of a selected edge loop (Selection Center).
- **Utilizing Existing Objects:** When you want to use existing parts like bolts or nuts as reference points.

### 4. Place & Move Origin / Set Origin to Empty
**Function Role:**
Creates an Empty and simultaneously moves the "Origin" of the target mesh to that location.

**Use Cases / When to Use:**
- **Hard Surface Rigging Preparation:** Since mechanical parts often require their rotation axis to be at the origin, placing an Empty and moving the part's origin there instantly prepares it for rotation animation.
- **Origin Correction:** When you want to reset an origin that shifted during modeling to an intended pivot position (the Empty's location).

---

## 🦴 Armature Creation

### 5. Create Armature from Empties
**Function Role:**
Automatically generates a single skeleton (armature) by connecting multiple placed Empties.

**Use Cases / When to Use:**
- **Automating Rig Generation:** Eliminates the manual effort of extruding bones one by one. Simply connect the placed markers (Empties) to complete the rig.
- **Pistons and Cylinders:** By placing Empties at the start and end points and running this function, you can create a skeletal structure for telescopic mechanisms.

### 6. Adjust Mode (with Auto-Recovery)
**Function Role:**
Synchronizes the created armature bones with the original Empties. Moving an Empty will move the corresponding bone. v1.5.0 includes enhanced auto-recovery for broken rigs.

**Use Cases / When to Use:**
- **Post-Setup Corrections:** If you realize a joint position is off *after* creating the armature, you can correct the entire rig just by moving the Empty. Work that usually requires entering Bone Edit Mode can be done intuitively in Object Mode.

### 7. Reverse Adjust Mode
**Function Role:**
Generates placement Empties from an existing armature (e.g., one created manually).

**Use Cases / When to Use:**
- **Modifying Existing Rigs:** When you want to analyze or manage the structure of an old rig or a rig made by someone else using this add-on's features, you can extract Empties from bone positions to make them editable.

---

## 🔗 Chain Order Management

### 8. Auto Sort by Distance / Chain Management
**Function Role:**
Manages the connection order (parent-child relationship order) between Empties. Supports automatic sorting by distance and manual reordering.

**Use Cases / When to Use:**
- **Complex Multi-Joint Arms:** If the order of placed Empties doesn't match the intended connection order in a robot arm with many joints, this organizes them to create the correct bone flow.
- **Branching Structures:** When you want to visually manage which Empty is the parent and which is the child.

---

## 📦 Management & Display

### 9. Helper Collection Management
**Function Role:**
Groups working Empties into a dedicated collection ("helper") for one-click selection, hiding, or deletion.

**Use Cases / When to Use:**
- **Scene Organization:** Hides Empties when they become obstructive during work, or bulk deletes unneeded Empties after rigging is complete to keep the scene clean.

### 10. Chain Preview (GPU Visualization)
**Function Role:**
Draws lines and arrows in the 3D viewport to visualize the intended connection order of Empties.

**Use Cases / When to Use:**
- **Preventing Mistakes:** Allows you to visually confirm if the skeletal structure will be as intended *before* creating the armature, helping you spot incorrect connections (like jumps to distant points) in advance.

---

## 🎛️ IK Tools & Others

### 11. Instant IK Setup
**Function Role:**
Sets up IK (Inverse Kinematics) for the selected bone with a single click.

**Use Cases / When to Use:**
- **Quick Rigging:** When you want to control simple leg or arm movements with IK without building a full-scale rig, you can instantly apply IK without opening complex constraint settings panels.

### 12. Volume Snap (v1.4+)
**Function Role:**
A powerful custom snap function unique to this add-on. Calculates and snaps to "internal centers" that standard Blender snapping cannot achieve.

**Use Cases / When to Use:**
- **Cylinder/Pipe Centers:** When you want to place a pivot in the "empty space" at the center of a pipe where no vertices exist.
- **Centers of Thick Objects:** When you want to pass a bone through the midpoint between a front and back surface. Extremely useful in hard surface modeling.
