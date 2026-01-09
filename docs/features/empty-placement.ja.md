# Empty配置

Emptyオブジェクトをメッシュ上に配置するための機能群です。

---

## Interactive Dropper

最も強力な配置ツールです。メッシュ表面をクリックするだけでEmptyを配置できます。

### 使い方

1. メッシュオブジェクトを選択
2. **Start Empty Dropper** をクリック
3. メッシュ上の任意の位置をクリック
4. 右クリックまたは ++esc++ で終了

### キーボードショートカット

| キー | 機能 |
|------|------|
| ++tab++ | 近くのEmpty間を循環選択 |
| ++ctrl+"クリック"++ | 最寄りの頂点にスナップ |
| ++shift+"クリック"++ | 最寄りのエッジにスナップ |
| ++alt+"クリック"++ | Volume Snap: 対面位置 |
| ++alt+ctrl+"クリック"++ | Volume Snap: エッジループ中心 |
| ++alt+shift+"クリック"++ | Volume Snap: エッジリング中心 |
| ++right-button++ / ++esc++ | 終了 |

---

## Volume Snap（v1.4.0+）

パイプやチューブなどの内部構造へのスナップ機能です。

### モード

| 修飾キー | モード | 説明 |
|----------|--------|------|
| ++alt++ | Opposite | 表面と裏面の中点 |
| ++alt+ctrl++ | Loop Center | エッジループの重心 |
| ++alt+shift++ | Ring Center | エッジリングの重心 |

!!! tip "活用例"
    - **Opposite**: パイプ/チューブ内部の関節配置に最適
    - **Loop Center**: 円形断面の中心を検出
    - **Ring Center**: チューブの長さ方向の中心を検出

---

## Place at Selection

選択した頂点、エッジ、面の中心にEmptyを配置します。

### 使い方

1. 編集モードで頂点を選択
2. **Place at Selection** をクリック
3. 各選択頂点にEmptyが作成されます

---

## Place at Object Origin

アクティブオブジェクトの原点位置にEmptyを配置します。

---

## Place & Move Origin

Emptyを配置すると同時に、オブジェクトの原点をその位置に移動し、メッシュをEmptyに親子化します。

---

## Place Empty at Selection Center

選択した要素の中心（バウンディングボックスの中心）にEmptyを配置します。
原点は変更しません。複数の頂点を選択している場合に便利です。
