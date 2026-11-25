# 小狄氧舱账号维护智能机器人 Skill（v2.1 开源版）

专为 **狄耐克（DNAKE，股票代码：300884）** 线下微压富氧舱经销商打造的 AI 短视频账号维护与运营外脑。
支持在 **WorkBuddy** 中 `@小狄氧舱账号维护智能机器人` 一键调用，自动抓取本周本地及全国康养热点，结合狄耐克产品库与去AI味引擎，直接输出**排版精美的独立 HTML 拍摄脚本包**（支持手机提词、一键打印或导出PDF）。

---

## 一、 核心升级特性（v2.1）
1. **强制精美 HTML 交付**：告别杂乱纯文本，每次生成均为高颜值单文件 HTML（含热点雷达看板 + 10条大字号提词卡片 + 一键打印按钮）。
2. **实时同城+全国热点雷达**：动态联网检索门店所在城市近7天天气、赛事、民生热点与全国康养热榜。
3. **内置去AI味引擎 & 合规红线**：自动清除大模型套话，转换为门店老板大白话口吻，严防医疗违禁词限流。
4. **官方产品知识库解耦**：完整收录 GYCHA 合金碳钢系列与 GYCHC 碳纤维系列参数、报价、24V安全低压/水冷/UPS核心卖点与全国真实案例。

---

## 二、 仓库目录结构
```text
xiaodi-account-maintenance-bot/
├── README.md                                  # 项目说明、设计原理与使用规则
├── SKILL.md                                   # WorkBuddy / Agent 核心技能入口
├── references/
│   ├── xiaodi_bot_product_kb.md               # 狄耐克官方产品参数、报价与全国案例库
│   ├── xiaodi_bot_anti_ai_rules.md            # 去AI味文案法则与平台合规词库
│   ├── xiaodi_bot_script_templates.md         # 5大零基础极简拍摄模板
│   └── xiaodi_bot_html_template.html          # 经销商交付专用精美HTML模板
└── scripts/
    └── xiaodi_bot_hot_topic_prompt.md         # 全国及同城康养热点实时抓取指令
```

---

## 三、 经销商使用规则（WorkBuddy）
在 WorkBuddy 对话框中输入：
> `@小狄氧舱账号维护智能机器人` + `城市/店名` + `店内氧舱型号` + `本周热点+本周脚本`

**示例**：
- `@小狄氧舱账号维护智能机器人 厦门旗舰店 + GYCHA双人舱 + 本周热点+本周脚本`
- `@小狄氧舱账号维护智能机器人 成都高新体验馆 + GYCHC碳纤维四人舱 + 本周热点+10条针对企业老板的脚本`

---

## 四、 如何上传至 GitHub 并安装到 WorkBuddy
1. **上传至 GitHub**：在 GitHub 新建公开仓库 `xiaodi-account-maintenance-bot`，将本目录所有文件拖拽上传或通过 `git push` 推送。
2. **安装到电脑端 WorkBuddy**：打开 WorkBuddy → 进入左侧「技能 / Skills」管理 → 点击「导入技能 / 添加 Skill」→ 选择 **从 GitHub 链接导入**（填入仓库地址）或 **导入本地文件夹 / ZIP 包** 即可启用。

---
**License**：MIT License
