# 周末休整记录 + Codex 桌面版排错

> **日期**：2026-04-27 (Mon · 上班午休写)  
> **场景**：周末三天没学习的复盘 + 公司试 Codex 黑屏
> **主题**：休息节奏、AI 工具尝试、网络排查

---

## 周末做了什么（真实记录）

04-24（五）~ 04-26（日）三天没学 UE。但**不是单纯打游戏**：

| 项 | 估时 | 价值 |
|----|------|------|
| 玩游戏（Steam 有记录） | **11h** | 放松 |
| 躺着 | 大头 | 身体回血 |
| 健身 | 一次 | 长期收益 |
| 吃自助 | 一顿 | 生活仪式感 |
| 晚上看 GPT-5.5 发布 | 几小时 | 求知欲，**不算浪费** |
| 试 GPT Image-2 | 已单独归档 | 见 [`2026-04-23-gpt-img2-observations.md`](./2026-04-23-gpt-img2-observations.md) |

**自己的判断**：22h/周 是个**长期均值**，不是每天必须有产出。这周**重新从 04-27 开始**就行，不愧疚。

---

## 试 Codex 桌面版翻车记

### 现象
- 家里：装好、登录成功、能用
- 中间动作：**重置了网络**（具体哪个 reset 命令记不清）
- 公司：打开 → **持续黑屏** → 一个 `>_` 小图标在中间，没任何输入框

### AI 帮我分析的 3 个可能原因（按概率）

1. **"重置网络"清掉了家里代理配置**——Codex 走系统代理才能上 OpenAI，重置后断网了
2. **公司网络封 `api.openai.com`**——大多数国内公司网络默认这样
3. **Codex 自己的 UX 烂**：连不上 API 时既不报错也不超时，**直接黑屏装死**

### 我学到的排查命令（下次直接套）

```cmd
nslookup api.openai.com         :: 1. DNS 通不通
curl -v --max-time 5 https://api.openai.com   :: 2. 网络通不通
netsh winhttp show proxy        :: 3. 看系统代理
echo %HTTPS_PROXY%              :: 4. 看环境变量
```

| 卡在哪 | 真相 | 解决 |
|--------|------|------|
| 1 不通 | DNS 污染 | 换 1.1.1.1 / 8.8.8.8 |
| 1 通 2 不通 | IP 被墙 | 开代理 |
| 1+2 通还黑屏 | App bug | 重装、清用户数据 |
| 公司网络 | 大概率封了 OpenAI | 无解，认命 |

### 核心结论

**Codex 桌面版没有离线模式 / 没有错误提示**——连不上 OpenAI 服务器就是黑屏。这不是 bug，是它的设计。

---

## 当天真实测出来的结果（追加 · 2026-04-27 中午）

跑了那 4 条排查命令，结果：

```
nslookup api.openai.com  →  198.18.0.57
curl ... api.openai.com  →  HTTP/1.1 421, Server: cloudflare, CF-RAY: ...-ICN
netsh winhttp show proxy →  直接访问(没有代理)
echo %HTTPS_PROXY%       →  未设置
```

### 我学到的两个新知识点

1. **`198.18.x.x` 是 fake-ip 的特征**  
   这是 RFC2544 保留地址段，专门给 TUN 模式 / Clash 虚拟网卡用。看到这个 IP 段不要慌——说明代理在劫持 DNS，是正常的。

2. **`CF-RAY: ...-ICN` 说明流量走到了韩国仁川节点**  
   再加上 `Server: cloudflare` → 我的流量真的穿透到了 OpenAI 的 CDN，**网络这一关是通的**。

3. **网络通了 Codex 还是黑屏 = UWP 沙箱坑**  
   Microsoft Store 装的应用是 UWP/AppContainer，**走独立的网络栈，TUN 模式不一定能劫持它**。这是 Windows 一个深坑，未来做 Steam 商店分发游戏时也可能遇到。

### 真要修的话（没修，记一下）

```cmd
CheckNetIsolation LoopbackExempt -a -n="OpenAI.Codex_xxx"
```

但要先找到 Package Family Name，麻烦，**没修，直接放弃**。

### 最终决定

**卸载 Codex 桌面版**。理由：
1. 网络通了应用还黑屏 → 是 Store 版沙箱问题，修起来 ROI 极低
2. Cursor 已经支持切 GPT-5.5，**能力一样体验得到**
3. 真要测 Codex，[chatgpt.com/codex](https://chatgpt.com/codex) Web 版浏览器开就行

### 给未来自己加一条规则

> 装 Store / UWP 应用，**优先走非 Store 版**（官网下载的 .exe / .msi）。
> Store 版的沙箱机制对国内代理用户不友好。

---

## 反思：要不要继续折腾 Codex？

**不要**。理由：

1. 我已经在用 Cursor（订阅、好用、对话历史本仓库就是证据）
2. Cursor 已经支持切到 GPT-5.5 模型，**能力一样能体验**
3. OpenAI 桌面版在国内 = 三重墙（账号 / 订阅 / 网络），ROI 太低
4. 真要看新模型，**用 Web 版（chatgpt.com/codex）测一下就够**，不用纠结桌面客户端

**给未来自己的提醒**：
> 装一个新工具折腾超过 30 分钟，立刻问自己——"这件事如果不解决，会影响我的 UE 学习吗？" 答案是 No 的话，立刻关掉去学习。

---

## 关联到 UE5 学习

这次折腾的真正价值在**网络排查这套命令**——以后做 UE 项目联机部分（第 7 个月）时，调试 Replication / Dedicated Server 一样要用 `nslookup` / `curl` / `netsh`。**今天浪费的时间，未来项目里能省回来一点点**。
