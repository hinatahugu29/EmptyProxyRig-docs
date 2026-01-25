# Rig Mechanist Suite - Documentation

**Rig Mechanist Suite** は、Blenderでのメカニカルリギング、ハードサーフェスモデリング、そしてエンジニアリング精度の配置作業を支援するために開発された統合ツール群の公式ドキュメントリポジトリです。

This is the source code for the official documentation of **Rig Mechanist Suite**, a Blender addon suite for precision mechanical rigging.

## 🛠 Tools Included (収録ツール)

### 1. Visual Snap Assist (v9)
**幾何学的拘束ソルバー & CADライクなスナップツール**
標準機能では不可能なトポロジー非依存の中心点検出や、仮想ジオメトリ（補助線・円）を用いた交点スナップを実現します。
- **Volume Snap**: オブジェクトの内部、裏面、断面の中心をスナップ対象にします。
- **Assist Mode**: 空間上に仮想の線や円を作図し、「三辺測量」のように正確な位置を特定します。
- **Rotation Snap**: 軸・始点・終点を指定し、数値入力なしで正確な回転を行います（接線スナップ対応）。

### 2. EmptyProxyRig (v2)
**"Proxy First, Bone Later" - 非破壊リギング支援**
ボーンを作成する前に、Emptyオブジェクトを使ってリグの構造（プロキシ）を設計するワークフローを提供します。
- **Interactive Dropper**: 関節位置にEmptyを素早く配置・調整。
- **One-Click Armature**: Emptyの階層構造からアーマチュアを一発生成。ボーンのロール（捻じれ）はEmptyのZ軸で直感的に制御できます。
- **Adjust Mode**: 生成後もEmptyを動かすだけでボーン位置を修正可能。

### 3. Bone IK Tools (v2)
**メカニカルIKの自動セットアップ**
機械的な動きに特化したIK設定を効率化します。
- **Instant IK**: ターゲットボーンとポールターゲットを自動生成・配置。
- **Mech Settings**: オブジェクトモードのまま、関節のStiffness（固さ）やStretch（遊び）を調整可能。
- **Apply IK**: IKでつけたポーズをメッシュ形状として固定（ベイク）。可動部品の展開図作成などに便利です。

## 📚 Documentation Structure

ドキュメントソースは `docs/` ディレクトリに格納されています。
The documentation sources are located in the `docs/` directory.

- [`docs/ja/`](docs/ja/): 日本語ドキュメント (Japanese - Primary)
- [`docs/en/`](docs/en/): English Documentation

## 🚀 How to Build

This documentation is built with [MkDocs](https://www.mkdocs.org/).

```bash
# Install dependencies
pip install mkdocs-material

# Run local server
mkdocs serve
```
