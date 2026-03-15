# 需求详情：PortraitRpDemo 工作区 OpenClaw 试点改造

## 1. 主题目标与价值说明
为 `PortraitRpDemo` 以最小改动补齐 OpenClaw 风格 `.codex/` 记忆层，同时保持其演示型工作区的轻量特征。

## 2. 用户画像与使用场景
1. 用户画像：演示 agent、owner、执行维护者。
2. 使用场景：
   - 启动时恢复身份、用户、近期记忆；
   - 保持发布判定职责边界不变。

## 3. 用户旅程或关键流程
1. 新增 `.codex/`。
2. 更新 `AGENTS.md`。

## 4. 功能需求清单
### FR-PRD-01 新增 `.codex/`
1. 新增：
   - `.codex/SOUL.md`
   - `.codex/USER.md`
   - `.codex/MEMORY.md`
   - `.codex/TOOLS.md`
   - `.codex/HEARTBEAT.md`
   - `.codex/memory/`

### FR-PRD-02 更新读取顺序
1. `AGENTS.md` 增加：
   - `.codex/SOUL.md`
   - `.codex/USER.md`
   - 近两天 `.codex/memory/*.md`
   - 主会话 `.codex/MEMORY.md`

### FR-PRD-03 保留 demo 边界
1. 不削弱“发布格式校验”和“预发布判定”的现有职责。

## 5. 非功能需求
1. 保持轻量。
2. 不引入无关目录。

## 6. 验收标准
1. Given 已完成改造
2. When 检查 `../PortraitRpDemo/.codex/`
3. Then 核心文档与 `memory/` 已存在
4. And `AGENTS.md` 已具备 OpenClaw 风格读取顺序

## 7. 边界条件与异常处理
1. 若当前不需要本地技能，不强制新增 `.codex/skills/`。

## 8. 依赖项与开放问题
1. 依赖执行方按最小模板补齐。
2. 开放问题：是否后续补专用 `TOOLS.md` 内容；本轮不强制。
