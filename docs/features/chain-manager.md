# Chain Manager

Visually manage bone chain order.

---

## Chain Order Manager Panel

Displays Empties in the `helper` collection as a list and manages their order.

---

## Basic Operations

### Add Empties to Helper

1. Select Empties
2. Click **Add Selected to Helper**
3. `chain_index` is automatically assigned

### Change Order

- **▲ / ▼ buttons**: Move selected Empty up/down
- **Click name in list**: Select that Empty

---

## Display Options

| Icon | Function |
|------|----------|
| 🔍 | Focus on select (zoom when selecting) |
| A | Toggle name display |
| X-Ray | Toggle in-front display |
| Graph | Chain preview visualization |
| Numbers | Index number display |

---

## Auto Sort

### Chain Auto Sort

Automatically sort by distance from the active Empty.
Useful for linear chains.

### Chain Set from Selection

Set chain order from current selection order.

1. Select Empties in order with ++shift+"Click"++
2. Click **Set Order from Selection**
3. `chain_index` is set based on selection order

### Chain Assign Unindexed

Assign indices to Empties that don't have `chain_index`.
New indices are appended to the end of the chain.

### Chain Clear Indices

Remove all `chain_index` values from helper Empties.

---

## Empty Management

### Select All Helper Empties

Select all Empties in the helper collection.

### Toggle Helper Visibility

Show/hide the entire helper collection.

### Delete Helper Collection

Delete the helper collection and all its Empties.

!!! warning "Caution"
    This action cannot be undone with Undo.

### Replace Empty

Replace selected Empty with a new one while preserving attributes (name, parent, chain_index, collection membership).
