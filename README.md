# 🛡️ Prompt Injection Tester

> **在线检测你的 AI Agent 是否易受 Prompt Injection 攻击**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Live Demo](https://img.shields.io/badge/Live-Demo-success)](https://kaising-openclaw1.github.io/prompt-injection-tester/)

## 🚀 在线使用

👉 **[立即测试 →](https://kaising-openclaw1.github.io/prompt-injection-tester/)**

## ✨ 特性

- 🔍 **20+ 注入模式检测** — 覆盖角色劫持、提示词泄露、越狱攻击、编码混淆、社交工程等
- 🔒 **纯前端实现** — 数据不离开浏览器，零隐私风险
- ⚡ **实时检测** — 输入即检测，无需后端 API
- 📊 **可视化报告** — 严重程度分级、匹配位置、安全评分
- 🎯 **生产可用** — 检测规则参考 OWASP LLM Top 10 2026
- 📱 **响应式** — 桌面端、平板、手机全支持

## 🔬 检测能力

| 类别 | 检测项 |
|------|--------|
| **角色注入** | 角色劫持、DAN/越狱模式 |
| **信息泄露** | 系统提示词泄露、指令外泄 |
| **越狱绕过** | 假设场景、角色扮演、翻译绕过 |
| **指令劫持** | 指令覆盖、优先级劫持 |
| **恶意命令** | 代码执行、数据访问 |
| **社交工程** | 紧急/权威施压、情感操控 |
| **编码混淆** | Base64 编码、Leet 语 |
| **内容安全** | 负面内容生成、虚假信息 |
| **间接注入** | 上下文污染、未来指令预设、Token 消耗 |

## 📖 使用场景

1. **AI Agent 开发者** — 上线前自查输入是否包含已知攻击向量
2. **安全审计** — 快速评估第三方 LLM 集成的暴露面
3. **教育/培训** — 演示 Prompt Injection 攻击形态
4. **红队测试** — 配合 Fuzzing 工具进行批量检测

## 🤔 为什么需要 Prompt Injection 检测？

- **OWASP 2026** 将 Prompt Injection 列为 LLM Top 1 风险
- **Gravitee 2026 报告**：仅 14.4% 的 AI Agent 通过安全审批
- **2026 Q1 数据**：AI Agent 安全事件同比 +340%

## 🛠️ 部署到自己的域名

```bash
# 1. 克隆仓库
git clone https://github.com/kaising-openclaw1/prompt-injection-tester.git

# 2. 单文件部署（不需要构建）
# 直接把 index.html 上传到任何静态服务器：Vercel/Netlify/GitHub Pages/Cloudflare Pages

# 3. 集成到现有项目
# 复制 index.html 中的 JavaScript 检测引擎，独立使用
```

## 🎯 局限性

⚠️ **本工具是基于模式的检测器，不能替代多层防护：**

- ✅ 可检测：已知的、显性的攻击模式
- ❌ 不能检测：高度上下文化的语义攻击、新型 0-day 攻击向量

**推荐的完整防护体系：**
1. 输入过滤（本工具的能力）
2. 语义检测（需要 LLM 二级判断）
3. 沙箱隔离（工具执行权限最小化）
4. 输出审计（结果再次过滤）
5. 监控告警（异常行为实时通知）

## 💼 需要专业方案？

如果你需要更深度的 AI Agent 安全方案，包括：
- 自定义检测规则集
- 语义级深度检测（LLM-as-Judge）
- 沙箱化工具执行环境
- 完整的安全审计报告

👉 [查看完整服务方案](https://kaising-openclaw1.github.io/portfolio/)

## 📄 License

MIT License - 自由使用、修改、分发。

## 🤝 贡献

欢迎提交新的注入模式！Pull Request 请遵循：
1. 在 `PATTERNS` 数组中添加新规则
2. 提供至少 3 个真实样本作为测试
3. 说明该模式的攻击场景

---

**作者**：kaising-openclaw1
**相关项目**：[Prompt Injection Guard](https://github.com/kaising-openclaw1/prompt-injection-guard)（生产环境 Python SDK）
