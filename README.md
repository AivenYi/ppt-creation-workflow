# 🏭 PPT Creation Workflow Skill

> AI PPT 智能创建工作流（双阶段流水线）— 不直接生成 PPT，而是生成两套专业化提示词，让最合适的工具干最合适的活。

[![Version](https://img.shields.io/badge/version-2.1.0-blue)](https://github.com/wayen-ai/ppt-creation-workflow)
[![Platform](https://img.shields.io/badge/platform-WorkBuddy-orange)](https://www.codebuddy.cn/)
[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)

---

## 📌 这是什么？

一个 WorkBuddy Skill，帮你把模糊的 PPT 想法变成 50 页完整大纲，再生成两套专业提示词：
- **第一套** → 发给 Gemini（或 DeepSeek / Claude）生成详细内容
- **第二套** → 发给豆包 DOCPPTA 生成最终 PPT

### 流程一图看清

```
你说需求 → 我提问 → 出大纲 → 出Gemini提示词 → 你发给Gemini
→ Gemini输出内容 → 你发回给我 → 我出豆包提示词 → 你发给豆包 → 🎉 PPT完成！
```

---

## 🚀 快速开始

### 安装

1. 在 WorkBuddy 中安装本 skill
2. 不需要任何额外配置

### 使用

直接说：**"帮我做一个关于 XXX 的 PPT"**

我会依次问你：主题 / 用途 / 受众 / 时长 / 风格 / 内容偏好 → 然后生成完整材料。

---

## 📋 前置条件

| 你需要 | 说明 |
|--------|------|
| WorkBuddy | 运行 skill 的平台 |
| Gemini（或其他 LLM）| 用于生成 PPT 详细文字内容 |
| 豆包 DOCPPTA | 用于将内容渲染成 PPT |
| （可选）VPN/代理 | 仅访问 Gemini 时需要，skill 本身不需要 |

> ⚠️ 本 skill 本身**不发起任何网络请求**，不受代理/VPN 环境影响。

---

## 📁 文件结构

```
ppt-creation-workflow/
├── SKILL.md          # Skill 核心定义（WorkBuddy 读取此文件）
├── README.md         # 本文件
└── LICENSE           # MIT 开源协议
```

---

## 🔧 技术特性

- **零网络依赖**：skill 本身不联网，只在本地生成提示词文本
- **代理安全**：不受 HTTP_PROXY / HTTPS_PROXY 环境变量影响
- **跨平台**：纯文本工作流，Windows/macOS/Linux 均可使用
- **LLM 无关**：生成的提示词可发给任何大语言模型（Gemini / DeepSeek / Claude / ChatGPT / Kimi 等）

---

## 📦 发布渠道

| 平台 | 链接 |
|------|------|
| ClawHub | [wayen/ppt-creation-workflow](https://clawhub.ai/wayen/ppt-creation-workflow) |
| SkillHub | [skills.aiproducthub.cn](https://skills.aiproducthub.cn/) |
| GitHub | [wayen-ai/ppt-creation-workflow](https://github.com/wayen-ai/ppt-creation-workflow) |

---

## 👤 作者

**Wayen（易海）**

- 📧 邮箱：2904447373@qq.com
- 🎓 江西软件职业技术大学 B230708 班

---

## 📄 许可

MIT License — 详见 [LICENSE](./LICENSE) 文件。

---

## 🔄 版本历史

| 版本 | 日期 | 变更 |
|------|------|------|
| v2.1.0 | 2026-05-27 | 新增前置条件说明、代理/VPN 兼容说明、备选方案、troubleshooting |
| v2.0.0 | 2026-05-26 | 重构为双阶段流水线，新增内容追问强制环节 |
| v1.1.0 | 2026-05-25 | 改为自由输入（取代固定选项） |
| v1.0.0 | 2026-05-24 | 初始版本 |
