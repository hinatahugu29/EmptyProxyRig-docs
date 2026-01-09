# アーマチュア生成

配置したEmptyオブジェクトからアーマチュア（ボーン）を自動生成する機能です。

---

## Create Armature from Empties

helperコレクション内のEmptyをチェーン順序に従ってボーンに変換します。

### 前提条件

- Emptyが `helper` コレクションに登録されている
- Chain Order Manager で順序が設定されている

### 使い方

1. **Create Armature from Empties** をクリック
2. 自動でアーマチュアが生成されます

!!! note "ボーンの向き"
    ボーンは chain_index の順番で接続されます。
    index 0 → index 1 → index 2 → ...

---

## Adjust Mode

アーマチュア生成後でもEmptyの位置を調整し、ボーンに反映できます。

### ワークフロー

1. 生成されたアーマチュアを選択
2. **Adjust Mode: OFF** をクリックしてONにする
3. Emptyの位置を移動
4. **Adjust Mode: ON** をクリックしてOFFにする（変更が適用される）

!!! warning "注意"
    Adjust Mode中は他の編集を行わないでください。
    OFFにするまでボーンには反映されません。

---

## Reverse Mode

既存のアーマチュアからEmptyを生成してIKでリンクするモードです。

既に作成済みのリグを後から調整する場合に使用します。

---

## Empty Relocator

Emptyの位置を精密に調整するためのツールです。

### キーボードショートカット

| キー | 機能 |
|------|------|
| ++tab++ | 次/前のEmptyに切替 |
| ++ctrl++ | 頂点スナップモード |
| ++shift++ | エッジスナップモード |
| ++alt++ | Volume Snapモード |

Adjust Mode または Reverse Mode がアクティブな時、またはEmptyを直接選択している時に使用できます。

---

## Bone Roll Control

ボーンロール（ねじれ）の向きを調整します。

### Set Roll to Empty Up

Emptyの位置を「上」方向としてボーンロールを設定します。

1. 編集モードでボーンを選択
2. 上方向の参照としてEmptyを選択
3. **Bone Roll Menu → Set Roll to Empty Up** を使用

### Set Roll to View

現在のビュー方向に合わせてボーンロールを設定します。
