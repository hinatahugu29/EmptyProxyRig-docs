# チェーン管理

ボーンチェーンの順序を視覚的に管理する機能です。

---

## Chain Order Manager パネル

`helper` コレクション内のEmptyをリスト表示し、順序を管理します。

---

## 基本操作

### Emptyをhelperに追加

1. Emptyを選択
2. **Add Selected to Helper** をクリック
3. 自動で `chain_index` が割り当てられます

### 順序の変更

- **▲ / ▼ ボタン**: 選択中のEmptyを上下に移動
- **リスト内の名前をクリック**: そのEmptyを選択

---

## 表示オプション

| アイコン | 機能 |
|----------|------|
| 🔍 | フォーカス選択（選択時にズーム） |
| A | 名前表示のON/OFF |
| X-Ray | 手前表示のON/OFF |
| グラフ | チェーンプレビュー表示 |
| 数字 | インデックス番号表示 |

---

## 自動ソート

### Chain Auto Sort

アクティブなEmptyからの距離に基づいて自動ソートします。
直線的なチェーンに便利です。

### Chain Set from Selection

現在の選択順でチェーン順序を設定します。

1. Emptyを順番に ++shift+"クリック"++ で複数選択
2. **Set Order from Selection** をクリック
3. 選択順で `chain_index` が設定されます

### Chain Assign Unindexed

`chain_index` が未設定のEmptyに自動で番号を割り当てます。
新しいインデックスはチェーンの末尾に追加されます。

### Chain Clear Indices

すべてのEmptyから `chain_index` を削除します。

---

## Empty管理

### Select All Helper Empties

helperコレクション内の全Emptyを選択します。

### Toggle Helper Visibility

helperコレクションの表示/非表示を切り替えます。

### Delete Helper Collection

helperコレクションと全Emptyを削除します。

!!! warning "注意"
    この操作はUndoで元に戻せません。

### Replace Empty

選択されたEmptyを新しいEmptyに置き換えます（名前、親子関係、chain_index、コレクション所属を保持）。
