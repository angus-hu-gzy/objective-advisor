# ROADMAP

记录「代码之外」的运维收尾与后续迭代方向。与本仓库的 Skill 行为规则无关，不影响功能。

## 一、仓库设置（需在 GitHub 网页操作）

- [ ] **Description**：`让 AI 当顾问而不是应声虫：不迎合、先澄清再动手、区分已核实与未核实事实。An objective advisor Skill for DeepSeek Harness.`
- [ ] **Topics**：`deepseek-harness`、`agent-skills`、`skill`、`prompt-engineering`、`ai-agents`
- [ ] **License 识别**：Settings 页确认 License 显示为 MIT
- [ ] **邮箱归属**：确认 `3292801541@qq.com` 已在 GitHub Settings → Emails 验证，提交才能关联到账号并计入贡献图

## 二、已知待改进

- [ ] `TESTS.md` 的 14 条用例尚未实际跑过，仅 T1、T2 有明确验证记录，其余等待首轮回归
- [ ] 无 `.github/ISSUE_TEMPLATE`，反馈格式目前写在 README 里；若出现真实外部反馈再补模板
- [ ] 无 `CONTRIBUTING.md`，同上，等确有协作需求再加
- [ ] 未提供英文 README；`SKILL.md` 的 `description` 已用英文以保证跨客户端触发，正文为中文

## 三、迭代原则

改动 `SKILL.md` 前请先读 [TESTS.md](TESTS.md)：

1. 只增加有**真实失败案例**支撑的规则，不为显得完整而堆条款
2. 新增规则必须同步补一条测试用例，否则下次无法回归
3. 保留以下已验证行为的语义，不得因为缩写而丢失：
   - 需求模糊时先问，不擅自创建文件
   - 需求明确时直接执行，不反复追问
   - 不迎合，也不为了反对而反对
   - 默认简短，复杂问题分步展开
   - 不知道时不编造，关键事实区分是否已核实

## 四、不在计划内

以下方向经过评估后**明确不做**，避免 Skill 膨胀：

- 置信度 1–5 评分、正反双栏等强制输出格式（与「默认简短」冲突）
- 拆分 `references/` 或 `scripts/`（当前正文 76 行，远低于 500 行阈值，拆分只增加加载复杂度）
- 增加检索、文件操作等工具能力（本 Skill 只约束判断与表达，不承担执行）
