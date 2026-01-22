# EmptyProxyRig (v2)

**EmptyProxyRig (EPR)** is the structural backbone of the Rig Mechanist suite. It allows you to design your rig's hierarchy and pivot points using Empties before committing to a final Armature.

## Why "Proxy" Rigging?
Designing directly with Bones can be destructive and tedious to adjust. By using Empties as "Proxy Bones":
1.  **Non-Destructive**: Easily reparent or move pivots without messing up bone rolls immediately.
2.  **Origin-Friendly**: Empties can serve as temporary origins for hard-surface parts.
3.  **Visualization**: Use the "Chain Preview" to see the flow before generation.

## Features

### 1. Interactive Empty Dropper
*   See [VisualSnapAssist](visual_snap_assist.md) for snapping details.
*   **Operations**:
    *   `LMB`: Place Empty.
    *   `Wheel`: Adjust Size.
    *   `N`: Toggle Align to Normal.

### 2. Origin Management
*   **Place at Selection**: Create an Empty at the selected element.
*   **Place & Move Origin**: Moves the object's origin to the selection and creates a parent Empty there. Ideal for mechanical parts (hinges, rotors).
*   **Set Origin to Empty**: Snaps a mesh's origin to an existing Empty using the cursor.

### 3. Armature Generation
Once your Empties are placed and parented (creating a hierarchy):

*   **Create Armature from Empties**: Generates a skeleton.
    *   **Auto Roll Calculation**: Automatically aligns bone rolls based on the Empty's Z-axis (v2 feature).
*   **Adjust Mode**: Syncs bones back to Empties for corrections.
*   **Reverse Adjust Mode**: Creates Empties from an existing Armature (for editing existing rigs).

### 4. Chain Management
*   **Chain Preview**: Draws lines connecting Empties to visualize the hierarchy (Parent -> Child relations) in real-time.
*   **Select Helper Empties**: Quickly select all proxy objects for deletion or hiding.

## Command Reference

### Empty & Rigging Tools
Located in the *Rig Mechanist* tab.

#### Interactive Dropper
*   **Start Empty Dropper**: Activates the main placement tool.
    *   *Icon*: `RESTRICT_SELECT_OFF`

#### Empty Placement
*   **Place at Selection**: Create Empty at current selection (Vertex/Object).
    *   *Icon*: `VERTEXSEL`
*   **Place at Origin**: Create Empty at selected Object's origin.
    *   *Icon*: `OBJECT_ORIGIN`
*   **Place & Move Origin**: Move object origin to selection center and parent to new Empty.
    *   *Icon*: `PIVOT_CURSOR`
*   **Place Empty at Selection Center**: Create Empty at selection center without moving origin.
    *   *Icon*: `EMPTY_DATA`

#### Origin Management
*   **Set Origin to Empty**: Moves mesh origin to the active Empty's location.
    *   *Icon*: `EMPTY_DATA`
*   **Move Origin to Selection**: Moves origin to selection and creates a parent Empty.
    *   *Icon*: `PIVOT_CURSOR`

#### Empty Management
*   **Select All Helper Empties**: Selects all Empties in the "helper" collection.
    *   *Icon*: `RESTRICT_SELECT_OFF`
*   **Move Selected to Helper**: Moves currently selected Empties to the "helper" collection.
    *   *Icon*: `COLLECTION_NEW`
*   **Toggle Helper Visibility**: Hides/Shows the helper collection.
    *   *Icon*: `HIDE_OFF` / `HIDE_ON`
*   **Replace Empty**: Replaces an Empty with a new one (refresh).
    *   *Icon*: `FILE_REFRESH`
*   **Delete Helper Collection**: Removes the entire helper collection and its contents.
    *   *Icon*: `TRASH`

#### Armature Tools
*   **Create Armature from Empties**: Generates the armature based on the Empty hierarchy.
    *   *Icon*: `BONE_DATA`
*   **Adjust Mode**: Toggles synchronization between Empties and Bones.
    *   *Icon*: `BONE_DATA`
*   **Reverse Adjust Mode**: Creates Empties from an existing Armature.
    *   *Icon*: `BONE_DATA`

### Chain Order Manager
For managing the connection order of Empties.

*   **Move Up / Down**: Reorder the selected Empty in the chain.
    *   *Icon*: `TRIA_UP` / `TRIA_DOWN`
*   **Auto Sort**: Sorts Empties by distance from the root.
    *   *Icon*: `SORTSIZE`
*   **Set from Selection**: Manually defines order based on selection order.
    *   *Icon*: `HAND`

