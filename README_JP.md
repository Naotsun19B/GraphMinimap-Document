# GraphMinimap

![Plugin](https://user-images.githubusercontent.com/51815450/147378061-05e7c9d0-488a-4e9c-bfdf-bb1966bb5fb1.PNG)

<!--ts-->
* [概要](#概要)
* [動作環境](#動作環境)
* [インストール](#インストール)
* [機能と使い方](#機能と使い方)
    * [Hidden](#hidden)
    * [Resizable](#resizable)
    * [Visible](#visible)
    * [Controllable](#controllable)
* [オプション](#オプション)
* [作者](#作者)
* [履歴](#履歴)
<!--te-->

## 概要

このプラグインは、グラフ全体の概要を示すミニマップをグラフエディタに追加します。  
ミニマップからグラフエディタを操作することもできます。

## 動作環境

対象バージョン : UE4.24 ～ 4.27 (UE5.0EA)    
対象プラットフォーム : Windows, Mac, Linux

## インストール

[マーケットプレイス](https://www.unrealengine.com/marketplace/ja/product/graph-minimap)からインストールしてください。

## 機能と使い方

ブループリントやマテリアルなどの基本的なグラフに対応しています。  
グラフエディタを開くと自動的にミニマップが表示されます。  
ショートカットキーでミニマップのモードを切り替えることが出来ます。  
デフォルトのショートカットキーは```Ctrl + M```です。  
ミニマップのモードとサイズはグラフごとに保存され、次回以降グラフエディタを開いた時に復元されます。

### Hidden

ミニマップが非表示の状態です。

### Resizable

![Resizable](https://user-images.githubusercontent.com/51815450/147378312-897bc859-d8ae-4587-a393-a1ac4ccc471b.gif)

ドラッグ操作でミニマップのサイズを変更することができます。  
マウススクロールでミニマップの描画スケールを変更することができます。

### Visible

![Visible](https://user-images.githubusercontent.com/51815450/147378411-a44fcdc6-9bd5-44aa-8a09-5f1c0769f87f.gif)

ミニマップの当たり判定がなくなり、ミニマップ越しにグラフエディタを操作することができます。

### Controllable

![Controllable](https://user-images.githubusercontent.com/51815450/147378422-be90a3b0-a9bd-40a8-a6b5-f7a931d5dd2d.gif)

ドラッグ操作でグラフエディタのカメラの位置を移動させることができます。  
マウススクロールでズーム操作ができます。

## オプション

![ShortcutKeySettings](https://user-images.githubusercontent.com/51815450/147378158-5c75649f-88e6-4f6d-9af9-cf0ac07ef649.PNG)

「機能と使い方」でご紹介したショートカットキーはエディタ環境設定のキーボードショートカットから変更できます。

![Settings](https://user-images.githubusercontent.com/51815450/147378165-9eeb0cd2-9247-47cd-873c-dcf59eb57500.PNG)

|**カテゴリ**|**項目**|**説明**|
|---|---|---|
|Default State|Default Graph Minimap State|ミニマップのモードが保存されていない時に使用されるデフォルトのミニマップのモード。|
| |Default Graph Minimap Size|ミニマップのサイズが保存されていない時に使用されるデフォルトのミニマップのサイズ。|
| |Default Rendering Scale|ミニマップの描画スケールが保存されていない時に使用されるデフォルトのミニマップの描画スケール。ミニマップの描画スケールを小さくすることでMax Graph Sizeよりも大きなサイズのグラフでミニマップを使用できます。|
| |Keep Graph Minimap State|次回の起動時に各グラフのミニマップの状態を復元するかどうか。|
| |Clear Cache File Button|保存されたミニマップのデータを削除するためのボタン。|
|Limitation|Max Graph Size|ミニマップに描画できるグラフの最大サイズ。サイズが大きすぎると、ビデオメモリが不足してクラッシュする可能性があります。|
|Minimap|Minimap Alignment|ミニマップがグラフエディタに表示される位置。|
| |Minimap Opacity|グラフエディタに表示するミニマップの不透明度。|
| |Minimap Tint Color|グラフエディタに表示するミニマップの色合い。|
| |Mode Icon Size|ミニマップの左上に表示されるモードアイコンのサイズ。|
| |Padding|グラフを描画する時に適用される余白のサイズ。|
| |Mode Icon Tint Color|ミニマップの左上に表示されるモードアイコンの色合い。|
| |Camera Bounds Color|ミニマップ上に表示されるカメラの境界の色。|
| |Camera Bounds Thickness|ミニマップに表示されるカメラ境界の線の太さ。|
| |Drag Sensitivity|ミニマップのドラッグ操作時のマウス感度。|
| |Draw Size And Scale|ミニマップの右上にグラフの描画スケールとスケーリングされたサイズを描画するかどうか。|

## 作者

[Naotsun](https://twitter.com/Naotsun_UE)

## 履歴

- (2022/01/15) v1.1  
  ミニマップを表示しているとコンボボックスなどがちらつく不具合を修正  
  より大きなグラフでミニマップが使用できるようにするために描画のスケールを指定できるように  
  ミニマップのデザインを少し修正  

- (2021/12/25) v1.0   
  プラグインを公開