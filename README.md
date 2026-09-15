# Web Security Skills · 猎洞十二技

> 一套自研的 Web 安全测试方法论技能库：以「五步猎洞法」（识面 → 定点 → 验证 → 利用 → 收官）为统一骨架，覆盖 12 类核心 Web 漏洞的完整实战流程。可作 AI Agent 技能使用，也可作工程师的案头手册。

## 设计理念

传统漏洞手册是"知识点罗列"——查得到，用不顺。这套手册按**实战者的决策流**组织：

1. **何时启用** —— 先判断这是什么场景，再翻武器库
2. **原理拆解** —— 一句话讲透病根，拒绝背诵式理解
3. **五步猎洞法** —— 每类漏洞同样的五步节奏，形成可复用的肌肉记忆
4. **实战推演** —— 虚构但完整的全流程案例（虚构域名，可安全复现思路）
5. **对抗与绕过** —— 防线与破法的对照表
6. **防御视角** —— 站在蓝队给修复清单，测试报告直接引用
7. **踩坑记录 + 速查卡** —— 假阴性教训与临场速查

## 技能清单

| # | 技能 | 一句话 |
|---|------|--------|
| 1 | [SQL 注入](skills/01-sql-injection/) | 让数据库自己开口说话 |
| 2 | [XSS](skills/02-xss/) | 站在用户浏览器里的一行代码 |
| 3 | [SSRF](skills/03-ssrf/) | 借服务器的手，摸服务器的家 |
| 4 | [XXE](skills/04-xxe/) | 藏在 DOCTYPE 里的搬运工 |
| 5 | [CSRF](skills/05-csrf/) | 让用户的浏览器替你扣扳机 |
| 6 | [访问控制失效](skills/06-broken-access-control/) | 系统记得你是谁，却不检查你要谁的 |
| 7 | [反序列化](skills/07-insecure-deserialization/) | 递给服务器一个"自己会动的对象" |
| 8 | [SSTI](skills/08-ssti/) | 模板引擎听懂了你的话 |
| 9 | [文件上传](skills/09-file-upload/) | 一张图片的三十六种身份 |
| 10 | [WAF 绕过](skills/10-waf-evasion/) | 和规则引擎玩"你画我猜" |
| 11 | [JWT 攻击](skills/11-jwt-attacks/) | 三段点号里的信任游戏 |
| 12 | [业务逻辑](skills/12-business-logic/) | 漏洞列表之外的漏洞 |

## 使用方法

### 作为 AI Agent 技能

```bash
git clone https://github.com/<你的用户名>/web-security-skills.git
cp -r web-security-skills/skills/* ~/.claude/skills/   # 按你的 Agent 技能路径调整
```

之后对 AI 助手说：

> "帮我测试这个接口有没有 SQL 注入"

Agent 将按「五步猎洞法」的结构化流程推进测试。

### 作为人工手册

每个 `skills/<name>/SKILL.md` 均为独立文档，直接阅读。`速查卡` 一节适合临场快速回忆。

## 目录结构

```
web-security-skills/
├── README.md
├── LICENSE
└── skills/
    ├── 01-sql-injection/SKILL.md
    ├── 02-xss/SKILL.md
    ├── ...（共 12 个，每个一技）
    └── 12-business-logic/SKILL.md
```

## ⚠️ 免责声明

本项目仅用于**已获得书面授权的安全测试与学习研究**。使用者必须：

1. 仅在授权范围内测试，遵守《网络安全法》《刑法》第 285/286 条等法律法规
2. 文中所有案例均为虚构演示（`*.demo-example.com` 为示例域名）
3. 自行承担滥用产生的一切法律责任

未经授权对他人系统进行测试属于违法行为。
