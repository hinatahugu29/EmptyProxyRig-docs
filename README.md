# Rig Mechanist Suite - Documentation

This is the source code for the official documentation of **Rig Mechanist Suite**, a Blender addon suite for precision mechanical rigging.

**Rig Mechanist Suite** は、Blenderでのメカニカルリギング、ハードサーフェスモデリング、そしてエンジニアリング精度の配置作業を支援するために開発された統合ツール群の公式ドキュメントリポジトリです。

---

## 🛠 Tools Included (収録ツール)

### 1. Visual Snap Assist (v9)
**Geometric Constraint Solver & CAD-like Snapping**
Achieve topology-independent center detection and intersection snapping using virtual geometry (helper lines/circles).
- **Volume Snap**: Snap to internal volume centers, back-faces, or cross-sections.
- **Assist Mode**: Draw virtual lines/circles in 3D space to find precise intersections ("Triangulation").
- **Rotation Snap**: Define Axis, Start, and End points for precise rotation without numerical input (Tangent Snap included).

**(JP)**
標準機能では不可能なトポロジー非依存の中心点検出や、仮想ジオメトリ（補助線・円）を用いた交点スナップを実現します。
- **Volume Snap**: オブジェクトの内部、裏面、断面の中心をスナップ対象にします。
- **Assist Mode**: 空間上に仮想の線や円を作図し、「三辺測量」のように正確な位置を特定します。
- **Rotation Snap**: 軸・始点・終点を指定し、数値入力なしで正確な回転を行います（接線スナップ対応）。

### 2. EmptyProxyRig (v2)
**"Proxy First, Bone Later" - Non-Destructive Rigging**
Design your rig structure (proxy) using Empty objects before committing to bones.
- **Interactive Dropper**: Quickly place and adjust Empties at joint locations.
- **One-Click Armature**: Generate an entire armature from the Empty hierarchy. Bone rolls are intuitively controlled by the Z-axis of the Empties.
- **Adjust Mode**: Modify bone positions even after generation by simply moving the Empties.

**(JP)**
ボーンを作成する前に、Emptyオブジェクトを使ってリグの構造（プロキシ）を設計するワークフローを提供します。
- **Interactive Dropper**: 関節位置にEmptyを素早く配置・調整。
- **One-Click Armature**: Emptyの階層構造からアーマチュアを一発生成。ボーンのロール（捻じれ）はEmptyのZ軸で直感的に制御できます。
- **Adjust Mode**: 生成後もEmptyを動かすだけでボーン位置を修正可能。

### 3. Bone IK Tools (v2)
**Automated Mechanical IK Setup**
Streamline IK setup specifically for mechanical movements.
- **Instant IK**: Auto-generate targets and pole targets.
- **Mech Settings**: Adjust Stiffness and Stretch directly in Object Mode.
- **Apply IK**: Bake the IK pose into the mesh/rest pose. Ideal for creating deployed/retracted state variations of mechanical parts.

**(JP)**
機械的な動きに特化したIK設定を効率化します。
- **Instant IK**: ターゲットボーンとポールターゲットを自動生成・配置。
- **Mech Settings**: オブジェクトモードのまま、関節のStiffness（固さ）やStretch（遊び）を調整可能。
- **Apply IK**: IKでつけたポーズをメッシュ形状として固定（ベイク）。可動部品の展開図作成などに便利です。

---

## 📚 Documentation Structure

The documentation sources are located in the `docs/` directory.
ドキュメントソースは `docs/` ディレクトリに格納されています。

- [`docs/en/`](docs/en/): English Documentation
- [`docs/ja/`](docs/ja/): 日本語ドキュメント (Japanese)

## 🚀 How to Build

This documentation is built with [MkDocs](https://www.mkdocs.org/).

```bash
# Install dependencies
pip install mkdocs-material

# Run local server
mkdocs serve
```
