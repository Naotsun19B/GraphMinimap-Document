# GraphMinimap

![Plugin](https://user-images.githubusercontent.com/51815450/177293045-ffae8179-55cd-4d89-bf6b-e627e797c43a.PNG)

<!--ts-->
* [概要](#概要)
* [動作環境](#動作環境)
* [インストール](#インストール)
* [機能と使い方](#機能と使い方)
    * [Hidden](#hidden)
    * [Resizable](#resizable)
    * [Visible](#visible)
    * [Controllable](#controllable)
    * [表示エリア](#表示エリア)
    * [Stream Deck](#stream-deck)
* [オプション](#オプション)
* [作者](#作者)
* [履歴](#履歴)
<!--te-->

## 概要

このプラグインは、グラフ全体の概要を示すミニマップをグラフエディタに追加します。  
ミニマップからグラフエディタを操作することもできます。

## 動作環境

対象バージョン : UE4.24 ～ 5.3    
対象プラットフォーム : Windows, Mac, Linux

## インストール

[マーケットプレイス](https://www.unrealengine.com/marketplace/ja/product/graph-minimap)からインストールしてください。  
プラグインのインストール後に機能が使用できない場合は、プラグインが有効化されていない可能性がありますので、編集 > プラグイン からプラグインの有効のチェックが入っているかをご確認ください。

## 機能と使い方

ブループリントやマテリアルなどの基本的なグラフに対応しています。  
グラフエディタを開くと自動的にミニマップが表示されます。  
ショートカットキーでミニマップのモードを切り替えることが出来ます。  
デフォルトのショートカットキーは```Ctrl + M```です。  
ミニマップのモードとサイズはグラフごとに保存され、次回以降グラフエディタを開いた時に復元されます。

### Hidden

ミニマップが非表示の状態です。

### Resizable

https://user-images.githubusercontent.com/51815450/177293227-29e3eaf7-1f49-45fe-b529-76a5a516bc8b.mp4

ドラッグ操作でミニマップのサイズを変更することができます。  
マウススクロールでミニマップの描画スケールを変更することができます。

### Visible

https://user-images.githubusercontent.com/51815450/177293415-67996847-9c8c-4bcd-b071-85b7fd67c2b1.mp4

ミニマップの当たり判定がなくなり、ミニマップ越しにグラフエディタを操作することができます。

### Controllable

https://user-images.githubusercontent.com/51815450/177293513-ee3428b1-7757-42d8-a1b3-a7f5be7b0401.mp4

ドラッグ操作でグラフエディタのカメラの位置を移動させることができます。  
マウススクロールでズーム操作ができます。

### 表示エリア

![MinimapArea](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/f205a45a-593f-4331-9197-1ea8347d1f25)

巨大なグラフで作業する際にもミニマップを活用できるように、グラフ全体を表示する以外にもグラフ内にあるコメントごとにミニマップに表示できる機能があります。  
ショートカットキーかミニマップ上のコンボボックスでミニマップの表示エリアを切り替えることができます。  
デフォルトのショートカットキーは```Ctrl + N```です。  
選択している表示エリアはグラフごとに保存され、次回以降グラフエディタを開いた時に復元されます。  

### Stream Deck

![StreamDeckApplication](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/a8abe4ca-9b4c-4ca2-a45b-854aec65f59c)

このプラグインはStream Deckからの機能の呼び出しに対応しています。

機能を利用するには以下の手順に従ってください。

1. エディタ環境設定の`Graph Minimap - Stream Deck`の`Install Stream Deck Plugin`からStream Deck向けのGraph Minimapプラグインをインストールします。
2. Stream Deckアプリケーションで利用したい機能のボタンを配置します。
3. 配置したボタンのプロパティの`Http Path`と`Port Number`を設定します。(デフォルトのままでも可)
4. エディタ環境設定の`Graph Minimap - Remote Control`の`Http Path`と`Port Number`にStream Deck側と同じ値を設定します。(デフォルトのままでも可)
5. エディタ環境設定の`Graph Minimap - Remote Control`の`Enable Remote Control`を`true`にすることでStream Deckと接続できます。
6. Stream Deckから配置したボタンを押下してください。

## オプション

![ShortcutKeySettings](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/df052bb6-4a64-44a6-bcad-e2300b97bf18)

「機能と使い方」でご紹介したショートカットキーはエディタ環境設定のキーボードショートカットから変更できます。

![Settings](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/de89046d-939b-4cdf-9be4-d7681c85bc7c)

| **セクション**                      | **項目**                      | **説明**                                                                                                        |
|--------------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------|
| Graph Minimap                  | Default Graph Minimap State | ミニマップのモードが保存されていない時に使用されるデフォルトのミニマップのモード。                                                                     |
|                                | Default Graph Minimap Size  | ミニマップのサイズが保存されていない時に使用されるデフォルトのミニマップのサイズ。                                                                     |
|                                | Default Rendering Scale     | ミニマップの描画スケールが保存されていない時に使用されるデフォルトのミニマップの描画スケール。ミニマップの描画スケールを小さくすることでMax Graph Sizeよりも大きなサイズのグラフでミニマップを使用できます。 |
|                                | Keep Graph Minimap State    | 次回の起動時に各グラフのミニマップの状態を復元するかどうか。                                                                                |
|                                | Clear Cache File Button     | 保存されたミニマップのデータを削除します。                                                                                         |
|                                | Max Graph Size              | ミニマップに描画できるグラフの最大サイズ。サイズが大きすぎると、ビデオメモリが不足してクラッシュする可能性があります。                                                   |
|                                | Minimap Alignment           | ミニマップがグラフエディタに表示される位置。                                                                                        |
|                                | Minimap Opacity             | グラフエディタに表示するミニマップの不透明度。                                                                                       |
|                                | Minimap Tint Color          | グラフエディタに表示するミニマップの色合い。                                                                                        |
|                                | Mode Icon Size              | ミニマップの左上に表示されるモードアイコンのサイズ。                                                                                    |
|                                | Padding                     | グラフを描画する時に適用される余白のサイズ。                                                                                        |
|                                | Mode Icon Tint Color        | ミニマップの左上に表示されるモードアイコンの色合い。                                                                                    |
|                                | Camera Bounds Color         | ミニマップ上に表示されるカメラの境界の色。                                                                                         |
|                                | Camera Bounds Thickness     | ミニマップに表示されるカメラ境界の線の太さ。                                                                                        |
|                                | Drag Sensitivity            | ミニマップのドラッグ操作時のマウス感度。                                                                                          |
|                                | Draw Size And Scale         | ミニマップの右上にグラフの描画スケールとスケーリングされたサイズを描画するかどうか。                                                                    |
|                                | Show Minimap Area           | ミニマップ上に現在表示されているミニマップ領域の名前を表示するかどうか。                                                                          |
|                                | Minimap Area Opacity        | ミニマップ上に現在表示されているミニマップ領域の名前の不透明度。                                                                              |
| Graph Minimap - Remote Control | Enable Remote Control       | HTTPサーバー経由のリモート制御が有効かどうか。サーバーを再構築した際には再度ご確認ください。                                                              |
|                                | Http Path                   | HTTPサーバーに接続するためのURL。編集するには一度`Enable Remote Control`を`false`にしてください。                                           |
|                                | Port Number                 | HTTPサーバーへの接続に使用されるポート番号。                                                                                      |
| Graph Minimap - Stream Deck    | Install Stream Deck Plugin  | Stream Deck向けのGraph Minimapプラグインをインストールします。                                                                   |

## 作者

[Naotsun](https://twitter.com/Naotsun_UE)

## 履歴

- (2023/09/09) v1.7
  UE5.3に対応しました  
  エディタ環境設定にあるプラグインの設定を全てのプロジェクト共通で保存されるようにしました  

- (2023/05/12) v1.6   
  UE5.2に対応しました  
  コメントごとにミニマップを表示する機能を追加しました（巨大なグラフで役に立ちます）  
  Stream Deckからの機能呼び出しに対応しました  

- (2022/11/08) v1.5   
  UE5.1に対応しました  

- (2022/07/03) v1.4   
  OSのDPIスケールが100%でない場合の不具合を修正  

- (2022/01/23) v1.3   
  関数をリスト上でダブルクリック時のノードへの自動フォーカスが動作しない不具合を修正

- (2022/01/17) v1.2   
  グラフを操作している間は詳細パネルが表示されない不具合を修正

- (2022/01/15) v1.1  
  ミニマップを表示しているとコンボボックスなどがちらつく不具合を修正  
  より大きなグラフでミニマップが使用できるようにするために描画のスケールを指定できるように  
  ミニマップのデザインを少し修正  

- (2021/12/25) v1.0   
  プラグインを公開
