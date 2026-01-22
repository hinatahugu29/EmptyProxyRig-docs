# BoneIK Tools

**BoneIK Tools** adds the finishing touch to your rig by automating the setup of Inverse Kinematics (IK).

## Features

### Instant IK Setup
Select a bone in Pose Mode and click **"Add IK"**.

Everything happens automatically:
1.  **Constraint**: Adds an IK constraint to the selected bone.
2.  **Target**: Creates a new IK Target bone at the tail.
3.  **Pole Target**: Creates a Pole Target bone for knee/elbow direction control.
4.  **Chain Length**: Attempts to auto-detect the appropriate chain length.

## Usage
Simply select the bone you want to control (e.g., the shin or forearm) and run the operator. No strict naming conventions are required.

## Command Reference

### Bone & IK Tools
Located in the *Rig Mechanist* tab. Active when an Armature is selected.

#### Interactive Creator
*   **Pick Bone & Add IK**: Instantly sets up IK for the selected bone.
    *   *Icon*: `HAND`

#### Display Settings
*   **Show Names**: Toggles bone name display.
    *   *Icon*: `BONE_DATA`
*   **X-Ray**: Toggles X-Ray (Show in Front) for the armature.
    *   *Icon*: `GHOST_ENABLED`

#### Bone List (IK Setup)
A list of bones in the current armature.

*   **[Bone Name Button]**: Selects the bone.
*   **Add IK Target** (Pipette Icon): Adds IK to this bone.
    *   *Icon*: `EYEDROPPER`
*   **Apply IK** (Checkmark): Applies visual transform and removes constraint (Bakes the pose).
    *   *Icon*: `CHECKMARK`
*   **Remove IK** (X Icon): Removes the IK constraint.
    *   *Icon*: `X`

