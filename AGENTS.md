# AGENTS.md — LANDSLIDE Introduction Page

## 项目概览
LANDSLIDE 社区静态介绍页面，采用 Micrographics 设计风格（密集技术信息海报美学）。页面以产品技术规格说明书的形式呈现社区信息，包含序列号、坐标网格、技术标签等装饰元素。

## 技术栈
- **类型**: 原生静态页面 (native-static)
- **文件**: `index.html` + `styles/main.css`
- **字体**: Inter (sans-serif) + JetBrains Mono (monospace)，通过 Google Fonts 加载
- **服务器**: Python `http.server` (端口 5000)

## 项目结构
```
/workspace/projects/
── index.html          # 主页面（Micrographics 风格布局）
├── styles/
│   └── main.css        # 样式文件（网格系统、模块样式、装饰元素）
├── DESIGN.md           # 设计规范文档
├── AGENTS.md           # 本文件
└── .coze               # 项目配置
```

## 页面模块
| 编号 | 模块 | 内容 |
|------|------|------|
| 000 | Hero | 社区名称、标语、技术规格参数 |
| 001 | About | 社区概述、使命、类型、语言 |
| 002 | Focus Areas | 四大研究方向（多智能体、人机协作、视觉生成、自由探索） |
| 003 | Projects | 活跃项目列表（Sphinx、.github） |
| 004 | How to Join | 加入流程（3步） |
| 005 | Ground Rules | 社区规则（6条） |
| 006 | Getting Started | 入门序列（3步） |
| CTA | Call to Action | 加入号召（黑色背景高对比区域） |
| Footer | 页脚 | 组织信息、规格、坐标、认证标志、条形码 |

## 设计规范要点
- **配色**: 纯黑 #000 / 纯白 #FFF / 灰色系渐变
- **字体**: 等宽字体用于编号/坐标/标签，无衬线字体用于标题/正文
- **布局**: 严格网格系统，模块间细线分隔，每个模块有编号和坐标标注
- **装饰**: 十字准星、条形码、序列号、状态徽章、虚线分隔
- **禁忌**: 无渐变/发光/阴影、无圆角卡片、无彩色图标、无大段留白

## 开发命令
```bash
# 启动开发服务器
python -m http.server 5000 --bind 0.0.0.0

# 构建（静态项目无需构建）
# 无构建步骤
```

## 修改指南
- **修改内容**: 编辑 `index.html` 对应模块的 HTML 结构
- **修改样式**: 编辑 `styles/main.css`，按模块注释定位
- **添加模块**: 在 `index.html` 中添加新的 `<section class="module">` 块，在 CSS 中添加对应样式
- **修改配色**: 调整 `:root` 中的 CSS 变量
- **响应式**: 媒体查询断点为 900px 和 600px
