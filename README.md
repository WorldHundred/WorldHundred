<!-- ======================= BANNER ======================= -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:2F54EB,100:8DA2FF&height=200&section=header&text=Cheng%20Qiu&fontColor=ffffff&fontSize=52&fontAlignY=36&desc=AI%20Agent%20Developer%20%C2%B7%20ReAct%20%2F%20MCP%20%2F%20On-Device%20LLM&descSize=18&descAlignY=58&animation=fadeIn" alt="banner"/>

<!-- ======================= TYPING ======================= -->
<p align="center">
  <a href="https://worldhundred.github.io/">
    <img src="https://readme-typing-svg.demolab.com?font=Nunito&weight=600&size=24&pause=1800&color=2F54EB&center=true&vCenter=true&width=620&lines=AI%20Agent%20%E5%BC%80%E5%8F%91%20%C2%B7%20%E6%89%8B%E5%86%99%20ReAct%20%E5%86%85%E6%A0%B8%20%F0%9F%91%8B;%E4%B8%8D%E4%BE%9D%E8%B5%96%E6%A1%86%E6%9E%B6%EF%BC%8C%E6%8A%8A%E6%A8%A1%E5%9E%8B%E7%9A%84%E6%AF%8F%E4%B8%80%E6%AD%A5%E6%91%8A%E5%BC%80%E6%9D%A5%E7%9C%8B;Building%20agents%20with%20evidence%2C%20not%20vibes" alt="typing"/>
  </a>
</p>

<!-- ======================= QUICK BADGES ======================= -->
<p align="center">
  <a href="https://worldhundred.github.io/"><b>🌐 个人主页 / Portfolio → worldhundred.github.io</b></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Computer%20Science-NJUST%20Taizhou-2F54EB?style=for-the-badge&logo=googlescholar&logoColor=white" alt="njust-tz"/>
  <a href="https://worldhundred.github.io">
    <img src="https://img.shields.io/badge/Website-worldhundred.github.io-2F54EB?style=for-the-badge&logo=googlechrome&logoColor=white" alt="website"/>
  </a>
  <a href="mailto:2668648461@qq.com">
    <img src="https://img.shields.io/badge/Email-2668648461%40qq.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="email"/>
  </a>
  <a href="https://github.com/WorldHundred">
    <img src="https://img.shields.io/badge/GitHub-WorldHundred-101828?style=for-the-badge&logo=github&logoColor=white" alt="github"/>
  </a>
</p>

---

## 👋 About me

嗨，我是 **邱程 (Cheng Qiu)**，南京理工大学泰州科技学院计算机科学与技术本科在读（2025 – 2029）👋

主攻 **AI Agent、LLM 应用与端侧推理**。不依赖 LangChain / OpenAI SDK，用标准库手写了一个约 **550 行的 ReAct 内核** —— 9 个工具、stdio MCP Server、能在 llama.cpp 上完全离线跑，并配了一套 **29 题的确定性评测**，用同一组任务对比云端模型与本地 4B 模型的成功率、延迟和成本。也做过跨境购物多 Agent 系统的二次开发与召回评测。

比起"把模型接进产品"，我更在意 **工具怎么约束、失败怎么归因、评测结果到底可不可信**。在校期间专业排名前 10%，获校一等奖学金与全国大学生数学建模竞赛（A 题）省级奖项。

🔎 正在寻找 **AI Agent 开发实习**（杭州 / 南京 / 上海）

🌐 个人主页：**[worldhundred.github.io](https://worldhundred.github.io)**

<!-- ======================= TECH STACK ======================= -->
## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,fastapi,redis,mysql,vue,ts,js,nodejs,git,github,linux,bash,vscode,markdown&perline=7" alt="stack"/>
</p>

---

<!-- ======================= SPOTLIGHT ======================= -->
## 🌟 Spotlight — personal-research-agent

<table>
  <tr>
    <td width="200" align="center" valign="middle">
      <a href="https://github.com/WorldHundred/personal-research-agent">
        <img src="https://github.com/WorldHundred/personal-research-agent/blob/main/docs/images/ui.png?raw=true" width="170" alt="运行界面"/>
      </a>
    </td>
    <td valign="middle">
      <h3>手写 ReAct 内核的个人研究助理</h3>
      <p><b>A ReAct agent written from scratch — no LangChain, no OpenAI SDK.</b><br/>
      标准库直连 Chat Completions · 约 550 行内核 · 仅 3 个第三方依赖 · 9 个工具 · 多轮记忆（2026.09 – 2026.10）。</p>
      <p>
        <img src="https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square&logo=python&logoColor=white" alt="python"/>
        <img src="https://img.shields.io/badge/ReAct-Hand--written-2F54EB?style=flat-square" alt="react"/>
        <img src="https://img.shields.io/badge/MCP-stdio%20server-5EEAD4?style=flat-square" alt="mcp"/>
        <img src="https://img.shields.io/badge/llama.cpp-offline-101828?style=flat-square" alt="llamacpp"/>
      </p>
    </td>
  </tr>
</table>

**它做了什么？**

- 🧠 **手写 ReAct 内核** — 用 `urllib` 直连 `/chat/completions`，原始 JSON、返回的 `tool_calls`、上下文如何拼接全部可见，不藏在框架后面。
- 🧩 **工具即对象** — `JSON Schema + 函数实现 + 注册表`绑成同一个 `Tool`，从结构上杜绝声明与实现脱节；同一套 Schema 以 stdio MCP 暴露给 Claude Code，逐字段一致。
- 💻 **端侧离线** — 只改 `LLM_BASE_URL` 就能切到 llama.cpp。Qwen3-4B + Q4_K_M 占 3.6GB 显存，约 95 tok/s，完全离线。
- 📊 **可复现评测** — 29 题 10 类，网络与文件工具全用固定桩。云端 100% / 本地 86.2%，4 次失败全部归因到工具纪律，而不是答错。
- 🛡️ **有边界的运行时** — 137 个离线测试；步数上限 + 重复调用检测双层防死循环；AST 白名单替代 `eval`；笔记目录穿越拦截。

<p align="center">
  <a href="https://github.com/WorldHundred/personal-research-agent"><b>📄 完整 README 与评测报告</b></a>
</p>

---

<!-- ======================= ALSO BUILDING ======================= -->
## 🔭 Also building

- **[banxuemiao](https://github.com/WorldHundred/banxuemiao)** — 本地优先 + 云端备份的游戏化学习打卡 App：7 个页面、5 个 tab，跨零点自动归档，登录后 5 秒防抖全量备份；uniCloud 三块云函数 + token 鉴权；Canvas 2D 手绘统计图。`uni-app` `Vue3` `uniCloud`
- **Globex 跨境购物多 Agent** — 课程基线工程的二次开发（不公开）：把 POSIX 的 `fcntl` 锁换成 `msvcrt` fallback 让它在 Windows 上跑通，并行派发实测端到端 752.0s → 326.8s，67 条标注 query 的召回评测 Recall@8 达 0.909。`AgentScope 2.0` `Qdrant` `LangFuse`

---

<!-- ======================= STATS（仓库养起来后再解除注释） =======================

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=WorldHundred&theme=default" alt="profile-details"/>
</p>
<p align="center">
  <img height="165" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=WorldHundred&theme=default" alt="stats"/>
  <img height="165" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=WorldHundred&theme=default" alt="top-langs"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=WorldHundred&hide_border=true&ring=2F54EB&fire=2F54EB&currStreakLabel=2F54EB" alt="streak"/>
</p>

===================================================================== -->

---

<p align="center"><sub>📫 <b>2668648461@qq.com</b> · 欢迎来聊 Agent</sub></p>

<!-- ======================= FOOTER ======================= -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:8DA2FF,100:2F54EB&height=120&section=footer" alt="footer"/>
