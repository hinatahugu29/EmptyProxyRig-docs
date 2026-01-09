# はじめに

Empty Proxy Rig のインストールと基本的な使い方を説明します。

---

## インストール

### 1. ダウンロード

Superhive または GitHub からアドオンの `.zip` ファイルをダウンロードします。

### 2. Blenderにインストール

1. Blender を起動
2. **Edit → Preferences → Add-ons** を開く
3. 右上の **Install...** ボタンをクリック
4. ダウンロードした `.zip` ファイルを選択
5. **Install Add-on** をクリック

### 3. 有効化

1. 検索バーに「Empty Proxy Rig」と入力
2. チェックボックスをオンにして有効化

---

## パネルの場所

3D Viewport のサイドバー（**N** キー）を開き、**Empty Proxy Rig** タブを選択します。

---

## 基本ワークフロー

### Step 1: Emptyを配置

1. メッシュオブジェクトを選択
2. **Start Empty Dropper** をクリック
3. メッシュ上の関節位置をクリックしてEmptyを配置
4. 右クリックまたは ++esc++ で終了

!!! tip "キーボードショートカット"
    - ++tab++: 近くのEmpty間を循環選択
    - ++ctrl+"クリック"++: 頂点にスナップ
    - ++shift+"クリック"++: エッジにスナップ
    - ++alt+"クリック"++: Volume Snap（対面位置）

### Step 2: チェーン順序を設定

1. 配置したEmptyを選択
2. **Add Selected to Helper** でhelperコレクションに追加
3. **Chain Order Manager** パネルで順序を調整

### Step 3: アーマチュアを生成

1. **Create Armature from Empties** をクリック
2. 自動でボーンチェーンが生成されます

### Step 4: 調整（オプション）

- **Adjust Mode**: アーマチュア生成後も位置を調整可能
- **Empty Relocator**: 精密なEmpty位置調整ツール

---

## 次のステップ

各機能の詳細は以下をご覧ください：

- [Empty配置](features/empty-placement.ja.md)
- [アーマチュア生成](features/armature-tools.ja.md)
- [チェーン管理](features/chain-manager.ja.md)
- [IKツール](features/ik-tools.ja.md)
- [コマンドリファレンス](reference/commands.ja.md)
