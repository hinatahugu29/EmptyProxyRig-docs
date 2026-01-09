# IK Tools

Easily set up IK (Inverse Kinematics) constraints.

---

## Panel Visibility

The IK Constraint Tools panel appears when:

- An armature is selected
- You are in **Pose Mode**

---

## Quick Actions

### Add IK Constraint

Add an IK constraint to selected bones.

1. Select bones in Pose mode
2. Click **Add IK Constraint**
3. Set a target (Empty, etc.)

### Apply Visual Transform

Bake the IK-driven pose as the current pose state.

### Pose as Rest Pose

Set the current pose as the rest pose (initial pose).

---

## IK Settings

### Target

The target object for IK. Usually an Empty.

### Chain Length

Number of bones affected by IK.

- `0`: Automatic (to root bone)
- `1+`: Affects specified number of bones

### Iterations

Number of IK calculation iterations. Higher = more accurate but slower.

### Use Stretch

When enabled, bones will stretch to reach the target if it's too far.

### Use Rotation

When enabled, target rotation also affects the bone.

### Influence

IK influence amount. Adjustable from 0 to 1.

---

## Tips

!!! tip "Setting Empty as Target"
    You can drag and drop an Empty into the Target field.

!!! tip "Editing Multiple Bones"
    When multiple bones are selected, the last selected (active) bone is edited.
    Use ++shift+"Click"++ to change the active bone.

---

## Delete Constraint

To delete a constraint:

1. Expand the constraint details in the panel
2. Click the red **Delete Constraint** button
