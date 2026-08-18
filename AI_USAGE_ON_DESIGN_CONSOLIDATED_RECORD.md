# AI Usage on Design — Consolidated Chat & Work Record

> Project: **AI Usage Study**  
> Owner: **Michael Fan**  
> Last consolidated: **18 August 2026**  
> Language: **繁體中文／廣東話為主，保留必要 English terminology**

## 1. 文件目的與範圍

本文件整合目前可取得的 AI Usage Study 聊天紀錄、研究筆記、工作框架、AI workflow、工具調查及設計實踐，方便後續：

- 建立 AI × UX/UI Design 的共通知識庫；
- 對齊 UX Research、UX Writing、Product、Engineering 與 Design 的合作方式；
- 規劃受監管銀行環境內的 AI adoption；
- 保存已討論的 decisions、assumptions、risks、tools 與 next actions；
- 作為日後 pilot、training、presentation 或 team playbook 的基礎。

### Public-repository privacy boundary

此 repository 是公開的，因此本整合版只收錄去識別化的工作知識。銀行內部逐字稿、受訪者個人資料、同事姓名、未公開 project details、原始錄音及可能受保密條款限制的資料不會原文放入本文件。原始資料只在 Source Inventory 中以檔名記錄。

### Completeness note

這是一份 **consolidated project record**，並非 ChatGPT account 的逐字 export。內容以目前可見的 project conversation summary、已保存 artifacts，以及可讀取的研究資料為準。

---

## 2. Executive Summary

AI 在 UX/UI 工作中最有價值的角色，不是取代 designer 或 researcher，而是擴闊探索、整理證據、加快低風險重複工作，以及縮短「idea → prototype → feedback → iteration」循環。

本研究形成了以下共同原則：

1. **AI proposes, humans decide, authorised systems act.**
2. AI 可以準備、整理、分類、草擬及提出選項；Human 必須負責方向、判斷、驗證、批准與 accountability。
3. AI output 必須連回 source evidence，清楚區分 facts、assumptions、unknowns 及 hypotheses。
4. Synthetic users 只適合 pre-UT sense check，不可取代真實 user research。
5. 在 banking／regulated environment，privacy、security、access control、audit trail、compliance review 與 human approval 必須先於 automation speed。
6. AI adoption 不應只量度「節省幾多時間」，亦應量度 quality、rework、decision confidence、traceability、adoption 與 risk。

Figma 2026 AI research 亦顯示，AI 的影響正由個人效率擴展到 team collaboration；design 與 code 的界線變得更流動，design 的價值則更集中於 problem framing、taste、trust、system behaviour 及 error recovery。

---

## 3. Core UX/UI Product Designer Lifecycle

本 project 採用以下八個 stages 組織 AI adoption 與設計工作：

| Stage | 核心問題 | 常見 deliverables | AI 可以協助 | Human responsibility |
| --- | --- | --- | --- | --- |
| Discover | 我們要解決甚麼問題？ | Journey Map、Stakeholder Map、Research Plan | 整理 brief、找缺口、產生問題清單 | 對齊 business/user goal、設定方向 |
| Research | 有甚麼 evidence？ | Interviews、Competitor Audit、Insights | Transcription、tagging、repository search、初步 synthesis | Research design、interpretation、bias check |
| Prototype | 有哪些可行方案？ | User Flow、Wireframe、Figma Prototype | 產生 variants、copy draft、structure suggestion | Interaction logic、design judgement、brand fit |
| Pilot | 方案是否有效？ | User Testing、Usability Report、Iteration | Test script、note grouping、issue clustering | Moderation、finding validation、priority decision |
| Production | 能否安全準確交付？ | Design Specs、Design QA、Accessibility Review | Spec draft、token check、copy consistency、QA checklist | Final QA、compliance、handoff accountability |
| Observe | 真實使用情況如何？ | GA4、Heatmaps、Session Replay、Agent Logs | Summarise signals、detect anomaly、group feedback | Metric interpretation、causality judgement |
| Optimize | 下一輪改善甚麼？ | Backlog、A/B Test、Iteration Plan | Opportunity ranking、hypothesis draft、change log | Prioritisation、experiment approval |
| Scale | 如何成為團隊能力？ | Governance、Templates、Training、Reusable Components | Knowledge retrieval、workflow orchestration | Ownership、policy、access、change management |

---

## 4. Theme-based Knowledge

### 4.1 AI as a design partner, not an autopilot

AI 適合：

- 擴闊 problem space；
- 快速形成 hypotheses；
- 草擬 research questions、meeting agenda、PRD、UX copy 及 documentation；
- 將散落 notes 分類和摘要；
- 產生多個方案以支援 divergence；
- 把 feedback 轉成可追蹤 issues 和 iteration suggestions。

AI 不應自行：

- 代表使用者作最終結論；
- 把 plausible text 當成 verified fact；
- 批准 banking content、legal wording 或 production release；
- 在沒有 source traceability 下決定 priority；
- 用 synthetic participant 取代真實 research participant。

### 4.2 Human-in-the-loop

Human checkpoints 應出現在：

- Goal／scope approval；
- Research plan approval；
- Finding validation；
- Design direction selection；
- Legal／Compliance／Accessibility review；
- Launch approval；
- Post-launch interpretation。

### 4.3 Source-grounded knowledge

理想的 AI research repository 應做到：

- 每項 insight 可連回 transcript、quote、ticket、analytics 或 source file；
- 顯示 evidence strength 與 confidence；
- 主動指出資料缺口與互相衝突的 evidence；
- 保留 version、owner、date、decision history；
- 支援權限控制及 audit trail。

### 4.4 Multiplayer design

AI 令 PM、designer、developer、researcher 可更早共同工作：

- PM 可以把 idea 快速變成 prototype；
- Designer 可以更早參與 discovery 和 product direction；
- Developer 可以在 canvas 與 code 之間迭代；
- Research insight 可以更快回到 design backlog；
- Linear handoff 逐步變成 parallel／iterative collaboration。

### 4.5 Designing AI experiences

AI product 並非普通 deterministic flow。Designer 需要同時設計：

- System behaviour 與 boundaries；
- Confidence、uncertainty 與 explanation；
- User control、confirmation 與 undo；
- Error、recovery、fallback 與 escalation；
- Trust、consent、privacy 與 transparency；
- Prompt／context handling；
- Agent action history 與 auditability。

---

## 5. Workflow Mapping

### 5.1 General agentic AI loop

**Goal → Plan → Act → Observe → Evaluate → Improve → Repeat or Stop**

| Step | Human lead | AI assist | Main output |
| --- | --- | --- | --- |
| Goal | 定義 business、user、design goals | 重寫及檢查 goal clarity | Approved goal statement |
| Plan | 決定 scope、method、risk | 拆 tasks、列 assumptions／unknowns | Work plan |
| Act | 研究、設計、測試、協作 | Search、draft、generate、classify | Evidence／design draft |
| Observe | 檢查 participant／user／system response | Transcribe、tag、summarise | Raw observations |
| Evaluate | 驗證 evidence、判斷 priority | 找 patterns、contradictions、gaps | Validated findings |
| Improve | 決定 design change | 建議 variants、copy、checklist | Updated prototype |
| Repeat／Stop | 判斷是否已達 stop condition | 比較 versions、整理 decision log | Next loop or approval |

### 5.2 Beginner journey: credit-card campaign page redesign

1. Receive business request。
2. Clarify business goal、user goal、design goal。
3. 收集 existing page、brand rules、data、research、constraints。
4. 將資料分類為 **Facts／Assumptions／Unknowns**。
5. 建立 work plan、scope、priority、timeline。
6. 進行 UX audit、competitor review、content review。
7. 建立 IA、wireframe、copy options、prototype variants。
8. 執行 usability test／stakeholder review。
9. 將 findings 連回 raw observations 與 supporting evidence。
10. 更新設計並 retest。
11. 完成 Business、Legal、Compliance、Accessibility、Design QA approval。
12. Launch 並確認 tracking。
13. 觀察 GA4／analytics／feedback，啟動下一個 optimization loop。

### 5.3 Recommended stop conditions

- Research questions 已得到足夠 evidence 回答；
- 沒有 critical usability issue；
- User 能理解並完成 key task；
- Required stakeholders 已批准；
- Tracking 與 launch readiness 已確認；
- 下一步只能由 real-world data 驗證。

---

## 6. UX Research × UX/UI Designer Collaboration Study

### 6.1 30-minute catch-up focus

研究討論聚焦三個問題：

1. UX Research team 的 end-to-end workflow 是甚麼？
2. Researcher 與 UX/UI Designer 在甚麼時間點合作、交接或共同決策？
3. 現有及期望中的 AI usage，可以在哪些 steps 提升速度、quality 或 traceability？

### 6.2 Observed workflow

**Intake／planning → Recruitment → Fieldwork → Analysis → Reporting → Design action → Follow-up**

### 6.3 Key collaboration pain points

- Research 與 Design 有時以 parallel timeline 推進，早期 alignment 不足；
- Jira／task ownership／status visibility 可能不一致；
- Notes、recordings、reports 分散在 shared drives 或不同 tools；
- Insight 與 design decision 未必保留清晰 traceability；
- 重複整理 transcript、tag、summary 和 report template 花費大量時間；
- AI output 的 accuracy、source、privacy 及 governance 尚需共同標準。

### 6.4 Current／piloted tooling inventory

以下屬於研究對話中提及的實際工具、內部能力或試行方向：

| Area | Tool／platform | Status／use |
| --- | --- | --- |
| Meeting／recording | Zoom AI | Meeting／recording support |
| Enterprise AI | Internal AI tool | Internal experimentation；產品名稱未可靠確認 |
| Research activities | Optimal Workshop | Research task support |
| Prototype | Figma prototypes | Design／test prototype |
| Storage | OneDrive／shared drives | Files、recordings、reports |
| Issue tracking | Jira | Tasks、issues、actions |
| Productivity AI | Microsoft Copilot | General productivity support |
| Reporting | Research-report template pilot | Standardising report creation |
| Pre-UT check | Synthetic-user experiment | Rapid sense check only；not a research replacement |

以下只屬建議或探索，不能寫成已採用：Maze、Dovetail、UserTesting、Doubao（豆包）及其他 external research tools。

### 6.5 Desired future capabilities

- Central recording／research repository；
- Source-linked Q&A；
- Gap、conflict 及 missing-evidence identification；
- AI-assisted probing question generation；
- Transcript → themes → findings → report automation；
- Research issue／action tracking；
- Synthetic-user sense check with explicit limitations；
- Reusable research／UX writing／design templates。

---

## 7. UX Writing × UX/UI Collaboration Study

### 7.1 Discovery objective

了解 UX Writing team：

- 如何接收 design／business request；
- 何時參與 user flow、wireframe、prototype、QA；
- 如何管理 terminology、tone of voice、legal copy、localisation；
- 如何與 designer 處理 Figma content、comments、handoff 及 revisions；
- 現時已使用或希望使用哪些 AI tools。

### 7.2 AI opportunities

- First-draft copy variants；
- Tone／terminology consistency checking；
- Plain-language rewrite；
- Translation／localisation layout check；
- Content inventory、duplicate detection、content gap detection；
- Error message、empty state、confirmation copy suggestions；
- Copy QA against approved glossary and legal wording；
- Figma content → CMS／repository sync concept。

### 7.3 Human controls

UX Writer 必須保留 final editorial judgement；banking claims、fees、eligibility、risk、terms and conditions 必須由 authorised owner／Legal／Compliance review。

---

## 8. Figma AI Study

### 8.1 Main workflow opportunities

- First draft／wireframe generation；
- Replace content、rewrite、shorten、translate；
- Generate／remove／edit imagery where appropriate；
- Layer naming、content population、rapid variants；
- Figma Make for prompt-to-prototype exploration；
- Design system reuse and component discovery；
- Code／canvas iteration through MCP-related workflows；
- Prototype divergence: generate multiple directions before selecting one。

### 8.2 Recommended iteration order

1. Structure；
2. Content；
3. Visual design；
4. Interaction／states；
5. Accessibility／QA；
6. Production readiness。

### 8.3 Four AI adoption patterns from Figma’s 2026 report

| Pattern | Description | Main risk |
| --- | --- | --- |
| Unified | Individual and organisation both adopt rapidly | Governance and scaling quality |
| Grassroots | Individuals move faster than organisation | Fragmented tools、workarounds、low confidence |
| Directive | Leadership moves first；teams catch up | Pressure without team capability |
| Nascent | Individual and organisation both move slowly | Missed learning and capability gap |

### 8.4 Selected report signals

- AI impact is moving from personal productivity to team collaboration；
- Designers increasingly participate in development；developers increasingly participate in design；
- Interactive prototypes and code／canvas iteration are becoming more common；
- AI product design increases the importance of trust、behaviour、judgement and error recovery；
- Shared standards and workflows are necessary to convert individual usage into team capability。

---

## 9. Agentic UX/UI Tool Ecosystem

| Need | Possible system role | Typical examples | Important control |
| --- | --- | --- | --- |
| Knowledge／reasoning | Summarise、classify、draft、retrieve | Approved enterprise LLM／ChatGPT／Copilot | Approved data boundary、source citation |
| Design canvas | Explore flows、variants、prototype | Figma、FigJam、Figma AI／Make | Design review、component governance |
| Component source | Store tokens、components、documentation | GitHub、Storybook | Version control、code review |
| Work management | Track request、decision、issue、owner | Jira、Confluence | Clear ownership、status discipline |
| Research | Test、analyse、store evidence | Approved research tools／repository | Consent、PII protection、method validity |
| Analytics | Observe real behaviour | GA4、Adobe Analytics、session tools | Tracking governance、causality caution |
| CMS／content | Reuse and publish approved content | Enterprise CMS／Figma content workflow | Editorial、Legal、Compliance approval |

### Storybook in this ecosystem

Storybook 是用來獨立建立、展示、測試及記錄 UI components 的 development environment。它可以讓 designer、developer 與 AI 查閱 production-ready component states，而 GitHub 則保存 source code、tokens、documentation 及 version history。

---

## 10. Pain Points Summary

| Theme | Pain point | Impact |
| --- | --- | --- |
| Problem framing | Design 被太遲加入 project | 容易直接跳到 solution、增加 rework |
| Knowledge | Files、notes、reports 分散 | Search time 長、insight 難重用 |
| Traceability | Findings 未連回 source | Decision confidence 低、難 audit |
| Collaboration | Research／Design／Product timeline 不同步 | Duplicate work、handoff gap |
| Content | Revisions、translation、terminology checking 重複 | Delivery 慢、consistency risk |
| Production | Design system 與 implementation 未同步 | Component drift、QA debt |
| AI quality | Hallucination、overconfident summary | 錯誤 insight 或錯誤 decision |
| Governance | Approved tools、data rules、ownership 不清 | Privacy、security、compliance risk |
| Adoption | 個人 experiment 多、team standard 少 | 難 scale、難量度效果 |

---

## 11. AI Opportunity Map

| Priority | Opportunity | Why | Suggested success measures |
| --- | --- | --- | --- |
| P1 | Meeting／research transcription and structured summary | High manual effort、low-risk with approved data handling | Editing time、accuracy、source coverage |
| P1 | Source-linked research repository search | Improves reuse and traceability | Search time、answer citation rate、reuse rate |
| P1 | UX writing consistency／glossary check | Frequent repetitive QA | Issues caught、review time、terminology compliance |
| P1 | Figma／design documentation assistant | Reduces handoff admin | Spec time、missing-state rate、developer questions |
| P2 | Feedback → Jira issue draft | Shortens action loop | Time to log、duplicate rate、acceptance rate |
| P2 | Design system component recommendation | Increases reuse | Component reuse、custom component reduction |
| P2 | Analytics summary／opportunity detection | Speeds Observe stage | Time to insight、validated opportunity rate |
| P3 | Synthetic-user pre-check | Cheap early sense check | Real-UT agreement rate、false confidence rate |
| P3 | Multi-agent workflow orchestration | Connects tools and stages | End-to-end cycle time、human intervention、error rate |

---

## 12. Governance and Risk Controls

### 12.1 Minimum controls

- Use only approved tools and connectors；
- Never input customer PII、credentials、confidential strategy or restricted banking data into unapproved models；
- Apply least-privilege access；
- Keep source links、prompt／output history、version and owner；
- Require human approval before external communication、ticket mutation、design publication or launch；
- Redact participant and employee identifiers；
- Add confidence／limitation notes to AI-generated findings；
- Test against representative real users；
- Define fallback and escalation when the AI is uncertain or wrong。

### 12.2 Anti-hallucination checklist

1. Ask AI to separate fact、assumption、unknown and recommendation。
2. Require source for every important claim。
3. Verify names、numbers、dates、quotes and tool adoption status。
4. Do not accept a theme without enough raw evidence。
5. Search for conflicting evidence and negative cases。
6. Let a qualified human approve the final interpretation。

---

## 13. Pilot Roadmap

### Phase 1 — Discover／baseline

- Select one low-risk workflow；
- Map current time、quality、pain points and tools；
- Confirm approved data and security boundary；
- Define KPI、guardrails、owner and stop condition。

### Phase 2 — Prototype

- Build prompt／template／connector workflow；
- Use redacted or synthetic sample data；
- Test accuracy、source traceability and usability；
- Record human corrections。

### Phase 3 — Pilot

- Run with a small team；
- Keep manual approval at each critical step；
- Compare AI-assisted versus current workflow；
- Gather researcher、writer、designer and stakeholder feedback。

### Phase 4 — Production and Scale

- Confirm Legal／Compliance／Security／Data approval；
- Publish SOP、roles、templates、training and escalation path；
- Monitor adoption、quality、risk and ROI；
- Review monthly and iterate。

---

## 14. KPI Framework

| Dimension | Example KPI |
| --- | --- |
| Efficiency | Cycle time、manual hours、time-to-first-draft |
| Quality | Accuracy、issue rate、rework、missing-state rate |
| Research integrity | Source coverage、validated finding rate、quote traceability |
| Design consistency | Component reuse、token compliance、copy consistency |
| Collaboration | Handoff questions、alignment time、decision turnaround |
| Adoption | Active users、repeat use、template reuse、completion rate |
| Risk | PII incidents、unapproved-tool use、hallucination severity、override rate |
| Outcome | Task success、conversion、VTA、satisfaction、support contact rate |

---

## 15. Action Items

1. 建立一個 approved AI tool inventory，標示 owner、data rule、use case、status。
2. 選擇 transcription／research summary 作第一個 low-risk pilot。
3. 建立共用 report structure：Executive Summary → Theme-based Knowledge → Workflow Mapping → Pain Points → AI Opportunities → Action Items → Supporting Quotes → Full Transcript（internal only）。
4. 定義 Facts／Assumptions／Unknowns／Evidence 的標準欄位。
5. 為 AI output 加入 source link、confidence、reviewer、date、version。
6. 建立 UX Research × Design 的 RACI、Jira status 和 handoff checkpoints。
7. 建立 UX Writing glossary、approved claims、tone rules 和 AI QA checklist。
8. 評估 Figma ↔ GitHub ↔ Storybook 的 design system retrieval／sync pilot。
9. 定義 synthetic-user 使用限制和 real-user validation requirement。
10. 每月用 KPI framework 回顧 pilot，決定 optimize、scale 或 stop。

---

## 16. Supporting Statements from the Study

以下為 project 內反覆出現的核心表述；為保護私隱及避免公開逐字稿，採用整理後語句：

- AI 應該幫團隊準備、整理和提出選項，但最終判斷由人負責。
- Research 與 Design 如果太遲對齊，後面會出現 Jira、timing 和 action gap。
- Synthetic users 可以作快速 sense check，但不能代替真實研究。
- Repository 的價值不只是儲存檔案，而是讓答案連回 source、指出 gaps 和保留 decisions。
- Faster is not automatically better；AI 的真正價值是幫助團隊探索更多、思考更深和更早驗證。
- AI era 的 human advantage 包括理解人、建立信任、facilitation、taste 和 accountable judgement。

---

## 17. Chronological Chat／Work Record Index

| Date | Record／topic | Main outcome |
| --- | --- | --- |
| 2026-07-24 | GPT Work、Agentic AI loop、Human-in-the-loop | 建立 AI-assisted UX/UI workflow 和 human／AI action distinction |
| 2026-07-24 | AI Adoption Plan for UX/UI | 加入 GitHub、Storybook、Figma、Jira／Confluence 協作構想 |
| 2026-07-27 | Agentic AI 支援 UX/UI | 整理 prompt、workflow stages、storage／sync options |
| 2026-07-28 | UX/UI design process study | 以 product-design lifecycle 對照 AI 使用點 |
| 2026-07-29 | Figma AI functions × UX/UI workflow | 整理 Figma AI、CMS／UX writing collaboration 機會 |
| 2026-07-29 | Reduce AI mistakes／hallucinations | 建立 evidence、verification、human review 原則 |
| 2026-07-30 | UX Research Catch-up Plan | 30-minute workflow／collaboration／AI usage agenda |
| 2026-07-30 | AI Loop 2026 beginner guide | Goal → Plan → Act → Observe → Evaluate → Improve loop |
| 2026-07-31 | Credit-card campaign AI loop | 建立由 business request 到 post-launch 的 beginner journey map |
| 2026-07-31 | UX Copywriting Catch-up Plan | 建立 UX Writing × Design workflow 和 AI discovery questions |
| 2026-07-31 | Figma 2026 AI report review | Unified／Grassroots／Directive／Nascent adoption patterns |
| 2026-07-31 | 2026 AI tools overview | 研究 UX research、testing、multi-tool／agent loop platforms |
| 2026-08-03 to 2026-08-14 | UX Research AI Usage Discover | 52:31 Cantonese transcript、tool inventory、pain points、AI opportunities |
| 2026-08-05 | UX/UI Product Designer lifecycle | 確立 Discover、Research、Prototype、Pilot、Production、Observe、Optimize、Scale |
| 2026-08-18 | Consolidated project record | 將 project knowledge 整合成 public-safe Markdown |

---

## 18. Source Inventory

### Saved artifacts reviewed

- `agentic_ai_ux_ui_master_guide.md`
- `UX-Research-AI-Usage-Discover_Cantonese-Transcript.md`
- `AI Loop for Beginners: UX Process Map.png`
- `How-I-Use-AI-to-Design-Better-2026-Aligned.pdf`
- `790e42a9663f2f4a772e5cc6547b5d2e6b59cb8c.pdf` — Figma’s 2026 AI report

### Related generated visuals recorded

- `Workflow Map: AI Campaign Design Cycle.png`
- `Chinese AI Workflow Loop Infographic.png`
- `AI Loop 2026 初學者指南.png`
- `AI Loop 入門資訊圖.png`
- `AI Loop 2026：人機協作循環圖.png`

### Internal-only source

- `UX-Research-AI-Usage-Discover_Cantonese-Transcript.md` contains a 52:31 Cantonese research conversation with speaker labels and identifiable internal context. It is represented in this public document through sanitised findings only and is not reproduced in full.

---

## 19. Recommended Repository Structure

```text
Ai-Usage-On-Design/
├── AI_USAGE_ON_DESIGN_CONSOLIDATED_RECORD.md
├── README.md                         # Future project landing page
├── frameworks/                      # Lifecycle, AI loop, governance
├── research/                        # Public-safe research summaries
├── templates/                       # Interview, report, prompt templates
├── pilots/                          # Pilot plans and KPI readouts
└── assets/                          # Approved public visuals
```

---

## 20. Version Notes

### v1.0 — 18 August 2026

- Consolidated available AI Usage Study conversation records and saved artifacts；
- Applied the eight-stage UX/UI lifecycle；
- Added UX Research、UX Writing、Figma AI、agentic loop、tool ecosystem、governance、KPI and pilot roadmap；
- Removed or generalised sensitive internal information for public-repository use；
- Explicitly separated actual／piloted tools from suggested tools。
