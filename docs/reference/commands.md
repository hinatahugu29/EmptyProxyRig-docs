# Command Reference

Complete list of all operators in Empty Proxy Rig Suite v1.5.0.

---

## 🎯 Interactive Placement

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.interactive_empty_dropper` | Start Empty Dropper | Place Empties by clicking on mesh faces. ++ctrl++=vertex, ++shift++=edge, ++alt++=Volume Snap |
| `its.empty_relocator` | Relocate Empty | Move existing Empty to new position (preserves attributes). Also usable when Empty is selected outside modes |

---

## 📍 Empty Placement

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.place_at_selection` | Place at Selection | Create Empty at selected vertices/bone heads |
| `its.place_at_origin` | Place at Object Origin | Create Empty at selected object's origin |
| `its.place_and_move_origin` | Place & Move Origin | Create Empty at selection center, move origin, parent mesh |
| `its.place_empty_at_selection_center` | Place Empty at Selection Center | Create Empty at selection center (origin unchanged) |

---

## 🎯 Origin Management

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.set_origin_to_empty` | Set Origin to Empty | Move object origin to Empty position |
| `its.move_origin_to_selection` | Move Origin to Selection | Move origin to selection and create Empty |

---

## 📦 Empty Management

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.select_all_helper_empties` | Select All Helper Empties | Select all Empties in helper collection |
| `its.move_selected_empties_to_helper` | Add Selected to Helper | Move selected Empties to helper collection |
| `its.replace_empty` | Replace Empty | Replace selected Empty with new one (preserves attributes) |
| `its.delete_helper_collection` | Delete Helper Collection | Delete helper collection and all Empties |
| `its.toggle_helper_visibility` | Toggle Helper Visibility | Toggle helper collection visibility |

---

## 🦴 Armature Creation

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.create_armature_from_empties` | Create Armature from Empties | Create bone chain from selected Empties (by chain_index) |
| `its.toggle_adjust_mode` | Adjust Mode (ON/OFF) | IK-linked: Empty movement updates armature (with auto-recovery) |
| `its.toggle_reverse_adjust_mode` | Reverse Adjust Mode (ON/OFF) | Generate Empties from existing armature and link with IK |

---

## 🔗 Chain Order Management

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.chain_move_up` | ▲ (Move Up) | Decrease selected Empty's chain_index (move up) |
| `its.chain_move_down` | ▼ (Move Down) | Increase selected Empty's chain_index (move down) |
| `its.chain_auto_sort` | Auto Sort by Distance | Auto-sort by distance (starting from active) |
| `its.chain_set_from_selection` | Set Order from Selection | Set chain_index based on selection order |
| `its.chain_assign_unindexed` | Index Unindexed Empties | Assign chain_index to unindexed Empties |
| `its.chain_clear_indices` | Clear All Indices | Remove all chain_index values |
| `its.chain_select_by_index` | (internal) | Select Empty from panel list (internal use) |

---

## 👁️ Display Options

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.toggle_chain_preview` | Toggle Chain Preview | Visualize chain connections with GPU (lines and arrows) |
| `its.toggle_chain_indices` | Toggle Index Display | Show chain_index next to each Empty |
| `its.toggle_helper_names` | Toggle Name Display | Show/hide Empty names in helper collection |
| `its.toggle_helper_in_front` | Toggle In Front | X-Ray display (always in front) |

---

## 🎛️ IK Constraint Tools

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.add_ik_to_selected_bones` | Add IK Constraint | Add IK constraint to selected bones |
| `its.apply_visual_transform` | Apply Visual Transform | Apply visual transform (bake constraint result) |
| `its.pose_as_rest_pose` | Pose as Rest Pose | Set current pose as new rest pose |
| `its.delete_bone_constraint` | Delete Constraint | Delete constraint from selected bone |

---

## 🎲 Bone Roll

| Command ID | Panel Label | Description |
|------------|-------------|-------------|
| `its.set_roll_to_empty_up` | Set Roll to Empty Up | Set bone roll using Empty position as Up direction |
| `its.set_roll_to_clip_plane` | Set Roll to View | Set bone roll to match current view direction |
| `ITS_MT_bone_roll_menu` | Bone Roll Menu | Bone roll adjustment menu |

---

## Volume Snap Modes (v1.4.0+)

| Modifier | Mode | Description |
|----------|------|-------------|
| ++alt++ | Opposite | Midpoint between front and back surfaces (pipe interiors) |
| ++alt+ctrl++ | Loop Center | Centroid of edge loop |
| ++alt+shift++ | Ring Center | Centroid of edge ring |

---

## Basic Snap Modes

| Modifier | Mode | Description |
|----------|------|-------------|
| None | Face | Face center |
| ++ctrl++ | Vertex | Nearest vertex |
| ++shift++ | Edge | Edge midpoint |

---

*Empty Proxy Rig Suite v1.5.0 © 2024-2026 hinata_hugu & AI*
