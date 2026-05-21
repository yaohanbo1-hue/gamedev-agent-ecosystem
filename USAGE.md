# 🚀 使用指南

## 什么是 GameDev Agent Ecosystem？

一套运行在 **WorkBuddy** 上的游戏开发 AI 团队，包含 58 个专业 Agent。  
你只需像对话一样输入需求，Agent 就会以对应专业角色给出专业输出。

---

## 快速上手

### Step 1：打开 WorkBuddy

进入 [WorkBuddy](https://workbuddy.com) 并创建新会话。

### Step 2：选择 Agent

把对应 Agent 的 **System Prompt**（见 `AGENTS/` 目录）复制到 WorkBuddy 的系统提示或首条消息中。

### Step 3：输入你的任务

直接用自然语言描述任务，Agent 会按其专业角色给出输出。

---

## 使用模式

### 模式一：单 Agent 直接使用

适合：**单一任务**，比如只想生成关卡、只想写对话

**格式**：
```
你是 [Agent角色名]，[Agent职责简述]。

[你的具体任务]
```

**示例 1 - 关卡设计**：
```
你是 LevelDesigner（关卡设计师），专注于 Roblox Obby 游戏设计。

请为我设计 5 个关卡：
- 第 1 关：1 星难度，简单跳跃平台
- 第 3 关：3 星难度，加入移动障碍物
- 第 5 关：5 星难度，组合技巧障碍

每个关卡输出：关卡名称、难度、平台布局、障碍物类型、通关技巧
```

**示例 2 - 叙事设计**：
```
你是 NarrativeWriter（叙事设计师），擅长历史题材互动剧情。

为鸿门宴游戏设计"项庄舞剑"场景的对话：
- 玩家扮演刘邦
- 设计 3 个选择：①假装镇定 ②借机离席 ③正面斡旋
- 每个选择对应不同的后续剧情和属性变化（勇气/智谋/运气）
```

**示例 3 - 数值分析**：
```
你是 BalanceAnalyzer（数值平衡分析师），擅长游戏经济系统分析。

分析以下打工生活模拟器的经济数值是否平衡：
- 初始金钱：100元
- 普通打工日收入：50元
- 房租每天：30元
- 食物每天：20元
- 升职需要：存款达到 500 元

输出：问题分析、具体调整建议、调整后的预期体验
```

---

### 模式二：多 Agent 流水线

适合：**完整流程任务**，比如从策划到开发的全流程

**方式**：在同一会话中依次激活不同 Agent，上一个的输出作为下一个的输入。

**示例 - 独立游戏快速立项**：

```
# 第 1 步 - 市场调研
你是 MarketResearcher（市场调研专家）。
分析 2026 年 Roblox 平台上 Obby 类游戏的市场现状，
给出：市场规模、热门方向、差异化机会。

# 第 2 步 - 用上面的结论，做玩法设计
你是 GameplayDesigner（核心玩法设计师）。
基于以上市场分析，为一款差异化 Obby 游戏设计核心玩法：
核心循环、特色机制、与竞品的差异点。

# 第 3 步 - 关卡生成
你是 LevelDesigner（关卡设计师）。
基于以上玩法设计，生成第一世界的 5 个关卡配置。
```

---

### 模式三：Command Center 全局调度

适合：**大型项目**，需要多个领域并行推进

```
你是 GameDev Command Center（游戏开发总指挥），负责协调整个 Agent 团队。

我需要开发一款 Roblox 休闲解谜游戏，请：
1. 分解开发任务
2. 指定每个任务应由哪个 Agent 负责
3. 给出并行推进的建议顺序
```

---

## 完整 Agent 列表

| # | Agent 名称 | 角色 | 触发场景 |
|---|-----------|------|----------|
| 0 | GameDev Command Center | 总指挥 | 复杂多任务调度 |
| 1-1 | MarketResearcher | 市场调研 | 立项前市场分析 |
| 1-2 | CompetitorAnalyst | 竞品分析 | 研究竞争对手 |
| 1-3 | UserResearcher | 用户研究 | 了解目标玩家 |
| 1-4 | BusinessModeler | 商业模式 | 变现策略设计 |
| 1-5 | RiskAssessor | 风险评估 | 项目风险识别 |
| 1-6 | TrendForecaster | 趋势预测 | 行业趋势分析 |
| 2-1 | ProjectManager | 项目经理 | 制定开发计划 |
| 2-2 | ResourceAllocator | 资源分配 | 团队资源规划 |
| 2-3 | ScrumMaster | 敏捷教练 | 敏捷流程落地 |
| 2-4 | ScheduleBuilder | 排期专家 | 制定时间表 |
| 2-5 | BudgetController | 预算控制 | 成本规划 |
| 2-6 | MilestoneTracker | 里程碑追踪 | 进度管理 |
| 2-7 | DependencyMapper | 依赖管理 | 任务依赖分析 |
| 2-8 | ChangeController | 变更控制 | 需求变更管理 |
| 3-1 | GameplayDesigner | 玩法设计师 | 核心玩法设计 |
| 3-2 | LevelDesigner | 关卡设计师 | 关卡生成 |
| 3-3 | NarrativeWriter | 叙事设计师 | 剧情对话生成 |
| 3-4 | CharacterDesigner | 角色设计师 | 角色设定 |
| 3-5 | WorldBuilder | 世界观构建 | 设定构建 |
| 3-6 | ProgressionDesigner | 进度系统 | 成长体系设计 |
| 3-7 | EconomyDesigner | 经济系统 | 数值经济设计 |
| 3-8 | QuestDesigner | 任务设计师 | 任务系统设计 |
| 3-9 | DifficultyTuner | 难度调校 | 难度曲线调整 |
| 3-10 | UIDesigner | UI设计师 | 界面设计 |
| 4-1 | ArchitectureDesigner | 架构设计 | 技术架构规划 |
| 4-2 | GameplayProgrammer | 逻辑程序员 | 核心逻辑开发 |
| 4-3 | CombatDesigner | 战斗程序员 | 战斗系统开发 |
| 4-4 | AIController | AI程序员 | NPC行为开发 |
| 4-5 | NetworkEngineer | 网络工程师 | 多人联网开发 |
| 4-6 | BackendDeveloper | 后端工程师 | 服务器开发 |
| 4-7 | FrontendDeveloper | 前端工程师 | 客户端界面 |
| 4-8 | UIProgrammer | UI程序员 | 界面逻辑开发 |
| 4-9 | DataPersistence | 数据持久化 | 存储方案设计 |
| 4-10 | SaveSystem | 存档系统 | 存档功能开发 |
| 4-11 | PerformanceOptimizer | 性能优化 | 性能分析优化 |
| 4-12 | LocalizationEngineer | 本地化 | 多语言适配 |
| 4-13 | PluginDeveloper | 插件开发 | 插件扩展开发 |
| 4-14 | DevOpsEngineer | DevOps | 自动化部署 |
| 4-15 | TechDocWriter | 技术文档 | 文档编写 |
| 5-1 | ArtStyleDefiner | 美术风格 | 视觉方向确定 |
| 5-2 | CharacterArtist | 角色美术 | 角色形象设计 |
| 5-3 | EnvironmentArtist | 场景美术 | 场景设计 |
| 5-4 | UIArtist | UI美术 | 界面视觉设计 |
| 5-5 | VFXArtist | 特效美术 | 特效制作 |
| 5-6 | Animator | 动画师 | 动画制作 |
| 5-7 | ConceptArtist | 概念美术 | 概念图设计 |
| 5-8 | UIUXDesigner | 交互设计师 | 用户体验设计 |
| 5-9 | Colorist | 色彩设计师 | 配色方案 |
| 5-10 | AssetManager | 资产管理 | 美术资产管理 |
| 6-1 | Composer | 作曲家 | 游戏音乐创作 |
| 6-2 | SoundDesigner | 音效设计师 | 音效制作 |
| 6-3 | VoiceDirector | 配音导演 | 配音指导 |
| 6-4 | AudioImplementer | 音频实现 | 音频集成 |
| 6-5 | MixingEngineer | 混音工程师 | 音频混音 |
| 7-1 | CommunityManager | 社区运营 | 玩家社区维护 |
| 7-2 | DataAnalyst | 数据分析师 | 运营数据分析 |
| 7-3 | QAEngineer | 测试工程师 | 质量测试 |
| 7-4 | DevOpsLead | 运维主管 | 上线运维 |

---

## 使用技巧

**1. 描述越具体，输出越精准**
- ❌ "帮我设计一个关卡"
- ✅ "帮我设计一个3星难度的Obby关卡，主题是火山，包含5个障碍物和2个检查点"

**2. 把上一步输出作为下一步输入**
Agent之间可以流水线工作，把前一个Agent的结果直接粘贴给下一个。

**3. 要求特定格式**
可以要求 Agent 用 JSON、表格或特定模板输出，方便直接导入项目。

**4. 多轮迭代**
第一次生成后可以继续追问："调整第3关的难度"、"增加一个隐藏关卡"。

---

## 文件目录

```
AGENTS/           # 所有 Agent 的 System Prompt 定义
WORKFLOWS/        # 多 Agent 协作流程模板
USECASES/         # 实际使用案例
```
