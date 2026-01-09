# コマンドリファレンス

Empty Proxy Rig Suite v1.5.0 の全オペレーター一覧です。

---

## 🎯 インタラクティブ配置

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.interactive_empty_dropper` | Start Empty Dropper | メッシュ面クリックでEmpty連続配置。++ctrl++=頂点、++shift++=辺、++alt++=Volume Snap |
| `its.empty_relocator` | Relocate Empty | 既存Emptyを新しい位置に移動（属性保持）。モード外でも選択時使用可 |

---

## 📍 Empty配置

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.place_at_selection` | Place at Selection | 選択した頂点/ボーンヘッドにEmpty作成 |
| `its.place_at_origin` | Place at Object Origin | 選択オブジェクトの原点にEmpty作成 |
| `its.place_and_move_origin` | Place & Move Origin | 選択中心にEmpty作成、原点を移動、メッシュを親子化 |
| `its.place_empty_at_selection_center` | Place Empty at Selection Center | 選択中心にEmpty作成（原点は変更しない） |

---

## 🎯 原点管理

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.set_origin_to_empty` | Set Origin to Empty | Emptyの位置にオブジェクト原点を移動 |
| `its.move_origin_to_selection` | Move Origin to Selection | 選択位置に原点を移動してEmptyを作成 |

---

## 📦 Empty管理

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.select_all_helper_empties` | Select All Helper Empties | helperコレクション内の全Emptyを選択 |
| `its.move_selected_empties_to_helper` | Add Selected to Helper | 選択したEmptyをhelperコレクションに移動 |
| `its.replace_empty` | Replace Empty | 選択されたEmptyを新しいEmptyに置き換え（属性保持） |
| `its.delete_helper_collection` | Delete Helper Collection | helperコレクションと全Emptyを削除 |
| `its.toggle_helper_visibility` | Toggle Helper Visibility | helperコレクションの表示/非表示を切替 |

---

## 🦴 アーマチュア作成

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.create_armature_from_empties` | Create Armature from Empties | 選択したEmptyからボーンチェーンを作成（chain_index順） |
| `its.toggle_adjust_mode` | Adjust Mode (ON/OFF) | IK制約でEmptyを動かすとアーマチュアが追従（自動リカバリー機能付） |
| `its.toggle_reverse_adjust_mode` | Reverse Adjust Mode (ON/OFF) | 既存アーマチュアからEmptyを生成してIKリンク |

---

## 🔗 チェーン順序管理

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.chain_move_up` | ▲ (Move Up) | 選択したEmptyのchain_indexを減少（上へ移動） |
| `its.chain_move_down` | ▼ (Move Down) | 選択したEmptyのchain_indexを増加（下へ移動） |
| `its.chain_auto_sort` | Auto Sort by Distance | 距離に基づいて自動ソート（アクティブから開始） |
| `its.chain_set_from_selection` | Set Order from Selection | 現在の選択順序に基づいてchain_indexを設定 |
| `its.chain_assign_unindexed` | Index Unindexed Empties | インデックスのないEmptyにchain_indexを付与 |
| `its.chain_clear_indices` | Clear All Indices | 全Emptyからchain_indexを削除 |
| `its.chain_select_by_index` | (internal) | パネルリストからEmptyを選択（内部使用） |

---

## 👁️ 表示オプション

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.toggle_chain_preview` | Toggle Chain Preview | チェーン接続をGPUで可視化（線と矢印） |
| `its.toggle_chain_indices` | Toggle Index Display | 各Emptyの横にchain_indexを表示 |
| `its.toggle_helper_names` | Toggle Name Display | helperコレクションのEmpty名を表示/非表示 |
| `its.toggle_helper_in_front` | Toggle In Front | X-Ray表示（常に全面に表示） |

---

## 🎛️ IK制約ツール

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.add_ik_to_selected_bones` | Add IK Constraint | 選択したボーンにIK制約を追加 |
| `its.apply_visual_transform` | Apply Visual Transform | ビジュアル変換を適用（制約を解除） |
| `its.pose_as_rest_pose` | Pose as Rest Pose | 現在のポーズを新しいレストポーズとして設定 |
| `its.delete_bone_constraint` | Delete Constraint | 選択したボーンから制約を削除 |

---

## 🎲 ボーンロール

| Command ID | Panel Label | 説明 |
|------------|-------------|------|
| `its.set_roll_to_empty_up` | Set Roll to Empty Up | Emptyの位置を「上」方向としてボーンロールを設定 |
| `its.set_roll_to_clip_plane` | Set Roll to View | 現在のビュー方向に合わせてボーンロールを設定 |
| `ITS_MT_bone_roll_menu` | Bone Roll Menu | ボーンロールメニュー |

---

## Volume Snap モード（v1.4.0+）

| 修飾キー | モード | 説明 |
|----------|--------|------|
| ++alt++ | Opposite | 表面と裏面の中点（パイプ内部） |
| ++alt+ctrl++ | Loop Center | 辺ループの重心 |
| ++alt+shift++ | Ring Center | 辺リングの重心 |

---

## 基本スナップモード

| 修飾キー | モード | 説明 |
|----------|--------|------|
| なし | Face | 面の中心 |
| ++ctrl++ | Vertex | 最寄り頂点 |
| ++shift++ | Edge | 辺の中点 |

---

*Empty Proxy Rig Suite v1.5.0 © 2024-2026 hinata_hugu & AI*
