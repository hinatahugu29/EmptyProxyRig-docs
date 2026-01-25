# EmptyProxyRig (v2)

**EmptyProxyRig (EPR)** は、Rig Mechanistスイートの「構造的バックボーン」を担うツールです。最終的なアーマチュア（骨格）を生成する前に、エンプティオブジェクトを使ってリグの階層構造やピボット位置を設計します。

## なぜ「プロキシ」リギングなのか？
いきなりボーンで設計を始めると、修正が破壊的になったり、軸合わせが面倒なことがあります。エンプティを「プロキシ（代理）ボーン」として使うことで以下のメリットが生まれます：

1.  **非破壊的修正**: 親子関係の付け替えやピボット移動が容易です。クライアントからの急な変更にも、Emptyを動かして `Adjust Mode` をトグルするだけで対応できます。
2.  **原点管理**: ハードサーフェスパーツの回転軸（原点）を同時に管理できます。
3.  **可視化**: 生成前に「Chain Preview」で構造を確認できます。

!!! tip "Philosophy: Proxy First, Bone Later"
    Emptyは常に「設計データ」として存在し、Armatureはそこから出力される「製品」に過ぎません。この分離により、「ボーンの呪縛」から解放されます。

## 主な機能

### 1. Interactive Empty Dropper (配置ツール)
*   高性能なスナップ機能については [VisualSnapAssist](visual_snap_assist.md) を参照してください。
*   **基本操作**:
    *   `左クリック`: Emptyを配置。
    *   `ホイール`: サイズ調整。
    *   `N キー`: 法線への整列 (Align to Normal) 切り替え。

### 2. Origin Management (原点管理)
メカニカルモデルでは、「関節の位置＝オブジェクトの原点」であることが望ましいです。
*   **Place at Selection**: 選択箇所にEmptyを作成します。
*   **Place & Move Origin**: メッシュの原点をその位置に移動し、親となるEmptyを作成します。メカパーツ（ヒンジやローター）のセットアップに最適です。
*   **Set Origin to Empty**: 既存のEmptyの位置にメッシュの原点を移動させます。

### 3. Armature Generation (アーマチュア生成)
Emptyを配置し、親子関係を設定した後に行います：

*   **Create Armature from Empties**: このボタン一つで骨格を生成します。
    *   **ロール自動計算 (Z-Axis Rule)**: EmptyのローカルZ軸が、生成されるボーンの「Up Vector（上方向）」として扱われます。
    
    > **設定のコツ**: シリンダーが手前に曲がる関節なら、EmptyのZ軸を真上に向けます。**「ボーンのひねりはEmptyの向きで決まる」**と覚えれば、編集モードでの数値入力は不要です。

*   **Adjust Mode**: ボーン位置をEmptyに合わせて再同期します。修正に便利です。
*   **Reverse Adjust Mode**: 既存のアーマチュアから逆にEmptyを生成します。

### 4. Chain Management (チェーン管理)
*   **Chain Preview**: エンプティ間の親子関係（親→子）を3Dビュー上にラインで描画し、つながりを可視化します。
*   **Select Helper Empties**: 作業用のEmptyを一括選択し、隠す・削除する等の管理を行います。

## コマンドリファレンス

### Empty & Rigging Tools
*Rig Mechanist* タブ内に配置されています。

#### Interactive Dropper
*   **Start Empty Dropper**: メインの配置ツールを起動します。
    *   *アイコン*: `RESTRICT_SELECT_OFF`

#### Empty Placement
*   **Place at Selection**: 選択している要素（頂点やオブジェクト）の位置にEmptyを作成します。
    *   *アイコン*: `VERTEXSEL`
*   **Place at Origin**: 選択したオブジェクトの原点位置にEmptyを作成します。
    *   *アイコン*: `OBJECT_ORIGIN`
*   **Place & Move Origin**: オブジェクトの原点を選択中心に移動させ、そこに親となるEmptyを作成します。
    *   *アイコン*: `PIVOT_CURSOR`
*   **Place Empty at Selection Center**: 原点は移動せずに、選択中心の位置にEmptyを作成します。
    *   *アイコン*: `EMPTY_DATA`

#### Origin Management
*   **Set Origin to Empty**: メッシュの原点を、アクティブなEmptyの位置へ移動させます。
    *   *アイコン*: `EMPTY_DATA`
*   **Move Origin to Selection**: 原点を選択位置へ移動し、親Emptyを作成します（即座にリグ化準備）。
    *   *アイコン*: `PIVOT_CURSOR`

#### Empty Management
*   **Select All Helper Empties**: "helper" コレクション内の全Emptyを選択します。
    *   *アイコン*: `RESTRICT_SELECT_OFF`
*   **Move Selected to Helper**: 選択中のEmptyを "helper" コレクションへ移動します。
    *   *アイコン*: `COLLECTION_NEW`
*   **Toggle Helper Visibility**: helperコレクションの表示/非表示を切り替え。
    *   *アイコン*: `HIDE_OFF` / `HIDE_ON`
*   **Replace Empty**: Emptyを再生成します（更新用）。
    *   *アイコン*: `FILE_REFRESH`
*   **Delete Helper Collection**: helperコレクションとその中身を全て削除します。
    *   *アイコン*: `TRASH`

#### Armature Tools
*   **Create Armature from Empties**: Emptyの階層構造に基づいてアーマチュアを生成します。
    *   *アイコン*: `BONE_DATA`
*   **Adjust Mode**: ボーンとEmptyの同期モードを切り替えます。
    *   *アイコン*: `BONE_DATA`
*   **Reverse Adjust Mode**: 既存のアーマチュアからEmptyを逆生成します。
    *   *アイコン*: `BONE_DATA`

### Chain Order Manager
Emptyの接続順序を管理するパネルです。

*   **Move Up / Down**: チェーンリスト内で選択したEmptyの順序を上げ下げします。
    *   *アイコン*: `TRIA_UP` / `TRIA_DOWN`
*   **Auto Sort**: 距離に基づいて自動的に並び替えます。
    *   *アイコン*: `SORTSIZE`
*   **Set from Selection**: 現在の選択順序でチェーン順序を上書きします。
    *   *アイコン*: `HAND`
