# Armature Tools

Generate and adjust armatures from placed Empty objects.

---

## Create Armature from Empties

Convert Empties in the helper collection to a bone chain based on chain order.

### Prerequisites

- Empties are registered in the `helper` collection
- Chain order is set in Chain Order Manager

### Usage

1. Click **Create Armature from Empties**
2. Armature is automatically generated

!!! note "Bone Direction"
    Bones are connected in chain_index order.
    index 0 → index 1 → index 2 → ...

---

## Adjust Mode

Refine Empty positions after armature generation and apply changes to bones.

### Workflow

1. Select the generated armature
2. Click **Adjust Mode: OFF** to turn ON
3. Move Empty positions as needed
4. Click **Adjust Mode: ON** to turn OFF (changes are applied)

!!! warning "Important"
    Do not perform other edits while Adjust Mode is active.
    Changes are not applied until you turn it OFF.

---

## Reverse Mode

Generate Empties from existing armature and link with IK.

Use this to adjust pre-existing rigs.

---

## Empty Relocator

Precise tool for adjusting Empty positions.

### Keyboard Shortcuts

| Key | Function |
|-----|----------|
| ++tab++ | Cycle to next/previous Empty |
| ++ctrl++ | Vertex snap mode |
| ++shift++ | Edge snap mode |
| ++alt++ | Volume Snap mode |

Available when Adjust Mode or Reverse Mode is active, or when an Empty is directly selected.

---

## Bone Roll Control

Adjust bone roll (twist) orientation.

### Set Roll to Empty Up

Use an Empty's position as the "up" direction to set bone roll.

1. Select bone(s) in Edit mode
2. Select an Empty as the up reference
3. Use **Bone Roll Menu → Set Roll to Empty Up**

### Set Roll to View

Align bone roll to the current view direction.
