# 执行提示词：PortraitRpDemo 工作区 OpenClaw 试点改造

## 当前工作区路径
1. 工作区根目录：`D:\code\AI\J-Agents\PortraitRpDemo`
2. 需求文档目录：`D:\code\AI\J-Agents\PortraitRpDemo\docs\openclaw\workspace-openclaw-governance`
3. 本轮所有新增、修改、验证都只能发生在上述 `PortraitRpDemo` 工作区根目录内。

请按照以下文件执行当前 `PortraitRpDemo` 工作区整改，不要扩散到其他目录：

1. `D:\code\AI\J-Agents\PortraitRpDemo\docs\openclaw\workspace-openclaw-governance\需求概述.md`
2. `D:\code\AI\J-Agents\PortraitRpDemo\docs\openclaw\workspace-openclaw-governance\需求详情-PortraitRpDemo工作区OpenClaw试点改造.md`

## 本轮目标
1. 以最小改动补齐 OpenClaw 风格 `.codex/` 记忆层。
2. 保持 demo 工作区的轻量性和现有发布判定语义。

## 必做事项
1. 创建：
   - `.codex/SOUL.md`
   - `.codex/USER.md`
   - `.codex/MEMORY.md`
   - `.codex/TOOLS.md`
   - `.codex/HEARTBEAT.md`
   - `.codex/memory/`
2. 更新 `AGENTS.md`，补齐 OpenClaw 风格读取顺序。
3. 保留现有 `release_valid.txt`、`release_invalid.txt` 的职责不变。

## 禁止事项
1. 不要把 demo 工作区复杂化到超出当前需要。
2. 不要修改其他工作区。

## 交付物
1. 改造后的目录清单。
2. `AGENTS.md` 更新说明。
3. 启动读取与记忆写入验证证据。
