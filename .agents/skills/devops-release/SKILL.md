---
name: devops-release
description: >
  量潮 DevOps 发布工作流。使用 qtcloud-devops release 命令完成发布，
  并人工校验 CHANGELOG 和 Release 文本质量。
---

# DevOps 发布工作流

## 流程

### Step 1: 检查发布状态

```bash
qtcloud-devops release status
```

检查各 scope 的发布状态：GitHub Release 是否存在、body 是否同步、版本号是否对齐。

### Step 2: 发布

```bash
qtcloud-devops release publish --version <VERSION> --yes
```

自动更新版本号 → CHANGELOG → tag → GitHub Release。

### Step 3: 检查发布后状态

```bash
qtcloud-devops release status
```

确认发布后的状态正确。

### Step 4: 校验文本质量

LLM 生成的 CHANGELOG 和 Release body 可能不稳定。打开以下文件人工检查：

- `CHANGELOG.md` — 检查条目是否准确、格式是否规范、有无多余或缺失内容
- GitHub Release 页面 — 查看 body 是否与 CHANGELOG 一致

如发现问题，手动修复后执行：

```bash
qtcloud-devops release status
```

确认修复后的状态。
