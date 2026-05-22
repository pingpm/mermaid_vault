# Mermaid 可视化编辑器 JSON 存储格式结构与字段标注说明

本文档详细介绍了 Mermaid 可视化编辑器中 **4 种核心图表编辑器**（标准流程图、思维导图、泳道流程图、时序图）的 JSON 存储数据格式结构。

每种图表的 JSON 结构均包含其核心节点、边/连接线以及全局配置字段。我们在数据存储层对这些数据结构进行了精细的设计，以保证其能够无缝转换为对应的 Mermaid.js 代码语法，并且能够在 React 渲染引擎中呈现丰富的自定义样式。

---

## 目录

1. [标准流程图编辑器 (Flowchart)](#1-标准流程图编辑器-flowchart)
2. [思维导图编辑器 (Mindmap)](#2-思维导图编辑器-mindmap)
3. [泳道流程图编辑器 (Swimlane)](#3-泳道流程图编辑器-swimlane)
4. [时序图编辑器 (Sequence Diagram)](#4-时序图编辑器-sequence-diagram)
5. [Markdown 编辑器 (Markdown)](#5-markdown-编辑器-markdown)

---

## 1. 标准流程图编辑器 (Flowchart)

标准流程图采用 ReactFlow (`@xyflow/react`) 进行节点和边线的托拽管理与交互渲染。其 JSON 数据包含节点数组 `nodes`、边线数组 `edges` 以及全局布局参数。

### 1.1 完整数据结构示例

```json
{
  "nodes": [
    {
      "id": "e67b2d56-78ab-49cd-a012-ef3456789abc",
      "type": "flow-process",
      "position": { "x": 150, "y": 200 },
      "parentId": "subgraph-group-id",
      "extent": "parent",
      "style": { "width": 160, "height": 56 },
      "data": {
        "label": "普通步骤节点",
        "width": 160,
        "height": 56,
        "textAlign": "center",
        "tag": "new",
        "tagNote": "这步是新增的核心业务逻辑",
        "customColors": {
          "bg": "#3b82f6",
          "border": "#1d4ed8",
          "text": "#ffffff"
        }
      }
    }
  ],
  "edges": [
    {
      "id": "edge-f123-e456",
      "source": "e67b2d56-78ab-49cd-a012-ef3456789abc",
      "target": "target-node-uuid",
      "sourceHandle": "right-source",
      "targetHandle": "left-target",
      "type": "flow-edge",
      "label": "流转条件",
      "style": {
        "stroke": "#4f46e5",
        "strokeDasharray": "6 3",
        "strokeWidth": 2.8
      },
      "markerEnd": {
        "type": "arrowclosed",
        "color": "#4f46e5",
        "width": 18,
        "height": 18
      },
      "data": {
        "label": "流转条件",
        "color": "#4f46e5",
        "lineStyle": "dashed",
        "arrowHead": "arrow",
        "edgeStyleOverride": "smooth",
        "textAlign": "center"
      }
    }
  ],
  "flowEdgeStyle": "smooth",
  "flowDirection": "LR",
  "mermaidCode": "flowchart LR\n  subgraph subgraph-group-id[\"子图容器\"]\n    t_0[\"普通步骤节点\"]\n  end\n  t_0 -.->|\"流转条件\"| t_1"
}
```

### 1.2 字段说明

#### A. 核心字段 (Root Level)





| 字段名 | 类型 | 说明 | 可选值 |
| --- | --- | --- | --- |
| `nodes` | `Array` | 节点数组。描述画布上的所有图形。 | - |
| `edges` | `Array` | 边线数组。描述节点之间的连接和线条样式。 | - |
| `flowEdgeStyle` | `String` | 全局默认的线条样式。 | `'smooth'` (平滑圆弧), `'orthogonal'` (直角折线), `'curve'` (贝塞尔曲线), `'straight'` (直线) |
| `flowDirection` | `String` | 全局流程图布局方向。 | `'TD'` (从上到下), `'LR'` (从左到右), `'BT'` (从下到上), `'RL'` (从右到左) |
| `mermaidCode` | `String` | 自动渲染出的 Mermaid.js 流程图代码字符串。 | - |

#### B. 节点对象字段 (`nodes[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 节点的唯一标识符 (UUID)。 | `"e67b2d56-78ab-49cd-a012-ef3456789abc"` |
| `type` | `String` | 节点形状类型，用于指定定制化的渲染组件。 | `'flow-process'` (普通步骤矩形/圆角)<br/>`'flow-process-rect'` (直角矩形)<br/>`'flow-terminator'` (起止圆角舱/胶囊)<br/>`'flow-decision'` (决策菱形)<br/>`'flow-database'` (数据库圆柱)<br/>`'flow-manual'` (手工操作梯形)<br/>`'flow-document'` (文档波浪底)<br/>`'flow-predefined'` (预定义子流程双边矩形)<br/>`'flow-note'` (便签/备注)<br/>`'flow-subgraph'` (子图容器) |
| `position` | `Object` | 节点在画布上的 2D 坐标。包含 `x` 和 `y` 的数值。 | `{"x": 100, "y": 150}` |
| `parentId` | `String` | （可选）若节点位于子图 (Subgraph) 内，则指向父子图节点的 `id`。 | `"subgraph-group-uuid"` |
| `extent` | `String` | （可选）限定子节点无法拖出父容器边缘。 | `'parent'` |
| `style` | `Object` | （可选）节点的高宽等样式包裹层。 | `{"width": 160, "height": 56}` |
| `data` | `Object` | 存储节点的核心数据属性与样式配置。 | 详见下方 `data` 表 |

**`nodes[...].data` 内部字段说明：**





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `label` | `String` | 节点文本标签内容。支持多行（在 Mermaid 中会转义为 `<br/>`）。 | `"核心处理步骤"` |
| `width` | `Number` | （可选）缩放后的显式宽度。 | `160` |
| `height` | `Number` | （可选）缩放后的显式高度。 | `56` |
| `textAlign` | `String` | （可选）文本对齐方式。 | `'left'`, `'center'`, `'right'` |
| `tag` | `String` | （可选）需求跟踪标签类别。 | `'new'` (新增), `'existing'` (已有), `'pending'` (待确认), `'other'` (其他) |
| `tagNote` | `String` | （可选）需求跟踪标签的详细备注信息。 | `"暂定方案，下周与架构组复核"` |
| `customColors` | `Object` | （可选）用户自定义的填充颜色。若不设则取全局主题色。 | `{"bg": "#fef3c7", "border": "#d97706", "text": "#92400e"}` |

#### C. 边线对象字段 (`edges[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 边线的唯一标识符。 | `"edge-uuid"` |
| `source` | `String` | 起始源节点的 UUID。 | `"node-1-uuid"` |
| `target` | `String` | 终止目标节点的 UUID。 | `"node-2-uuid"` |
| `sourceHandle` | `String` | （可选）起始节点锚点方向。 | `'right-source'`, `'bottom-source'`, `'top-source'`, `'left-source'` |
| `targetHandle` | `String` | （可选）目标节点锚点方向。 | `'left-target'`, `'top-target'`, `'right-target'`, `'bottom-target'` |
| `type` | `String` | 连线渲染器类型。 | `"flow-edge"` |
| `label` | `String` | （可选）线条上的说明文字。 | `"Y"` / `"条件成立"` |
| `style` | `Object` | 线条渲染的 SVG 路径样式。 | `{"stroke": "#6366f1", "strokeWidth": 2.8}` |
| `markerEnd` | `Object` | 终点箭头定义。 | `{"type": "arrowclosed", "color": "#6366f1"}` |
| `data` | `Object` | 存储边线上的高度自定义参数。 | 详见下方 `data` 表 |

**`edges[...].data` 内部字段说明：**





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `label` | `String` | 边线文本。 | `"通过"` |
| `color` | `String` | （可选）边线条自定义笔触颜色（Hex）。 | `"#10b981"` |
| `lineStyle` | `String` | 线条虚实类型。 | `'solid'` (实线), `'dashed'` (虚线), `'thick'` (粗实线) |
| `arrowHead` | `String` | 线条两端箭头指示样式。 | `'arrow'` (单向箭头 `-->`), `'none'` (无箭头 `---`), `'double'` (双向 `<-->`), `'circle'` (空心圆 `--o`), `'cross'` (叉叉 `--x`) |
| `edgeStyleOverride` | `String` | （可选）单条边线特有线条路径样式，覆盖全局 `flowEdgeStyle`。 | `'smooth'`, `'orthogonal'`, `'curve'`, `'straight'` |
| `textAlign` | `String` | 线条文字对齐位置。 | `'left'`, `'center'`, `'right'` |

---

## 2. 思维导图编辑器 (Mindmap)

思维导图数据采用树形节点层次列表表示。依靠 parent-child 链条关系渲染层级图，能够无缝导出为符合 Mermaid `mindmap` 标准的缩进大纲。

### 2.1 完整数据结构示例

```json
{
  "nodes": [
    {
      "id": "root-uuid",
      "label": "中心主题 (Root)",
      "parentId": null,
      "order": 0
    },
    {
      "id": "node-child-1",
      "label": "分支一",
      "parentId": "root-uuid",
      "order": 0,
      "collapsed": false
    },
    {
      "id": "node-child-2",
      "label": "分支二",
      "parentId": "root-uuid",
      "order": 1,
      "collapsed": true
    }
  ],
  "mmLayout": "both",
  "mmNodeStyle": "box",
  "mmBgPattern": "dots",
  "mmEdgeStyle": "curve",
  "mmTheme": "default",
  "mmSlotOverrides": {
    "1": { "stroke": "#ef4444" },
    "2": { "stroke": "#3b82f6" }
  },
  "mermaidCode": "mindmap\n  root((中心主题 (Root)))\n    分支一\n"
}
```

### 2.2 字段说明

#### A. 核心配置字段 (Root Level)





| 字段名 | 类型 | 说明 | 可选值 |
| --- | --- | --- | --- |
| `nodes` | `Array` | 思维导图所有层级节点的平面列表数组。通过 `parentId` 链接建树。 | - |
| `mmLayout` | `String` | 导图展示形态布局。 | `'right'` (偏右单向), `'left'` (偏左单向), `'both'` (向两侧辐射), `'down'` (向下排列) |
| `mmNodeStyle` | `String` | 节点边框样式。 | `'box'` (完整方框), `'underline'` (底部单横线下划线), `'plain'` (纯文本无边框) |
| `mmBgPattern` | `String` | 画布背景底纹。 | `'none'`, `'dots'` (网格圆点), `'lines'` (网格线条) |
| `mmEdgeStyle` | `String` | 分支线条连接风格。 | `'curve'` (平滑曲线), `'straight'` (直线折线), `'orthogonal'` (直角折线), `'rounded'` (带圆角的直角折线) |
| `mmTheme` | `String` | 导图全局色彩主题。 | `'default'`, `'ocean'`, `'sunset'`, `'monochrome'` |
| `mmSlotOverrides` | `Object` | 键值对映射，按照深度层级 (Depth) 独立覆写线条的笔触色彩样式。 | 键为数字（深度），值为包含颜色配置的对象，如 `{"1": {"stroke": "#hex"}}` |
| `mermaidCode` | `String` | 生成的 Mermaid.js 思维导图原生缩进大纲字符串。 | - |

#### B. 节点对象字段 (`nodes[...]`)





| 字段名 | 类型 | 说明 | 可选值/示例 |
| --- | --- | --- | --- |
| `id` | `String` | 节点的唯一 UUID。 | `"node-child-1"` |
| `label` | `String` | 节点显示文本标签。 | `"主线业务板块"` |
| `parentId` | `String` | 父节点的 `id`。**根节点必须为 `null`**。 | `"parent-node-uuid"` / `null` |
| `order` | `Number` | 同级兄弟节点中的展示排列顺序（0-based，数字小的排在前面/上方）。 | `0`, `1`, `2` |
| `collapsed` | `Boolean` | （可选）折叠标记。为 `true` 时，该节点的所有子分支将在画布及生成的 Mermaid 代码中被隐藏。 | `true` / `false` |

---

## 3. 泳道流程图编辑器 (Swimlane)

泳道图（跨职能流程图）通过将流程节点按职能模块/系统划分为不同的“通道”(Lanes) 来展示流转。在存储层，它不仅保存通道定义和节点，还包含了细致的 2D 绝对坐标定位（同时兼容传统行列网格坐标）。

### 3.1 完整数据结构示例

```json
{
  "lanes": [
    {
      "id": "lane-user",
      "label": "用户端",
      "order": 0,
      "width": 300,
      "height": 500,
      "labelVertical": false,
      "customColors": { "bg": "#f8fafc", "border": "#cbd5e1", "text": "#0f172a" }
    }
  ],
  "tasks": [
    {
      "id": "task-login",
      "laneId": "lane-user",
      "label": "点击登录",
      "shape": "process",
      "order": 0,
      "x": 60,
      "y": 40,
      "width": 156,
      "height": 56,
      "textAlign": "center",
      "tag": "existing",
      "tagNote": "复用已有登录组件",
      "customColors": { "bg": "#eff6ff", "border": "#3b82f6", "text": "#1e3a8a" }
    }
  ],
  "connections": [
    {
      "id": "conn-1",
      "fromTaskId": "task-login",
      "toTaskId": "task-auth",
      "label": "提交凭证",
      "sourceHandle": "right-source",
      "targetHandle": "left-target",
      "lineStyle": "solid",
      "arrowHead": "arrow",
      "edgeStyle": "orthogonal",
      "color": "#3b82f6",
      "textAlign": "center"
    }
  ],
  "swBgPattern": "lines",
  "swDirection": "LR",
  "swEdgeStyle": "orthogonal",
  "swTheme": "default",
  "swLaneGap": 24,
  "swLaneColorOverrides": {},
  "mermaidCode": "flowchart LR\n  subgraph lane_0[\"用户端\"]\n    t_0[\"点击登录\"]\n  end\n"
}
```

### 3.2 字段说明

#### A. 核心配置字段 (Root Level)





| 字段名 | 类型 | 说明 | 可选值 |
| --- | --- | --- | --- |
| `lanes` | `Array` | 通道（泳道栏）的定义列表。 | - |
| `tasks` | `Array` | 画布中被归属于各个通道的卡片/步骤节点列表。 | - |
| `connections` | `Array` | 泳道图内各个卡片节点之间的关系连线。 | - |
| `swBgPattern` | `String` | 泳道画布背景底纹。 | `'none'`, `'dots'`, `'lines'` |
| `swDirection` | `String` | 全局通道的排列方向。 | `'LR'` (水平泳道：通道从上往下堆叠，流程从左往右流转)<br/>`'TD'` (垂直泳道：通道从左往右排列，流程从上往下流转) |
| `swEdgeStyle` | `String` | 默认连线折现算法。 | `'smooth'`, `'orthogonal'` (泳道图推荐直角), `'curve'`, `'straight'` |
| `swTheme` | `String` | 全局主题色彩风格。 | `'default'`, `'ocean'`, `'sunset'`, `'monochrome'` |
| `swLaneGap` | `Number` | 各泳道通道之间的视觉间距。 | 默认 `24` |
| `swLaneColorOverrides` | `Object` | 通道栏高级独立颜色重写映射列表。 | - |
| `mermaidCode` | `String` | 转换为含有子图 `subgraph` 的 Mermaid flowchart 代码。 | - |

#### B. 泳道通道对象字段 (`lanes[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 通道唯一识别 UUID。 | `"lane-user"` |
| `label` | `String` | 泳道标题（如：“财务部门”、“后台系统”）。 | `"用户端"` |
| `order` | `Number` | 泳道相对层级渲染的排序指数 (0-based)。 | `0`, `1` |
| `width` | `Number` | （可选）泳道宽度（在水平泳道代表横向展开的长度）。 | `300` |
| `height` | `Number` | （可选）泳道高度（在水平泳道代表泳道的栏高）。 | `500` |
| `labelVertical` | `Boolean` | （可选）是否在通道侧边栏/顶部栏中把文本垂直旋转 90° 渲染。 | `true` / `false` |
| `customColors` | `Object` | （可选）指定通道标题栏与内部背景的独特色彩。 | `{"bg": "#fff", "border": "#ccc", "text": "#111"}` |

#### C. 卡片任务节点对象字段 (`tasks[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 任务卡片唯一 UUID。 | `"task-login"` |
| `laneId` | `String` | 强绑定该任务当前所在的所属 `lane` 的 `id`。 | `"lane-user"` |
| `label` | `String` | 卡片内文本内容。支持多行编写。 | `"点击登录"` |
| `shape` | `String` | 泳道卡片支持的几何构型。 | `'process'` (步骤矩形)<br/>`'decision'` (决策菱形)<br/>`'terminator'` (起止圆角舱)<br/>`'document'` (文档形态) |
| `order` | `Number` | 同一通道下的卡片排序序号（旧版本兼容）。 | `0` |
| `x` | `Number` | 任务在所属通道内部相对内容区的局部 X 轴坐标像素。 | `60` |
| `y` | `Number` | 任务在所属通道内部相对内容区的局部 Y 轴坐标像素。 | `40` |
| `width` | `Number` | 卡片框显式渲染宽度。 | `156` |
| `height` | `Number` | 卡片框显式渲染高度。 | `56` |
| `textAlign` | `String` | 文本对齐方式。 | `'left'`, `'center'`, `'right'` |
| `tag` | `String` | 跟踪状态的标签标记。 | `'new'`, `'existing'`, `'pending'`, `'other'` |
| `tagNote` | `String` | 跟踪状态下记录的特定业务解释。 | `"需协调前端联调"` |
| `customColors` | `Object` | 自定义节点背景、边框与文字颜色。 | `{"bg": "#ffc", "border": "#fa0", "text": "#000"}` |

#### D. 线条连接对象字段 (`connections[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 连线唯一 UUID。 | `"conn-1"` |
| `fromTaskId` | `String` | 起始任务卡片的 UUID。 | `"task-login"` |
| `toTaskId` | `String` | 目标任务卡片的 UUID。 | `"task-auth"` |
| `label` | `String` | （可选）线条文字标签。 | `"成功"` / `"重试"` |
| `sourceHandle` | `String` | 起点连接的锚点方向位置。 | `'right-source'`, `'bottom-source'` 等 |
| `targetHandle` | `String` | 终点连接的锚点方向位置。 | `'left-target'`, `'top-target'` 等 |
| `lineStyle` | `String` | 线条边框样式。 | `'solid'` (实线), `'dashed'` (虚线), `'thick'` (粗线条) |
| `arrowHead` | `String` | 箭头端点视觉。 | `'arrow'` (单向), `'none'` (无箭头), `'double'` (双向), `'circle'` (空心圆), `'cross'` (叉叉) |
| `edgeStyle` | `String` | （可选）独立控制该条线的多样折线路径算法，覆写全局。 | `'smooth'`, `'orthogonal'`, `'curve'`, `'straight'` |
| `color` | `String` | （可选）独立的线条笔触颜色 Hex。 | `"#3b82f6"` |
| `textAlign` | `String` | 文字在边线上的局部对齐位置。 | `'left'`, `'center'`, `'right'` |

---

## 4. 时序图编辑器 (Sequence Diagram)

时序图（序列图）用来描述系统交互、生命周期以及在垂直时间轴上发生的信息交互流转。存储结构基于生命线（列）、消息事件（行）、备注及组合逻辑片段。

### 4.1 完整数据结构示例

```json
{
  "lifelines": [
    { "id": "life-client", "label": "客户端", "kind": "actor", "order": 0 },
    { "id": "life-server", "label": "服务器", "kind": "entity", "order": 1 },
    { "id": "life-db", "label": "数据库", "kind": "database", "order": 2 }
  ],
  "messages": [
    {
      "id": "msg-query",
      "from": "life-client",
      "to": "life-server",
      "label": "GET /api/user",
      "type": "sync",
      "order": 0,
      "linkId": "link-api-doc"
    },
    {
      "id": "msg-response",
      "from": "life-server",
      "to": "life-client",
      "label": "HTTP 200 OK",
      "type": "return",
      "order": 1,
      "replyToId": "msg-query"
    }
  ],
  "notes": [
    {
      "id": "note-1",
      "text": "数据缓存命中",
      "position": "over",
      "lifelineIds": ["life-server"],
      "afterOrder": 0,
      "textAlign": "left",
      "width": 120
    }
  ],
  "fragments": [
    {
      "id": "frag-1",
      "kind": "alt",
      "label": "缓存命中",
      "startOrder": 0,
      "endOrder": 1,
      "branches": [
        { "condition": "未命中，读取DB", "startOrder": 1, "endOrder": 1 }
      ]
    }
  ],
  "links": [
    { "id": "link-api-doc", "name": "API 接口文档", "url": "https://api.domain.com/docs" }
  ],
  "colWidths": { "life-client": 120, "life-server": 140 },
  "gaps": { "life-client": 160 },
  "lifelineStyle": "dashed",
  "boxStyle": "rounded",
  "mermaidCode": "sequenceDiagram\n  actor life-client as 客户端\n  participant life-server as 服务器\n  life-client->>life-server: GET /api/user\n"
}
```

### 4.2 字段说明

#### A. 核心字段 (Root Level)





| 字段名 | 类型 | 说明 | 可选值 |
| --- | --- | --- | --- |
| `lifelines` | `Array` | 交互参与主体（垂直立柱生命线）。 | - |
| `messages` | `Array` | 生命线之间发送的消息及事件流转列表。代表时序中的每一行消息线。 | - |
| `notes` | `Array` | 挂载在时序特定事件节点上的文本注释框。 | - |
| `fragments` | `Array` | 组合片段。描述可选条件 (opt)、循环 (loop)、多分支 (alt) 或并发 (par) 等控制逻辑块。 | - |
| `links` | `Array` | 用于挂载在消息事件上的超链接，点击可跳转。 | - |
| `colWidths` | `Object` | 各列参与者方框在编辑器中的自定义渲染宽度。键为生命线 `id`，值为宽度。 | `{"life-uuid": 120}` |
| `gaps` | `Object` | 生命线之间的自定义跨度距离。键为生命线 `id`，值为间距数值。 | `{"life-uuid": 150}` |
| `lifelineStyle` | `String` | 垂直虚线杆渲染线型。 | `'dashed'` (默认虚线), `'solid'` (实线) |
| `boxStyle` | `String` | 顶部参与者容器方框的圆角风格。 | `'rounded'` (带圆角), `'square'` (纯直角) |
| `mermaidCode` | `String` | 导出的标准 Mermaid `sequenceDiagram` 时序图代码。 | - |

#### B. 参与者生命线对象字段 (`lifelines[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 参与者唯一标识 UUID。 | `"life-client"` |
| `label` | `String` | 参与者名称（首尾方框中显示的标题）。 | `"客户端"` / `"支付网关"` |
| `kind` | `String` | 参与者的图形类别角色类型。在 Mermaid 中支持各种特定图标修饰。 | `'entity'` (普通组件/圆框)<br/>`'actor'` (人偶图标)<br/>`'database'` (数据库图标)<br/>`'boundary'` (控制边界)<br/>`'control'` (逻辑控制器)<br/>`'collections'` (集合组件)<br/>`'queue'` (消息队列) |
| `order` | `Number` | 横向从左到右的位置次序 (0-based)。 | `0`, `1`, `2` |

#### C. 消息事件线对象字段 (`messages[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 消息唯一 UUID。 | `"msg-query"` |
| `from` | `String` | 发出消息的生命线 `id`。 | `"life-client"` |
| `to` | `String` | 接收消息的生命线 `id`。 | `"life-server"` |
| `label` | `String` | 消息线上的说明文字。 | `"GET /api/user"` |
| `type` | `String` | 消息线及箭头的具体形态。 | `'sync'` (同步消息：实线实心箭头 `->>`) <br/>`'async'` (异步消息：实线半箭头 `->`) <br/>`'return'` (返回消息：虚线半箭头 `-->>` / `-->`) <br/>`'create'` (新建事件) <br/>`'destroy'` (销毁事件) |
| `order` | `Number` | 垂直时序中的绝对从上到下执行次序号。 | `0`, `1`, `2` |
| `replyToId` | `String` | （可选）若当前是返回消息，绑定它所对应的发起消息的 `id`。 | `"msg-query"` |
| `linkId` | `String` | （可选）关联的 `links` 列表超链接 UUID。 | `"link-api-doc"` |

#### D. 便签备注对象字段 (`notes[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 便签唯一 UUID。 | `"note-1"` |
| `text` | `String` | 便签注释文字内容。 | `"本地内存缓存 15s"` |
| `position` | `String` | 便签在生命线前后的相对展示位置。 | `'over'` (跨接在生命线上)<br/>`'left of'` (处于某生命线左侧)<br/>`'right of'` (处于某生命线右侧) |
| `lifelineIds` | `Array` | 数组（通常单个或多个 UUID）。指定便签挂靠在哪些生命线下方。如果是 `'over'` 且包含两个 ID，则便签会横跨在这两条生命线中间。 | `["life-server"]` / `["life-server", "life-db"]` |
| `afterOrder` | `Number` | 顺序标定。指示该 Note 渲染在哪一条 `message` 事件下方。`-1` 代表在整张时序图的最上方。 | `-1`, `0`, `1` |
| `textAlign` | `String` | （可选）文本排版位置。 | `'left'`, `'center'`, `'right'` |
| `width` | `Number` | （可选）定制备注便签的高级渲染宽度像素。 | `120` |

#### E. 逻辑组合片段字段 (`fragments[...]`)





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `id` | `String` | 片段块唯一 UUID。 | `"frag-1"` |
| `kind` | `String` | 片段的分组逻辑特性。 | `'loop'` (循环), `'alt'` (多分支条件选择), `'opt'` (可选逻辑), `'par'` (并行处理), `'critical'` (临界区), `'break'` (中断步骤), `'ref'` (参考外部) |
| `label` | `String` | 片段框顶部显示的条件文字说明（主分支）。 | `"已命中缓存"` |
| `startOrder` | `Number` | 包裹的时间范围：起始 `message` 的 `order` 索引。 | `0` |
| `endOrder` | `Number` | 包裹的时间范围：截止 `message` 的 `order` 索引。 | `2` |
| `branches` | `Array` | （仅在 `alt` 类型下使用）描述“其他/否则 (else)”的子选择分支列表。 | 详见下方 `branches` 表 |

**`fragments[...].branches[...]` (分支) 字段说明：**





| 字段名 | 类型 | 说明 | 示例/可选值 |
| --- | --- | --- | --- |
| `condition` | `String` | 否则分支的条件判定文字。 | `"缓存未命中，需要访问数据库"` |
| `startOrder` | `Number` | 分支范围开始的 `message` 索引值。 | `1` |
| `endOrder` | `Number` | 分支范围结束的 `message` 索引值。 | `2` |

---

## 5. Markdown 编辑器 (Markdown)

Markdown 编辑器是一个全文本编辑器，用于支持用户直接使用 Markdown 标记语言写作。其存储格式极其扁平。

### 5.1 完整数据结构示例

```json
{
  "content": "# 周报总结\n\n- 完成了支付系统泳道图的设计\n- 绘制了接口时序图\n\n```mermaid\nflowchart LR\n  A --> B\n```",
  "mermaidCode": "# 周报总结\n\n- 完成了支付系统泳道图的设计\n- 绘制了接口时序图\n\n```mermaid\nflowchart LR\n  A --> B\n```"
}
```

### 5.2 字段说明





| 字段名 | 类型 | 说明 | 示例 |
| --- | --- | --- | --- |
| `content` | `String` | 用户编辑的完整 Markdown 内容。可能内嵌 Mermaid 代码块。 | `"# 标题\n内容..."` |
| `mermaidCode` | `String` | `content` 字段的冗余/备份字段，保证编辑器切换与读取的数据一致性。 | `"# 标题\n内容..."` |

---

## 数据转换与导出设计原则

在系统数据架构中，这四种图形化编辑器均采取 **“图形化拖拽属性模型 (Zustand 状态机)  <===> 原生 Mermaid.js 文本代码”** 的双向实时编译架构：

1. **序列化 (Serialization)**：当用户在 UI 画布上拖拽节点、修改属性或增删连接时，系统会立即触发状态机，调用对应的 `generateXXXMermaid()` 引擎，生成纯 ASCII Mermaid 源码，驱动右侧预览窗口。
2. **反序列化 (Deserialization)**：当用户在代码面板直接修改 Mermaid 代码时，解析引擎（如 `parseMermaidToFlow`, `parseMermaidToSwimlane` 等）会运行正则表达式与语法解析器，将文本逆向编译为对应的 JSON 并注入 Zustand Store，重新绘制图形画布。

通过这种方式，JSON 数据存储了丰富的高级 UI 样式（如像素位置、自定义配色、文字对齐、特定便签标签等），而生成的 Mermaid 源码则具备最大的通用性与跨平台导出能力。