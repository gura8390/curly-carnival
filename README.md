# 超苦逼冒险者
## 明眼人一看就明白，这是复刻的某个经典游戏。呃，因为我是非盈利，而且我找不到原作者，所以并不存在什么征集许可。单纯是直接进行的复刻。
> 一款复古文字风格的 HTML5 生存冒险游戏，灵感来源于经典文字 MUD 与生存沙盒玩法。

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![No Framework](https://img.shields.io/badge/No_Framework-纯原生-green)

## 游戏简介

你是一名苦逼的冒险者，被困在幽暗的森林中。为了生存，你需要采集资源、制作工具、建造庇护所、探索未知区域、与怪物战斗、与 NPC 交易。在这个残酷的世界里，饥饿、口渴、寒冷随时会夺走你的生命。

## 核心玩法

- **生存系统** — 生命 / 满腹 / 体力 / 水分 / 精神 / 体温，六维属性缺一不可
- **制作系统** — 烹饪 / 制造 / 炼金 / 科研，50+ 配方等你探索
- **建造系统** — 从木床到炼金桌，11 种建筑逐步解锁
- **地图探索** — 12 张地图，从幽暗森林到地牢深渊
- **战斗系统** — 24 种怪物，回合制战斗，暴击 / 防御 / 逃跑
- **地牢系统** — 10 层逐层推进，Boss 守关，属性随层数缩放
- **阵营选择** — 食人族（+5 攻击）或 法师（+5 魔法），不可逆转
- **NPC 交易** — 10 位 NPC，对话解锁地图，交易获取资源
- **音效系统** — Web Audio API 程序化生成 18 种音效
- **存档系统** — 自动存档 + 手动存档 + 导入导出

## 设计风格

**杂志风格 × 电子墨水美学**

- 配色：茉莉奶绿暖调（奶油底 `#f5f0e1` + 铜棕强调 `#8b7355`）
- 字体：Noto Serif SC（标题）+ Noto Sans SC（正文）+ IBM Plex Mono（数据）
- 原则：克制优于炫技，结构优于装饰，无圆角无阴影

## 快速开始

```bash
# 克隆项目
git clone https://github.com/your-username/xbvg.git

# 直接用浏览器打开
open index.html

# 或者用本地服务器
npx serve .
```

无需安装任何依赖，纯前端项目，打开即玩。

## 项目结构

```
xbvg/
├── index.html          # 主页面
├── css/
│   ├── style.css       # 主样式（杂志风格，茉莉奶绿配色）
│   ├── inventory.css   # 背包样式
│   ├── battle.css      # 战斗样式
│   └── responsive.css  # 响应式适配
└── js/
    ├── namespace.js    # 命名空间系统（window.KBA）
    ├── sound.js        # 音效系统（Web Audio API，18种音效）
    ├── utils.js        # 工具函数、UI更新、物品操作
    ├── storage.js      # 存档系统（localStorage，v5.0）
    ├── player.js       # 玩家属性、装备、魂点分配、阵营、地牢层数
    ├── time.js         # 时间系统（行动推进，非自动）
    ├── item.js         # 物品数据库 + 建筑数据库
    ├── map-data.js     # 地图数据 + 怪物数据（纯数据）
    ├── map.js          # 地图系统逻辑（交互、UI、地牢楼层）
    ├── craft.js        # 制作/烹饪/炼金/建造系统
    ├── npc.js          # NPC对话、交易、阵营选择系统
    ├── battle.js       # 战斗系统
    └── game.js         # 主逻辑、键盘快捷键、初始化
```

## 游戏流程

```
幽暗森林 → 采集基础资源
    ↓
造纸解锁地图 → 小镇 → 矿洞 → 古老废墟
    ↓
建造设施 → 烹饪/制造/炼金
    ↓
制作地牢钥匙 → 地牢10层逐层推进
    ↓
静谧森林 → 阵营选择 → 阵营地图
    ↓
击败魔王 → 通关
```

## 键盘快捷键

| 按键 | 功能 |
|------|------|
| `1-9` | 执行对应行动按钮 |
| `M` | 打开地图列表 |
| `B` | 建造菜单（仅在家） |
| `I` | 角色状态 |
| `ESC` | 关闭模态框 |

## 技术特性

- **零依赖** — 纯原生 JavaScript，无框架无构建工具
- **程序化音效** — Web Audio API 动态生成，无需外部音频文件
- **命名空间封装** — `window.KBA` 命名空间，避免全局污染
- **模块化架构** — 数据层与逻辑层分离，职责单一
- **响应式设计** — 支持移动端适配

## 许可证

MIT License

---

*苦逼冒险者，苦中作乐。*
