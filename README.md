# Jay0130-a

AI Agent 方向开发者，关注 **Agent Runtime / Tool Calling / Skills / Eval**，以及跨平台（Windows）工程问题：路径、编码、shell 差异这类真实环境里才会暴露的坑。

---

## 已合并的开源贡献

以下 9 个 PR 已合入对应项目的 `main` / `develop`：

| 项目 | PR | 内容 |
| --- | --- | --- |
| Tencent/teamai-cli | [#1034](https://github.com/Tencent/teamai-cli/pull/1034) | dsh 在 Windows 生成的 hook 命令改为 PowerShell 语法（修复 #1005：原先每条 hook 都 ParserError 且被静默吞掉） |
| Tencent/teamai-cli | [#1046](https://github.com/Tencent/teamai-cli/pull/1046) | `~` 统一经 `getUserHome()` 解析，消除 Git Bash / PowerShell 下的 home 不一致 |
| Tencent/teamai-cli | [#1058](https://github.com/Tencent/teamai-cli/pull/1058) | 新增 `teamai review`：对 `push` 出的分支做只读健康检查（结构 / 命名 / 重复 / 格式 / 泄漏） |
| Tencent/teamai-cli | [#870](https://github.com/Tencent/teamai-cli/pull/870) | 原生 Windows 下把临时根目录解析为长路径，修掉短路径导致的测试失败 |
| Tencent/WeKnora | [#4374](https://github.com/Tencent/WeKnora/pull/4374) | 拒绝旧版二进制 `.xls`，给出可操作的报错而不是让模型读到一个空表 |
| Tencent/WeKnora | [#4425](https://github.com/Tencent/WeKnora/pull/4425) | Helm 中 data-files claim 的访问模式改为可配置 |
| Tencent/WeKnora | [#4020](https://github.com/Tencent/WeKnora/pull/4020) | docreader 文本切分工具的单测 |
| QwenLM/qwen-code | [#13960](https://github.com/QwenLM/qwen-code/pull/13960) | 桌面版发布说明锚定到上一个桌面版本 |
| TencentCloud/octop-harness | [#63](https://github.com/TencentCloud/octop-harness/pull/63) | 子进程输出按 UTF-8 解码，不再依赖宿主 locale |

## 评审中的贡献

| 项目 | PR | 内容 |
| --- | --- | --- |
| QwenLM/qwen-code | [#14349](https://github.com/QwenLM/qwen-code/pull/14349) | `/auth` 文案改为渲染期解析，修掉运行期切换语言后菜单中英混排 |
| QwenLM/qwen-code | [#13962](https://github.com/QwenLM/qwen-code/pull/13962) | ripgrep 回退提示收敛为一行可操作文案，原始探测输出不再进横幅 |
| QwenLM/qwen-code | [#13932](https://github.com/QwenLM/qwen-code/pull/13932) | 索引行标题按 150 字符预算分配，修掉标题超预算时的 hook 丢失 |
| bytedance/deer-flow | [#6984](https://github.com/bytedance/deer-flow/pull/6984) | `SKILL.md` 的 BOM 不再进入模型上下文与指纹 |
| bytedance/deer-flow | [#6982](https://github.com/bytedance/deer-flow/pull/6982) | 补齐 skillscan 已声明假阴性（解构绑定）的回归固定 |
| TencentCloud/Octop | [#2030](https://github.com/TencentCloud/Octop/pull/2030) | Kimi 探测模型改为可配置，并在模型退役时给出可读报错 |

## 技术方向

- **Agent Runtime**：中间件链、取消与重连、流式事件协议
- **Skills / Tool Calling**：`SKILL.md` 契约、allowed-tools 策略、MCP 参数映射
- **Eval / Harness**：配置生效校验、请求态 vs 生效态、回归固定
- **跨平台工程**：Windows / PowerShell / 路径与编码差异

## 项目

- [Auto2offer](https://github.com/Jay0130-a/Auto2offer) — 面向个人求职者的 AI 招聘沟通协同智能体：发现岗位 → 匹配评估 → 生成招呼 → 安全校验 → 人工审批 → 发送 → 会话应答

---

<sub>PR 记录会持续更新。</sub>
