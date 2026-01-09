# FAQ

Frequently Asked Questions about Empty Proxy Rig.

---

## Installation & Setup

### Q: The panel doesn't appear

**A:** Please check the following:

1. Is the addon enabled? (Preferences → Add-ons)
2. Is the sidebar open? (Press ++n++)
3. Look for the "Empty Proxy Rig" tab

---

### Q: What Blender versions are supported?

**A:** Blender 4.2 and later.

---

## Empty Placement

### Q: Interactive Dropper doesn't work

**A:** Select a mesh object first, then run the operator.
It doesn't work with curves or armatures.

---

### Q: I can't find the helper collection

**A:** The helper collection is created automatically when you first add an Empty using "Add Selected to Helper".

---

### Q: What is Volume Snap?

**A:** A feature (v1.4.0+) for snapping to internal structures.

- ++alt++"Click"++: Snap to the midpoint between front and back surfaces
- Useful for placing joints inside pipes and tubes

---

## Armature Generation

### Q: Bone order is wrong

**A:** Check the chain order in Chain Order Manager.
Use "Set Order from Selection" to reorder by selection sequence.

---

### Q: Nothing happens when I turn off Adjust Mode

**A:** Move the Empty positions before turning OFF.
If positions haven't changed, there's nothing to apply.

---

### Q: Can I use this with existing armatures?

**A:** Yes! Use **Reverse Mode** to generate Empties from existing bones and link them with IK.

---

## General

### Q: Does Undo work?

**A:** Yes, ++ctrl+z++ works for most operations.
However, some operations that span mode changes may not undo in a single step.

---

### Q: I found a bug

**A:** Please report it on GitHub Issues.
Include reproduction steps and screenshots if possible.

[GitHub Issues](https://github.com/hinatahugu29)

---

### Q: Can I use this for commercial projects?

**A:** Please check the license terms on Superhive where you purchased the addon.
