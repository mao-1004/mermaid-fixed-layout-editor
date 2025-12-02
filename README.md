# mermaid-fixed-layout-editor

A browser-based editor that allows you to create Mermaid-like diagrams with **fixed node positions** using GUI drag-and-drop. Built with [JointJS](https://www.jointjs.com/).

Mermaid記法ライクなテキストで構造を定義し、GUIでドラッグ＆ドロップして**座標を固定**できるエディタです。

## Features (特徴)

- **Mermaid-compatible Syntax**: Define nodes and edges using text (e.g., `A --> B`).
- **Fixed Layout**: Drag and drop nodes to fix their positions permanently.
- **Bi-directional Editing**: Text updates the graph, and graph movements update the text coordinates automatically.
- **Rich Shapes**: Supports Database (Cylinder), Stored Data, Parallelogram, etc.
- **Flexible Routing**: Uses Manhattan routing (orthogonal lines) for clean diagrams.
- **Advanced Connections**: Control connection ports with `:top` (or `:t`), `:bottom` (`:b`), `:left` (`:l`), `:right` (`:r`).

## Usage (使い方)

1. Open the [App URL](https://mao-1004.github.io/mermaid-fixed-layout-editor/).
2. Start typing or dragging!

### Syntax Example

```mermaid
// Define Node: ID[Label] @(x, y)
User[User] @(100, 100)
DB[(Database)] @(300, 100)

// Define Edge with Port: ID:port --> ID:port
// Ports: :t (top), :b (bottom), :l (left), :r (right)
User:r --> DB:l
```

## Supported Shapes

- `[ ]` : Rectangle (Process)
- `( )` : Rounded Rectangle
- `[( )]` : Cylinder (Database)
- `[[ ]]` : Stored Data (Bow-tie rect)
- `[/ /]` : Parallelogram (I/O)
- `(( ))` : Circle
- `{{ }}` : Hexagon
- `{ }` : Rhombus (Decision)
- `> ]` : Document

## Supported Arrows

| Syntax | Description |
| :--- | :--- |
| `-->` | Solid arrow (Standard) |
| `-.->` | Dotted arrow |
| `==>` | Thick arrow |
| `---` | Solid link (No arrow) |
| `<-->` | Bidirectional solid arrow |
| `<-.->` | Bidirectional dotted arrow |
| `<==>` | Bidirectional thick arrow |

## License

This project is licensed under the MIT License.

## Credits

- Visualization Library: [JointJS](https://github.com/clientIO/joint) (Mozilla Public License 2.0)
- Icon & Inspiration: [Mermaid-js](https://mermaid.js.org/)
