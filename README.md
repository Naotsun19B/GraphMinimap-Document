# GraphMinimap

![Plugin](https://user-images.githubusercontent.com/51815450/177293045-ffae8179-55cd-4d89-bf6b-e627e797c43a.PNG)

<!--ts-->
* [Description](#Description)
* [Requirement](#Requirement)
* [Installation](#Installation)
* [Features And Usages](#features-and-usages)
    * [Hidden](#hidden)
    * [Resizable](#resizable)
    * [Visible](#visible)
    * [Controllable](#controllable)
    * [Stream Deck](#stream-deck)
* [Settings](#Settings)
* [Author](#Author)
* [History](#History)
<!--te-->

## Description

This plugin adds a minimap to the graph editor that gives you an overview of the entire graph.  
You can also operate the graph editor from the minimap.  

## Requirement

Target version : UE4.24 ～ 5.2    
Target platform : Windows, Mac, Linux  

## Installation

Install from the [marketplace](https://www.unrealengine.com/marketplace/en/product/graph-minimap).  
If the feature is not available after installing the plugin, it is possible that the plugin has not been enabled, so please check if the plugin is enabled from Edit > Plugins.

## Features And Usages

It supports basic graph editors such as blueprint and material, etc.  
The minimap is automatically displayed when you open the graph editor.  
You can switch the minimap mode with the shortcut key.  
The default shortcut key is ```Ctrl + M```.  
The minimap mode and size are saved for each graph and will be restored the next time you open the graph editor.  

### Hidden

The minimap is hidden.  

### Resizable

https://user-images.githubusercontent.com/51815450/177293227-29e3eaf7-1f49-45fe-b529-76a5a516bc8b.mp4

You can resize the minimap by dragging.  
You can change the drawing scale of the minimap by scrolling the mouse.  

### Visible

https://user-images.githubusercontent.com/51815450/177293415-67996847-9c8c-4bcd-b071-85b7fd67c2b1.mp4

There is no collision detection on the minimap, and you can operate the graph editor through the minimap.  

### Controllable

https://user-images.githubusercontent.com/51815450/177293513-ee3428b1-7757-42d8-a1b3-a7f5be7b0401.mp4

You can move the camera position of the graph editor by dragging.  
You can zoom with the mouse scroll.  

### 表示エリア

![MinimapArea](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/f205a45a-593f-4331-9197-1ea8347d1f25)

In addition to displaying the entire graph, there is a function that allows you to display each comment in the graph on the minimap so that you can use the minimap even when working with huge graphs.  
You can switch the display area of the minimap with the shortcut key or the combo box on the minimap.  
The default shortcut key is ```Ctrl + N```.  
The selected display area is saved for each graph and restored the next time the graph editor is opened.  

### Stream Deck

![StreamDeckApplication](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/a8abe4ca-9b4c-4ca2-a45b-854aec65f59c)

This plugin supports calling functions from Stream Deck.

Follow the steps below to use the feature:

1. Install the Graph Minimap plugin for the Stream Deck from the `Graph Minimap - Stream Deck` in the editor preferences, then `Install Stream Deck Plugin`.
2. Place buttons for the functions you want to use in the Stream Deck application.
3. Set the `Http Path` and `Port Number` properties of the placed button. (You can leave it as default)
4. Set the `Http Path` and `Port Number` of `Graph Minimap - Remote Control` in the editor preferences to the same values as those on the Stream Deck side. (You can leave it as default)
5. You can connect to the Stream Deck by setting `Enable Remote Control` in `Graph Minimap - Remote Control` in the editor preferences to `true`.
6. Press the button placed from the Stream Deck.

## Settings

![ShortcutKeySettings](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/df052bb6-4a64-44a6-bcad-e2300b97bf18)

The shortcut keys introduced in "Functions And Usage" can be changed from the keyboard shortcuts in the editor preferences.  

![Settings](https://github.com/Naotsun19B/GraphMinimap-Document/assets/51815450/de89046d-939b-4cdf-9be4-d7681c85bc7c)

| **Section**                    | **Item**                    | **Description**                                                                                                                                                                                               |
|--------------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Graph Minimap                  | Default Graph Minimap State | The default minimap state used when the minimap state is not cached.                                                                                                                                          |
|                                | Default Graph Minimap Size  | The size of the minimap to display on the graph editor.                                                                                                                                                       |
|                                | Default Rendering Scale     | The default minimap drawing scale used when the minimap drawing scale is not saved. You can use the minimap with graphs that are larger than the Max Graph Size by reducing the drawing scale of the minimap. |
|                                | Keep Graph Minimap State    | Whether to restore the state of the minimap for each graph at the next startup.                                                                                                                               |
|                                | Clear Cache File Button     | Delete the cached minimap data.                                                                                                                                                                               |
|                                | Max Graph Size              | Maximum size of graph that can be drawn in the minimap. If set it too high, you may run out of video memory and crash.                                                                                        |
|                                | Minimap Alignment           | The position on which the minimap is displayed in the graph editor.                                                                                                                                           |
|                                | Minimap Opacity             | The opacity of the minimap to display on the graph editor.                                                                                                                                                    |
|                                | Minimap Tint Color          | The tint color of the minimap to display on the graph editor.                                                                                                                                                 |
|                                | Mode Icon Size              | The size of the mode icon displayed in the upper left of the minimap.                                                                                                                                         |
|                                | Padding                     | The size of the margin applied when drawing the graph.                                                                                                                                                        |
|                                | Mode Icon Tint Color        | The tint color of the mode icon displayed in the upper left of the minimap.                                                                                                                                   |
|                                | Camera Bounds Color         | The color of camera bounds displayed on the minimap.                                                                                                                                                          |
|                                | Camera Bounds Thickness     | The thickness of camera bounds displayed on the minimap.                                                                                                                                                      |
|                                | Drag Sensitivity            | The mouse sensitivity when dragging.                                                                                                                                                                          |
|                                | Draw Size And Scale         | Whether to draw the graph's drawing scale and scaled size in the upper right corner of the minimap.                                                                                                           |
|                                | Show Minimap Area           | Whether to show the name of the currently displayed minimap area on the graph minimap.                                                                                                                        |
|                                | Minimap Area Opacity        | The opacity of the name of the currently displayed minimap area on the graph minimap.                                                                                                                         |
| Graph Minimap - Remote Control | Enable Remote Control       | Whether remote control via HTTP server is enabled. Please check again when the server is rebuilt.                                                                                                             |
|                                | Http Path                   | The URL to connect to HTTP server. Disable remote control once to edit.                                                                                                                                       |
|                                | Port Number                 | The port number used to connect to the HTTP server.                                                                                                                                                           |
| Graph Minimap - Stream Deck    | Install Stream Deck Plugin  | Install the Graph Minimap plugin for Stream Deck.                                                                                                                                                             |

## Author

[Naotsun](https://twitter.com/Naotsun_UE)

## History

- (2023/05/12) v1.6   
  Added support for UE5.2    
  Added ability to show minimap for each comment (useful for huge graphs)  
  Added support for function calls from Stream Deck    

- (2022/11/08) v1.5   
  Added support for UE5.1  

- (2022/07/03) v1.4   
  Fixed a bug when the DPI scale of the OS is not 100%

- (2022/01/23) v1.3   
  Fixed a bug that autofocus to node does not work when double-clicking a function on the list

- (2022/01/17) v1.2   
  Fixed a bug that the details panel is not displayed while operating the graph

- (2022/01/15) v1.1  
  Fixed a bug that the combo box etc. flickers when displaying the mini map  
  Enabled to specify the drawing scale so that the minimap can be used in larger graphs  
  Modified the design of the minimap a little.  

- (2021/12/25) v1.0   
  Publish plugin
