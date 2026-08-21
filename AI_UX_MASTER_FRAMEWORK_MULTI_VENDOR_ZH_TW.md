# 設計工作流程中的 AI 應用——多平台 3A × 3K Master Framework

**最終草稿日期：** 2026-08-21  
**設計生命週期：** Discover 探索 → Research 研究 → Prototype 原型 → Pilot 試行 → Production 生產 → Observe 觀察 → Optimize 優化 → Scale 規模化  
**框架：** 3A AI 成熟度 × 3K 知識維度  
**主要情境：** 受監管銀行的 UX/UI 數碼產品設計  
**涵蓋範圍：** Google、Figma、OpenAI、Anthropic、Microsoft、Atlassian 及精選 UX 專用平台

---

## 1. Executive Summary 執行摘要

這是 vendor-neutral（不綁定單一供應商）的 master version。較早的 Google-only framework 仍可作為 Google 生態的深入參考，但實際設計工作流程應根據工作目的、證據質素、系統整合及風險選擇工具，而不是把單一供應商強行放進每個步驟。

- **3A 衡量運作成熟度。** **Adopt** 是整合已核准的 AI 協助；**Adapt** 是把工作流程標準化及客製化；**Adept** 是以已評估、可觀察及可回復的自動化重新設計工作模式。
- **3K 衡量使用者知識。** **Know-how** 是執行能力；**Know-what** 是策略判斷；**Know-where** 是在正確情境、來源、帳戶及系統使用 AI 的能力。
- 產品內置 Autonomous Agent，不代表公司已達 **Adept**。成熟度取決於治理、可重複性、評估、Owner 及可量度成果，而非產品宣傳用語。
- 建議架構要分開 **System of Record（權威資料系統）**、**AI Reasoning Assistant（推理助手）**、**Creation Surface（創作介面）**、**Validation Surface（驗證介面）** 及 **Action Layer（執行層）**。不應讓同一產品無聲地同時成為全部五者。
- AI 可加快證據整理、方案發散、文件撰寫、Prototype 製作、測試分析及 Code Drafting；Research Consent、Problem Framing、Design Decision、Accessibility Acceptance、Model Risk Threshold 及 Production Release 仍由人類負責。

> **Human-accountability rule：** AI 可以提出、摘要、生成、比較或提示問題；指定的 Designer、Researcher、Analyst、Engineer 或 Product Owner 必須核對證據並承擔最終決定。

### 1.1 3A 成熟度定義

| 級別 | 運作定義 | 所需證據 | 不能證明成熟度的事項 |
|---|---|---|---|
| **Adopt — 整合** | 已核准的現成 AI 功能協助範圍清晰、可回復的工作；每項輸出均由人手轉移 Context 及核准。 | 明確 Use Case、受訓使用者、Baseline、Review Checklist、Manual Fallback。 | 使用最強模型；大量生成 Artifact。 |
| **Adapt — 客製化** | 團隊使用受管控的 Source Pack、Reusable Instructions、Schema、Rubric、Connector 或 Design System Context。 | 有版本的配置、Owner、代表性 Test Set、受控 Data Routing、已量度的改善。 | 只有一次性的 Custom Prompt、Project、Gem 或 Template，卻沒有 Lifecycle Control。 |
| **Adept — 掌握／創新** | 已評估的自動化協調已核准系統，並具備 Observability、Least Privilege 及由人控制的 Release。 | Production Evaluation、Logs、Drift/Cost Monitoring、Confirmation Points、Rollback 及已證實的 User Benefit。 | 無人監督的 Prototype；未經證明便大規模推行。 |

### 1.2 3K 知識維度定義

| 維度 | 必須回答的問題 |
|---|---|
| **Know-how 執行技能** | Designer 能否完成任務、檢查證據、修改 Artifact，並在失敗時復原？ |
| **Know-what 策略識別** | Designer 能否識別正確問題、必須保留的人類判斷、風險及成功證據？ |
| **Know-where 情境／來源** | Designer 能否把每項 Input/Output 放進正確的核准帳戶、來源、System of Record 及 Decision Point？ |

---

## 2. Tool-selection Architecture 工具選擇架構

### 2.1 五個不同角色

| 角色 | 目的 | 例子 | 控制原則 |
|---|---|---|---|
| **System of Record** | 儲存權威 Research、Requirement、Decision、Component 或 Code | Confluence、Jira、Dovetail、Figma Libraries、Storybook、Git | AI 可讀取已核准內容，但不可無聲取代 Ownership、Versioning 或 Approval。 |
| **Reasoning Assistant** | 搜尋、綜合、比較、草擬及批判 | ChatGPT Work、Claude for Work、Gemini、Microsoft 365 Copilot、Rovo、Notion AI | 必須限制 Source Scope、提供 Citation/Evidence Link、指出不確定性並由人核對。 |
| **Creation Surface** | 直接操作 Flow、Screen、Prototype、Media 或 Document | Figma agent、Figma Make、Figma Weave、Miro AI、Claude Artifacts、Copilot Pages | 生成結果必須可編輯，並保留 Provenance 及 Canonical Design System Mapping。 |
| **Validation Surface** | 測試 Accessibility、Component、Visual Change、Research Result 或 Telemetry | Stark Sidekick、Storybook/Chromatic、Maze、UserTesting、GA4、BigQuery/Looker | 自動檢查只涵蓋指定規則；Human Testing 及 Expert Acceptance 仍屬必要。 |
| **Action / Agent Layer** | 從跨系統擷取資料或執行動作 | Rovo Agents、Copilot Studio、ChatGPT Connectors/Agents、Claude Connectors/MCP、Figma MCP、Codex、Claude Code | Least Privilege、Read-only Default、Explicit Confirmation、Logs、Allowlists、Stop Conditions 及 Rollback。 |

### 2.2 資料分類

| 類別 | 例子 | 預設規則 |
|---|---|---|
| **D0 — 公開／模擬** | 已發布資料、虛構 Persona、已核准 Placeholder Content | 可輸入已核准工具；仍須檢查 Copyright、Product Status 及 Source Quality。 |
| **D1 — 內部** | 非敏感流程筆記、Draft Requirement | 只可使用受管控 Enterprise Account；必須有 Owner 及 Retention。 |
| **D2 — 機密** | 未發布產品、專有 Research、Code、Design System Asset | 只可使用具 IAM、DLP、Retention、Logging 及 Minimum-necessary Data 的已核准 Enterprise Tenancy/Project。 |
| **D3 — 個人／受監管** | Participant、Customer、Employee Data、Recording、Financial/Transaction Data | 預設禁止；必須取得特定目的的 Privacy、Legal、Security Approval，並具 Consent/Lawful Basis、Minimization 及 Deletion Lineage。 |

---

## 3. 多平台 Product / Surface Catalogue

**閱讀原則：** 「AI may assist」描述實際設計用途，不代表工具可以作出 Design Decision。採購或正式使用前，必須重新確認 Availability、Edition、Data Handling、Region 及 Beta Status。

| Capability Lane | Product / Surface | Vendor | AI may assist | 最適合階段 | 銀行使用邊界／人類控制 | 狀態及官方來源 |
|---|---|---|---|---|---|---|
| 通用工作助手 | **ChatGPT Work — Projects、Deep Research、File Analysis、Connectors、Visual Work Surfaces** | OpenAI | 搜尋及綜合已核准來源；比較 Brief；分析檔案；草擬 Research Plan、Flow、Specification 及 Review Checklist。 | Discover、Research、Observe、Scale | D1–D3 只可使用 Enterprise Workspace 及已核准 Connector；Designer 必須打開來源及驗證結論。 | 功能視 Workspace 及 Admin Control 而異。[OpenAI 官方文件](https://developers.openai.com/) |
| 圖像生成／編輯 | **GPT Image 2** | OpenAI | 生成模擬 Concept Image、編輯已授權 Asset、製作 Mood-board Direction 及 Placeholder Visual。 | Prototype、Pilot、Optimize | 預設只用 D0／已核准 Reference；Brand/Legal 審核 Representation、Likeness、Text 及 IP。 | 新工作不應依賴已 Deprecated 的 DALL·E Surface。[GPT Image 2](https://developers.openai.com/api/docs/models/gpt-image-2) |
| Coding Agent | **Codex** | OpenAI | 讀取已核准 Repository、實作 UI Draft、建立 Test、檢查 Diff 及協助 Code Review。 | Production、Scale | Code 由 Developer 負責；Security、Accessibility、Test 及 Merge Gate 仍是必要。 | 只可在已核准 Repository 及 Environment 使用。[OpenAI 官方文件](https://developers.openai.com/) |
| 通用推理 | **Claude for Work — Projects、Artifacts、Web Search、Connectors** | Anthropic | 保存 Project Context；綜合證據；建立可編輯 Document、Diagram、Flowchart、React Prototype 及批判性 Review。 | Discover、Research、Prototype、Scale | 公司資料使用 Work Plan；檢查 Connector Scope。Artifact 是 Prototype，不是 Production 或 Accessibility 證明。 | Artifacts 支援 Document、SVG、Diagram、Website 及 React Component。[Claude Artifacts](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them) · [Projects](https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects) |
| Connected Assistant | **Claude Connectors / Remote MCP** | Anthropic | 從 Google Drive、Atlassian 或其他已啟用服務取得已核准內容，並透過已允許 Connector 執行動作。 | Discover、Research、Production、Scale | 由 Owner 啟用、Least Privilege、Read-only Default；Custom MCP 可能帶來 Prompt Injection 或 Malicious Tool Risk。 | 功能及可用性視 Plan 而異。[Custom Connectors](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp) |
| Coding Agent | **Claude Code** | Anthropic | 檢查 Codebase、草擬 UI Implementation、Test、Documentation；在設定後使用 Figma MCP Context。 | Production、Scale | Developer 審核所有 Diff；禁止無人監督 Merge/Deploy。 | 適用 Commercial Agreement 及 Security Configuration。[Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) |
| Managed Productivity | **Microsoft 365 Copilot Chat、Copilot Pages** | Microsoft | 以獲授權的 M365 Content 為 Grounding；把回覆轉為持久、可編輯、可分享的 Problem Brief、Research Summary 及 Decision Page。 | Discover、Research、Pilot、Scale | Copilot 沿用現有權限，因此過度分享仍是治理風險；Owner 必須核對來源及 Access。 | Pages 是可編輯的 Collaborative Canvas。[Copilot Pages](https://support.microsoft.com/en-us/microsoft-365-copilot/get-started-with-microsoft-365-copilot-pages) · [Privacy](https://learn.microsoft.com/en-us/copilot/privacy-and-protections) |
| Enterprise Agent Builder | **Copilot Studio / Microsoft 365 Declarative Agents** | Microsoft | 使用 Instructions、Approved Knowledge 及 Bounded Actions 建立 Design Knowledge 或 Policy Assistant。 | 所有階段的 Adapt/Adept | 適合 Scoped Retrieval 及 Simple Workflow；複雜 Multi-step Decision 需要 Custom Orchestration 及 Human Gate。 | Declarative Agent 繼承 M365 Control，但有 Architecture Limit。[Declarative Agents](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-declarative-agent) · [Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio) |
| Google Managed Work | **Gemini in Workspace / Managed Gemini App** | Google | 草擬／摘要 Docs、Sheets、Slides；分析已核准檔案；支援 Discovery、Research、Reporting 及 Communication。 | Discover、Research、Pilot、Observe、Scale | 銀行資料只可用 Managed Account；Availability 及 Control 視 Edition/Region 而異。 | [Workspace AI Privacy](https://workspace.google.com/security/ai-privacy/) |
| Source-grounded Notebook | **Gemini Notebook（前稱 NotebookLM）** | Google | 由已核准 Brief、Policy、Research 建立附 Citation 的 Evidence Notebook；產生 Briefing Guide 及找出矛盾。 | Discover、Research、Scale | Imported Copy 可能過期；需要 Source Owner、Canonical URI、Sync State 及 Expiry。 | [Source Behavior](https://support.google.com/notebooklm/answer/16215270) |
| Google Enterprise/API | **Gemini Enterprise Agent Platform / Gemini API** | Google | 在 Off-the-shelf Chat 不足時，建立已評估的 Grounded Assistant、Multimodal Analysis 或受管控 Product AI。 | 所有階段的 Adapt/Adept | Platform Team 必須提供 IAM、Redaction、Observability、Evaluation、Region、Retention、Rollback。 | 個別 API/Feature 可能是 GA 或 Preview。[Enterprise Agent Platform](https://cloud.google.com/products/gemini-enterprise-agent-platform) |
| Google Coding | **Gemini Code Assist Standard/Enterprise** | Google | 在已核准 Development Environment 草擬 UI Code、Test 及 Explanation。 | Production、Scale | Engineering Review 及 Canonical Component Mapping 必須保留。 | [Gemini Code Assist](https://developers.google.com/gemini-code-assist/docs/write-code-gemini) |
| Knowledge / Search | **Confluence + Atlassian Rovo Search、Chat、Agents** | Atlassian | 搜尋 Confluence/Jira 及 Connected Sources；根據組織知識回答；草擬／Review Design Documentation；運行 Onboarding 或 Design Policy Agent。 | Discover、Research、Production、Scale | Rovo 尊重 User Permission，但不能解決 Over-sharing 或 Stale Content；每頁需要 Owner、Metadata、Review Date。 | Rovo 包含 Search、Chat、Agents、Studio。[What is Rovo?](https://support.atlassian.com/rovo/docs/what-is-rovo/) · [Agent Profiles](https://support.atlassian.com/rovo/docs/browse-agents/) |
| Knowledge / Search 替代 | **Notion AI Enterprise Search、Research Mode** | Notion | 搜尋 Workspace、Database、Connected Apps、Web；建立附 Citation 的 Project Report；在功能允許時比較 GPT、Claude、Gemini。 | Discover、Research、Scale | 只在 Notion 是已核准 System 時使用；必須刻意限制 Source Scope 並確認 Model-specific Connector 行為。 | Business/Enterprise 功能。[Enterprise Search](https://www.notion.com/help/enterprise-search) · [Research Mode](https://www.notion.com/help/research-mode) |
| Research Repository | **Dovetail AI — Contextual Chat、Magic Summary/Highlight/Cluster/Redact** | Dovetail | 轉錄已核准 Session、草擬摘要、Highlight Evidence、Cluster Theme、查詢 Research、建立附 Source Link 的初步 Insight Report。 | Research、Pilot、Observe、Scale | Researcher 檢查 Raw Evidence、Negative Case 及 Sampling；D3 需要 Consent、Retention、Deletion Lineage。 | 功能及語言質素視 Plan 而異。[Dovetail AI](https://dovetail.com/help/dovetail-ai/) |
| Collaborative Synthesis | **Miro AI — Create with AI、Clustering、Summary、Diagram、Prototype** | Miro | 生成可編輯 Sticky Note／Flowchart；按 Keyword/Sentiment 分群；摘要 Workshop；把 Board Content 轉為 Diagram 或 Prototype Draft。 | Discover、Research、Prototype | Facilitator 必須保留 Outlier 及 Participant Meaning；AI Cluster 只是 Hypothesis，不是 Research Finding。 | [Miro AI Overview](https://help.miro.com/hc/en-us/articles/28765406244498-Miro-AI-overview) · [Create with AI](https://help.miro.com/hc/en-us/articles/20164358139794-Create-with-AI) |
| Design Creation | **Figma agent in Figma Design** | Figma | 以對話方式建立、修改、優化設計；套用 Design System；取得 Feedback；建立 Reusable Plugin/Shader。 | Prototype、Optimize、Scale | Designer 檢查 Component Provenance、Layout、Content、States、Accessibility；受 Admin AI Control 約束。 | 本稿日期為 **Open Beta／逐步推出**。[Get Started with Figma AI](https://help.figma.com/hc/en-us/articles/24039793359767-Get-started-with-Figma-AI) |
| Functional Prototyping | **Figma Make** | Figma | 把 Prompt 或 Attached Figma Design/Component 轉為 Functional Prototype、Web App、Interactive UI；直接指定 Preview 區域反覆修改。 | Prototype、Pilot | 在 Code、Data、Security、Accessibility、Performance Review 前，只可視為 Prototype。 | Full Function 視 Plan/Seat 而異。[Explore Figma Make](https://help.figma.com/hc/en-us/articles/31304412302231-Explore-Figma-Make) |
| Media Workflow | **Figma Weave、Weave Tools in Figma** | Figma | 建立 Node-based AI Media Workflow；生成 Variation、Mockup、Vector Illustration；Transfer Style、Replace Background、Change Lighting、Apply Palette。 | Prototype、Optimize | 預設只用 D0／Cleared Asset；保留 Brand/IP Review 及所需 Synthetic Content Disclosure。 | Figma 內的 Weave Tools 是 **Open Beta**；Standalone Weave 是獨立產品。[Use Weave Tools](https://help.figma.com/hc/en-us/articles/40779260614935-Use-Weave-tools-in-Figma) |
| Figma AI Productivity | **Replace Content；Rewrite；Translate；Shorten；Rename Layers** | Figma | 填入真實感 UI Content、修改 UX Copy、批量整理 Layer。 | Prototype、Production | UX Writer/Designer 核對 Product Truth、Legal Text、Terminology、Locale、Naming Convention。 | [Replace Content](https://help.figma.com/hc/en-us/articles/23796390206743-Replace-text-content-with-AI) · [Rename Layers](https://help.figma.com/hc/en-us/articles/24004711129879-Rename-layers-with-AI) |
| Figma AI Imagery | **Make Image；Edit Image；Remove Background；Upscale；Expand/Remove Object** | Figma | 不離開 Design Canvas 即可生成／修改配圖。 | Prototype、Optimize | Brand、Representation、Rights Review；生成圖像不可作事實證據。 | [Make or Edit an Image](https://help.figma.com/hc/en-us/articles/24004542669463-Make-or-edit-an-image-with-AI) |
| Figma AI Prototyping | **Add Interactions with AI** | Figma | 連接已選 Frame、Navigation 及常見 Prototype Flow。 | Prototype、Pilot | Designer 測試全部 Route、Back Behaviour、Keyboard Order、Error/Recovery、Dead End。 | [Make Interactions with AI](https://help.figma.com/hc/en-us/articles/24004778051479-Make-interactions-with-AI) |
| Design-to-code / Context | **Figma Dev Mode、Code Connect、Figma MCP Server** | Figma | 向 Coding Agent 提供 Structured Component、Variable、Layout Context；把 Design Component Map 到 Production Component；在允許時讀寫 Editable Figma Primitive。 | Production、Scale | 必須有 Canonical ID 及 Code Mapping；Agent Output 需要 Diff、Test、Merge Review。 | 部分 MCP Write Capability 是 Beta／受 Seat 限制。[Figma MCP](https://help.figma.com/hc/en-us/articles/39216419318551-Get-started-with-the-Figma-MCP-server) |
| Component Source of Truth | **Storybook + Chromatic Visual Tests** | Storybook/Chromatic | 文件化 Production Component 及 States；以 Screenshot Baseline 找出 Visual Change；Coding Agent 可把 Component Contract 作為 Context。 | Production、Scale | 不會自動證明 UX Quality 或完整 Accessibility；Reviewer 必須核准 Intentional Diff。 | [Storybook Visual Tests](https://storybook.js.org/docs/9/writing-tests/visual-testing) |
| Accessibility Assistant | **Stark Sidekick for Figma/Sketch** | Stark | 掃描 Design 並針對 Contrast、Typography、Alt Text 等問題提出 Fix Suggestion。 | Prototype、Pilot、Production | 「Potential」問題需要人手判斷；Rendered UI 仍需 Keyboard、Screen Reader、Zoom/Reflow、Motion、Cognitive Test。 | [Stark Sidekick](https://www.getstark.co/support/getting-started/using-sidekick/) |
| Research / Testing | **Maze AI — Study Creation、Bias Suggestion、Dynamic Follow-up、AI Moderator、Theme/Sentiment Analysis** | Maze | 草擬 Study、提示 Leading Question、Adaptive Follow-up、摘要 Session 及找出 Theme。 | Research、Pilot、Optimize | Researcher 核准 Objective、Sampling、Question Wording；披露 AI Moderation；Theme 不等於 Causal Proof。 | 部分功能屬 Beta、Enterprise 或 Add-on。[Maze AI](https://maze.co/ai/) |
| Research / Testing 替代 | **UserTesting AI Insight Summary** | UserTesting | 利用 Transcript 及 Behavioral Data 摘要支援的 Task Result Pattern，並連回 Source/Contributor Evidence。 | Pilot、Observe | Researcher Review Session 及 Contradictory Case；Feature Limit 視 Study Type/Contributor Count。 | [AI Insight Summary](https://help.usertesting.com/hc/en-us/articles/13268691111453-AI-insight-summary) |
| App / Prototype Builder | **Replit Agent、Design Canvas** | Replit | 探索 Mockup、比較 Visual Direction、把已核准 Figma Frame 轉為 Interactive App，並在套用至 Code 前反覆修改。 | Prototype、Pilot | 在 Enterprise、Security、Code、Accessibility、Deployment Review 前只屬 Prototype Environment。 | Entitlement 視 Plan 而異。[Replit Agent](https://docs.replit.com/core-concepts/agent) · [Design Systems](https://docs.replit.com/teams/custom-design-system) |
| Analytics | **GA4 / Gemini in BigQuery / Looker Conversational Analytics** | Google | 偵測 Anomaly、草擬需 Review 的 SQL、探索受管控 Semantic Data、協助表達已驗證 Observation。 | Observe、Optimize | Analyst 負責 Event Taxonomy、Consent、Join、Denominator、Power、Causal Interpretation。 | 必須分辨 Preview 及 GA Surface。[Gemini in BigQuery](https://docs.cloud.google.com/bigquery/docs/write-sql-gemini) |

### 3.1 Figma AI 功能名稱——明確清單

Requirement 及 Procurement Record 應使用確切功能名稱，避免只寫含糊的「Figma AI」。

| Figma Surface | 正式功能名稱 | 實際設計用途 | 主要限制 |
|---|---|---|---|
| Figma Design | **Figma agent** | 建立／修改／優化設計、套用 Design System Context、取得 Feedback、建立 Plugin/Shader。 | Open Beta／逐步推出；仍需 Design Review。 |
| Figma Make | **Prompt-to-app Functional Prototyping** | 由 Prompt 及 Figma Context 生成／修改可運作 Prototype 或 Web App。 | Prototype 不等於 Production-ready Application。 |
| Figma Design/Sites | **Replace Content** | 把 Placeholder Copy 換成真實感 Content。 | 不是 Product Truth；核對 Terminology 及 Regulatory Copy。 |
| Figma Products | **Rewrite Text / Translate Text / Shorten Text** | 快速產生 UX Copy Alternative 及 Localization Draft。 | 需要 UX Writing、Localization、Compliance Review。 |
| Figma Design | **Rename Layers with AI** | 按 Context 批量命名 Default Layer。 | 不能完全執行公司 Component Naming Policy。 |
| Figma Products | **Make Image / Edit Image** | 在 Canvas 生成／修改圖像。 | Rights、Factuality、Likeness、Bias 由人核對。 |
| Figma Design | **Add Interactions with AI** | 連接 Frame 及常見 Navigation Action。 | 只是起始 Flow；必須驗證所有 State/Route。 |
| Figma Design | **Asset / Visual Search** | 在功能可用時，以 Visual/Semantic Context 搜尋 Asset/Component。 | Search Result 不證明 Asset 最新或已核准。 |
| Figma Design | **Weave Tools** | Generate Mockup、Transfer Style、Replace Background、Change Lighting、Text to Vector Illustration、Apply Color Palette。 | Open Beta；Standalone Weave 有獨立 Account/Credit。 |
| Dev Workflow | **Figma MCP Server — Read/Write Context** | 向已核准 Agent 提供 Structured Design Context；在允許時建立／更新 Editable Figma Primitive。 | Beta／Seat Limit；每次寫入均須確認及檢查 Diff。 |
| Dev Workflow | **Dev Mode + Code Connect** | 檢查 Design Intent，把 Figma Component Map 到真實 Code Component。 | 需要持續維護 Mapping；本身不是 AI Compliance Check。 |

---

## 4. 八階段 Multi-vendor Workflow

### 4.1 Discover 探索——對齊問題、成果、Stakeholder 及證據

| Step | Context 及 Designer 直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 建立來源** | Designer 列出 Brief、Policy、Past Research、Analytics 及 Stakeholder Owner。 | Confluence + Rovo；M365 Copilot；Notion AI；Gemini Notebook；具核准 Connector 的 ChatGPT/Claude | 找出相關資料、顯示 Source Link、摘要矛盾、指出缺失 Owner/Date。 | 哪項來源最權威；是否允許 Access/Reuse。 | 具 Owner、URI、Update Date、Data Class 的 Source Register。 |
| **Step 2 — 定義問題** | Designer 與 PO/DPO 定義 User、Job、Business Outcome、Constraint、Decision Rights。 | Copilot Pages；ChatGPT Project；Claude Project/Artifact；Gemini in Docs | 草擬 Problem Statement、Assumption Log、Stakeholder Map、Questions。 | Product Strategy、Regulatory Interpretation、Scope、Success Criteria。 | 已核准 Problem Frame 及 Assumption Backlog。 |
| **Step 3 — 視覺化對齊** | 把已核准 Problem Frame 轉為可編輯 System/Journey Overview。 | Miro AI；Figma/FigJam；Claude Artifacts | 由已核准文字建立首版 Flowchart、Stakeholder Map、Journey Structure。 | 圖表是否代表真實情況；未解 Conflict 及 Exclusion。 | 連結 Evidence 的可編輯 Overview Diagram。 |

**3A × 3K：** Adopt 使用範圍清晰的 Summarization；Adapt 使用 Reusable Discovery Rubric 及 Source Manifest；Adept 使用已評估的 Read-only Retrieval Agent。Know-how 是 Prompting 及 Source Inspection；Know-what 是 Strategic Framing；Know-where 是把資料放回 Canonical Evidence。

### 4.2 Research 研究——計劃、收集、綜合並保存證據

| Step | Context 及 Designer/Researcher 直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — Planning** | Researcher 定義 Learning Objective、Sample、Method、Consent、Exclusion。 | ChatGPT Work；Claude；Gemini；M365 Copilot；Maze | 草擬 Guide、批判 Leading Question、建立 Objective-to-question Traceability Matrix。 | Sampling、Ethics、Method、Compensation、Consent、Stopping Rule。 | 已核准 Research Plan 及 Script。 |
| **Step 2 — Collection** | Researcher 執行／監督 Session，只記錄獲准資料。 | Maze AI Moderator/Follow-up；UserTesting；Dovetail Transcription | Transcribe、提出 Bounded Follow-up、Tag Metadata、提示可能 PII。 | AI Moderation 是否合適；Disclosure；Participant Safety；何時介入。 | 與 Consent 相連的 Raw Evidence、Retention/Deletion Record。 |
| **Step 3 — Synthesis** | Researcher Review Transcript、Clip、Observation、Behavioral Evidence。 | Dovetail AI；Miro AI Clustering；Gemini Notebook；ChatGPT/Claude | 建議 Highlight、Summary、Cluster、Counterexample、Open Question，並連結 Source。 | Theme Meaning、Evidence Strength、Dissent、Bias、Translation、Saturation。 | Evidence Matrix、Findings、Limitations。 |
| **Step 4 — 轉成設計輸入** | Designer 把已驗證 Finding 轉為 Need、Task、Scenario、Acceptance Risk。 | Figma/FigJam；Miro；Confluence/Rovo；Copilot Pages | 草擬 Job、Opportunity、User Story、Edge Case、Research-to-requirement Link。 | Priority、Feasibility、每項 Requirement 的 Insight 根據。 | 可追溯 Design Brief。 |

**3A × 3K：** Adapt 加入有版本的 Coding Framework 及 Prompt/Evidence Schema；Adept 可持續分類已核准 Feedback，但必須保留 Traceability，並將 Low-confidence/Outlier Evidence 提交人手 Review。

### 4.3 Prototype 原型——由證據建立 Flow、Wireframe 及 Connected Screens

| Step | Context 及 Designer 直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 同步最新 Context** | Designer 取得最新 Research、PRD、Policy、Design System Guidance。 | Confluence + Rovo；ChatGPT/Claude Connector；Copilot；Gemini Notebook；Figma Agent MCP Connector | 只摘要最新已核准內容，列出 Conflict，附 Citation/Owner。 | 哪個 Version 有效；哪些問題須向 PO/DPO、Research、Compliance 確認。 | 有 Version ID 的 Signed Context Pack。 |
| **Step 2 — 建立 User-flow Logic** | 把 Requirement 轉為 Main Path、Alternate、Error、Empty、Timeout、Recovery Path。 | Miro AI；FigJam/Figma Agent；Claude Artifacts；ChatGPT Visual Surface | 生成可編輯 Horizontal Flowchart，指出 Missing State/Decision Branch。 | Information Architecture、Decision Logic、Risk、User-control Point。 | 已核准 User-flow Diagram。 |
| **Step 3 — 逐個建立 Wireframe Screen** | 根據已核准 Flow 每個 Node 逐一建立 Screen。 | Figma Agent；Figma Design；Miro Prototype；Figma Make；Replit Canvas | 使用 Canonical Component 草擬 Screen、Content Alternative、Layout Variation、Responsive Direction。 | Screen Hierarchy、Task Clarity、Component Choice、Disclosure、Cognitive Load。 | 與 Flow Node 相連的編號 Lo-/Mid-fi Wireframe。 |
| **Step 4 — 連接及 Review 全圖** | 把全部 Wireframe 連成 Interaction Map，與 PO/DPO End-to-end Review。 | Figma **Add Interactions with AI**；Figma Prototyping；Figma Make | 加入基本 Connection，提示 Unreachable Screen、Missing Back Path、Inconsistent Label。 | Flow 是否解決 User Need、Operational/Regulatory Constraint。 | Connected Prototype Map 及 Gap Log。 |
| **Step 5 — 加入 Asset 及 Content** | 只加入真實測試所需 Image/Copy。 | Figma Replace/Rewrite/Translate/Shorten；GPT Image 2；Figma Make/Edit Image；Weave Tools | 產生 Placeholder Image、UX Copy Alternative、Translation、Asset Variation。 | Product Truth、Brand、Rights、Representation、Locale、Legal Wording。 | Test-ready Content 及 Asset Provenance。 |
| **Step 6 — 初步 Accessibility Review** | 在測試前檢查 Design-level Risk。 | Stark Sidekick；Figma Inspection；已核准 Contrast/Token Tool | 提示 Contrast、Typography、Alt-text 及其他可能問題。 | Acceptance；Focus、Reading Order、Zoom、Motion、Cognition 的 Manual Assessment。 | Accessibility Issue Log 及 Remediation Plan。 |

### 4.4 Pilot 試行——以真實使用者及受控操作情境驗證

| Step | Context 及直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 準備** | 定義 Task、Participant、Device、Assistive Technology、Risk Scenario。 | Maze；UserTesting；ChatGPT/Claude/Gemini/Copilot | 草擬 Task Wording、Test-data Matrix、Note Template；提示可能 Bias。 | Recruitment、Accessibility Coverage、Test Fidelity、Stop Rule。 | Pilot Protocol。 |
| **Step 2 — 執行** | 觀察使用者在 Connected Prototype 的 Task Completion 及 Recovery。 | Figma Prototype/Make；Maze；UserTesting | Capture Path、Transcript、Follow-up、支援的 Behavioral Evidence。 | 何時 Probe/Stop/保護 Participant；Severity、Root Cause。 | Session Evidence。 |
| **Step 3 — 分析** | Triangulate 使用者做了甚麼、說了甚麼及不能從何處復原。 | Dovetail AI；Maze Theme；UserTesting AI Summary；ChatGPT/Claude | 產生 First-pass Summary、Theme Candidate、Clip、Contradiction List。 | Finding Validity、Priority、Bias、Subgroup Harm、Go/No-go。 | 有 Evidence Trace 的 Pilot Report。 |
| **Step 4 — Close the Loop** | 更新 Flow、Screen、Decision Log。 | Figma；Confluence/Rovo；Copilot Pages | 草擬 Change Log，把每個 Issue Map 到已修改 Node/Screen。 | 哪項修改回應證據；是否需要 Retest。 | Revised Prototype 及 Signed Decision Record。 |

### 4.5 Production 生產——交付可測試 Design Contract 並安全實作

| Step | Context 及直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 準備 Design Contract** | 標示 Approved Frame，文件化 Component、Token、State、Content、Breakpoint、Accessibility Note。 | Figma Dev Mode；Code Connect；Confluence；Storybook | Figma Text AI 改善 Description Draft；Rovo/Copilot/ChatGPT/Claude 依 Template 產生文件草稿。 | Completeness、Canonical ID、State Behaviour、Acceptance Criteria。 | Versioned Handoff Contract。 |
| **Step 2 — Implementation** | Engineer 把 Structured Design/Component Context 引入 Approved Repository。 | Figma MCP；Codex；Claude Code；Gemini Code Assist；已核准 Replit Agent | 草擬 UI Code/Test、Reuse Mapped Production Component、解釋 Diff。 | Architecture、Security、Data Handling、Performance、Merge Decision。 | Reviewed Pull Request。 |
| **Step 3 — 驗證 Component/Visual** | 隔離測試全部 State，將 Rendered Output 與 Approved Baseline 比較。 | Storybook；Chromatic Visual Tests；Stark；CI | 建立 Test Draft、提示 Visual Change、Accessibility Candidate。 | Change 是否有意；Rendered UI 是否通過 Acceptance。 | Component/Visual/Accessibility Evidence。 |
| **Step 4 — 安全 Release** | 執行 Localization、Telemetry、Security、Performance、Accessibility、Rollback Check。 | 現有 CI/CD、Monitoring；Agent 只作 Bounded Support | 草擬 Release Note、摘要 Evidence、提示 Missing Approval。 | Canary Exposure、Production Release、Stop/Rollback、Incident Owner。 | Signed Release Candidate 及 Audit Trail。 |

### 4.6 Observe 觀察——把 Telemetry 及 Feedback 轉成已驗證 Insight

| Step | Context 及直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 驗證 Instrumentation** | 確認 Taxonomy、Consent、Identity Assumption、Schema、Missing/Duplicate Event、Metric Owner。 | GA4；BigQuery；Approved Analytics Stack | 草擬 SQL 或 Tagging QA Check。 | Metric Definition、Data Quality、Lawful Collection。 | Instrumentation QA Record。 |
| **Step 2 — Detect / Explore** | 一併 Review Product Behaviour、Feedback、Complaint、Incident。 | Gemini in BigQuery/Looker；Dovetail Channels；UserTesting；ChatGPT/Claude File Analysis | 找出 Anomaly、Segment Candidate、Common Feedback、Possible Explanation。 | Observation 是否真實、重大、可行動；Correlation vs Causation。 | 有 Supporting Evidence 的 Validated Observation。 |
| **Step 3 — Route Action** | 把 Insight 連到 Affected Flow、Screen、Component、Owner、Risk。 | Confluence/Rovo；Copilot Pages；Figma；Jira | 草擬 Issue、Affected-state List、Evidence Summary。 | Priority、Response、Incident Escalation、是否需新 Research。 | Traceable Action Recommendation。 |

### 4.7 Optimize 優化——透過有效 Experiment 及 Guardrail 改善

| Step | Context 及直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 定義 Hypothesis** | 寫明 Evidence、Target Behaviour、Primary Metric、Guardrail、Subgroup Check、Stopping Rule。 | Copilot Pages；ChatGPT/Claude/Gemini；Confluence | 批判 Logic、列出 Confound、草擬 Preregistration。 | Test 是否合乎倫理、具有足夠 Power 及價值。 | Approved Experiment Plan。 |
| **Step 2 — 生成受限 Variant** | 只生成由 Hypothesis 支持、符合 Canonical System 的 Variant。 | Figma Agent；Figma Make；Figma Weave；GPT Image 2；Miro AI | 產生 Layout、Interaction、Content Treatment Alternative。 | Variant 是否 Coherent、Accessible、Non-manipulative、On-brand。 | 可 Review Variant Set。 |
| **Step 3 — 執行／分析** | 透過 Approved Experiment Platform 執行，監察 Guardrail。 | Analytics Stack；BigQuery/Looker Assistance | 草擬需 Review Query、檢查 Anomaly、摘要 Result。 | Power、SRM、Multiple Comparison、Causality、Subgroup Disparity、Rollback。 | Validated Experiment Result。 |
| **Step 4 — 保存 Learning** | 更新 Design、Evidence、Decision Record。 | Figma；Storybook；Confluence/Rovo；Dovetail | 草擬 Change/Learning Record。 | Ship、Iterate、Reject 或 Retest。 | Versioned Learning 及 Approved Change。 |

### 4.8 Scale 規模化——制度化 Knowledge、Component 及 Governed Agent

| Step | Context 及直接操作 | Product / Surface | AI may assist | Human must decide | 核准輸出 |
|---|---|---|---|---|---|
| **Step 1 — 管理 Canonical Source** | 為 Research、Policy、Component、Code Asset 指定 Owner、Version、Expiry、Permission、Deprecation Status。 | Confluence/Rovo；Dovetail；Figma Libraries；Storybook；Git | 偵測 Missing Metadata、Stale Content、Conflict。 | Canonical Status 及 Remediation Owner。 | Governed Source Inventory。 |
| **Step 2 — 封裝 Reusable Assistance** | 把 Approved Prompt、Instruction、Schema、Example、Evaluation Case 存於 Vendor Chat 以外。 | ChatGPT Projects/Agents；Claude Projects/Connectors；Gemini/Gems；Copilot Agents；Rovo Agents | 由 Governed Configuration 部署 Bounded Role Assistant。 | Scope、Permission、Supported Task、Escalation、Release Version。 | Versioned Assistant Package。 |
| **Step 3 — 選擇性連接系統** | 先加入 Read-only Connector；只在證實價值及 Control 後才加入 Action。 | Figma MCP；Rovo；Copilot Studio；Claude MCP；OpenAI Connectors/Agents；Miro MCP | Retrieve Approved Context、草擬 Change、開啟可 Review Proposal。 | 可存取／修改哪些 System；Confirmation 及 Rollback Design。 | 有 Log 的 Least-privilege Integration。 |
| **Step 4 — 評估及營運** | 監察 Quality、Accessibility、Retrieval Drift、Incident、Latency、Cost、Human Override。 | Vendor Eval/Observability + Internal Dashboard | 運行 Test Set、提示 Drift、摘要 Operational Evidence。 | Promotion/Downgrade、Suspension、Vendor Exit、Competency Requirement。 | Revalidation 及 Operating Record。 |

---

## 5. 3A × 3K 在整個 Workflow 的應用

| 成熟度 | Know-how 執行 | Know-what 判斷 | Know-where 情境／Routing | 常見工具組合 |
|---|---|---|---|---|
| **Adopt** | 用一個已核准 Assistant 完成 Bounded Task；檢查來源、修改輸出、記錄 Tool/Reviewer。 | 選擇 Blast Radius 低、容易驗證的任務；知道何時不需要 AI。 | D0–D1 只進入 Approved Enterprise Account；人手把核准 Artifact 放回 System of Record。 | Copilot/ChatGPT/Claude/Gemini 草擬；Figma AI 處理 Bounded Canvas Work；Dovetail/Maze 作 First-pass Analysis。 |
| **Adapt** | 使用 Source Pack、Template、Schema、Prompt Release、Canonical Component ID、Repeatable Evaluation。 | 判斷哪些 Context 提升質素，哪些增加 Privacy、Injection、Cognitive-load Risk。 | 只連接 Approved Source；使用有 Version 的 Manifest、Owner、Expiry、Permission-aware Retrieval。 | Rovo/Notion/Notebook 作 Governed Retrieval；Figma Agent/Make 使用 Design System Context；Storybook/Code Connect 作 Implementation Contract。 |
| **Adept** | 操作已評估 Agent，跨系統 Retrieve/Propose Change；檢查 Log；測試 Rollback/Exception Path。 | 只有在自動化改善已驗證 User/Business Outcome 且不削弱 Guardrail 時才重設流程。 | 在 Approved Environment 使用 Least-privilege Action；重大修改前 Human Confirmation；保留 Vendor-exit Path。 | 選擇性使用 Copilot Studio、Enterprise Gemini、Approved OpenAI/Anthropic Agent、Coding Agent、Figma/Miro MCP、CI。 |

### Promotion Rule

Workflow 只有在具備以下證據時才可升級：至少兩個 Repeatable Cycle、Named Owner、External Versioned Configuration、Representative Evaluation、Controlled Data Routing、Measured Benefit、沒有重大 Accessibility/Privacy/Safety Loss，以及已測試 Fallback。Vendor Feature 由 Beta 轉 GA 不會自動提升 Workflow 成熟度。

---

## 6. HSB Design Context 建議 Tool Stack

此建議保留既有偏好——**Figma、Confluence、Storybook、Copilot、GPT、Claude、Gemini**——只在清楚解決 Gap 時加入 Specialist Tool。

### 6.1 Core Stack

| 需要 | 建議 Core | 確切用途 |
|---|---|---|
| Central Knowledge | **Confluence + Rovo** | Design/Research/Decision Page 的 System of Record；具 Owner、Metadata、Review Date；Permission-aware Search/Chat；Design Knowledge Agent 必須經評估。 |
| Daily Enterprise Assistant | **Microsoft 365 Copilot** | 在獲授權 Word、PowerPoint、Excel、Outlook、Teams、SharePoint Context 工作；以 Copilot Pages 保存 Collaborative Brief/Decision。 |
| Deep Reasoning / Challenger | **ChatGPT Work + Claude for Work + Managed Gemini** | 高影響工作使用一個 Primary Model 加一個受控 Challenger；禁止把相同 D2/D3 資料貼進未核准 Consumer Account。 |
| Design / Prototyping | **Figma Design + Figma Agent + Figma Make** | Context Sync → Flow → Screen-by-screen Wireframe → Connection Map → Functional Prototype；全部 Map 回 Canonical Component 並由 Designer Review。 |
| Media Exploration | **Figma Weave / Weave Tools** | 使用 Cleared D0 Asset 生成 Visual Variant、Mockup、Style/Palette/Lighting/Background；使用前經 Brand/Legal Approval。 |
| Handoff / Component Truth | **Figma Dev Mode + Code Connect + Storybook** | 把 Figma Component Map 到 Production Component；文件化全部 State；保持 Design/Code Reference 對齊。 |
| Implementation Assistance | **Codex、Claude Code 或 Gemini Code Assist** | 選擇 Repository 已核准 Coding Agent；草擬 Implementation/Test、檢查 Diff、Human Merge。 |
| Visual Regression | **Chromatic + Storybook** | 把 Component Screenshot 與 Approved Baseline 比較，Review 所有 Intentional Change。 |

### 6.2 經 Security、Privacy、Procurement Review 後的 Optional Specialist Tool

| Gap | 可選工具 | 加入原因 |
|---|---|---|
| Research Repository / Evidence Traceability | **Dovetail AI** | Transcript、Highlight、Theme、Source Workflow 比 General Chatbot 完整。 |
| Remote Testing / Adaptive Follow-up | **Maze AI** 或 **UserTesting** | 加入 Participant Workflow、Behavioral Evidence、Test-specific Analysis。 |
| Workshop Synthesis / Editable Diagram | **Miro AI** | Research Wall、Flow、Collaborative Diagram 均可直接編輯。 |
| Design-stage Accessibility | **Stark Sidekick** | 及早提示 Candidate Issue；補充而非取代 Rendered/Manual Testing。 |
| Alternative App Prototype | **Replit Agent / Design Canvas** | 當 Figma Make 不是 Approved Route 時作 Functional Exploration；仍需 Production Review。 |
| Alternative Knowledge Environment | **Notion AI Enterprise Search** | 只在 Notion 已被採用及核准時考慮；避免把 Confluence 複製成第二個無管控 Source of Truth。 |

### 6.3 避免 Tool Sprawl

不應把 Catalogue 中全部工具一次過採購。每個 Capability Lane 應選擇：

1. 一個 Canonical System of Record。
2. 一個 Default Enterprise Assistant。
3. 在有理據的高影響工作使用一個 Challenger Model。
4. 一個 Primary Design/Prototype Surface。
5. 一套 Research-testing Stack。
6. 一條 Approved Coding-agent Route。
7. 一條 Validation/Release Evidence Path。

每個 Alternative 都要記錄：為何需要、可接收哪類資料、Owner 是誰、如何量度質素，以及離場時如何 Export/Delete Content。

---

## 7. Mandatory Workflow Controls 必要控制

### 7.1 Source Freshness Record

每項 AI 使用的來源需要：Source ID/Title、Owner、Canonical URI/System、Imported Timestamp、Authoritative Last-update Timestamp、Sync State、Expiry/Review Date、Permitted Use/Data Class、Conflict/Revocation Status。Stale、Unowned、Failed-sync 或 Revoked Content 必須停止用於決策。

### 7.2 Human Gates

| Gate | 時間 | 所需證據 | Stop Condition |
|---|---|---|---|
| **G0 — Pre-use** | 任何工具接收資料前 | Product/Edition/Status、Account、Data Class、Region、Retention/Training Terms、DLP/IAM、IP、Vendor Owner、Fallback。 | Personal/Unpaid Route 處理銀行資料；Terms/Status/Owner 不明。 |
| **G1 — Research/Data Ingestion** | Note、Recording、Internal Source 進入 AI 前 | Consent/Lawful Basis、Minimization、Reuse、Translation、Deletion Lineage、Source Freshness、Connector Threat Model。 | Consent/Purpose 不清；Stale Source；Deletion 無法傳播。 |
| **G2 — Pre-pilot** | 接觸 Controlled User 前 | Participant/Device/AT Plan、Prototype Fidelity、Severity Model、Log/Retention、Stop Rule。 | 沒有 Real-user Plan；AI-only Evaluation；未核准 D2/D3 或 Beta Use。 |
| **G3 — Pre-production** | Release 前 | Design Contract、Security/Accessibility/Localization Evidence、Telemetry QA、Inventory、Canary、Kill Switch、Rollback、On-call。 | Rollback 未測試；沒有 Owner；Critical Test 失敗。 |
| **G4 — Operate/Revalidate** | 定期及 Trigger 時 | KPI、Incident、Drift、Source/Model/Status、Access、Cost、Vendor-exit Evidence。 | Evaluation 失敗、Material Harm、Stale Source、Access Incident、Policy Change。 |

### 7.3 Universal Checklist

- [ ] 清楚寫明 Task、User、Decision、Constraint、Output Schema。
- [ ] 分類資料並確認 Approved Account、Region、Retention、Product Status。
- [ ] 只附加通過 Source Manifest 的內容。
- [ ] 把 Trusted Instruction 與 Retrieved/User-controlled Data 分開。
- [ ] 使用 Source/Tool Allowlist、Minimum Scope、Read-only Connector Default。
- [ ] 要求 Citation/Evidence ID、Uncertainty，並打開原始 Source。
- [ ] 保留 Outlier、Contradiction、Unknown，避免 AI 把它們「平均化」。
- [ ] 測試 Happy、Empty、Error、Loading、Timeout、Refusal、Recovery、Escalation State。
- [ ] 測試 Language、Literacy、Disability、Device/Connectivity、Bias、Representational Harm。
- [ ] 記錄 Product、可見 Model、Configuration、Prompt/Instruction Release、Source、Reviewer、Decision。
- [ ] 保留 Manual Fallback；Evidence 過期、Consent 不清或 Risk 超出 Approval 時立即停止。

### 7.4 Accessibility Boundary

AI 及 Automated Scanner 可提示 Candidate、草擬 Alt Text 或建議 Fix。Conformance 必須以 Rendered Product 配合 Expert/Manual Testing：Keyboard/Focus、Screen Reader、Zoom/Reflow、Contrast、Motion、Input/Error Recovery、Cognitive Comprehension、Localization 及代表性 Disabled-user Research。任何 LLM、Figma Feature、Stark Scan、Lighthouse Result 或 Model Score 都不能單獨證明 Accessibility Conformance。

---

## 8. KPI 及 Evaluation Framework

| 維度 | Measures | Guardrail |
|---|---|---|
| Efficiency | Brief-to-flow Time、Documentation Lead Time、Component Retrieval Time、Handoff Rework | 必須計 Human Review Time 及 Correction Cost。 |
| Evidence Quality | Citation Accuracy、Source-freshness Pass、Quote Fidelity、Dissent Retention、Translation Defect | Source/Consent Lineage 不完整時禁止發布。 |
| Design Quality | Canonical Component Use、State Coverage、Drift Defect、Visual-regression Failure、Localization Defect | AI Output Volume 不是成功。 |
| Accessibility / Inclusion | Manual AT Defect、Subgroup Task Parity、Comprehension、Motion/Zoom/Reflow Failure | Automated/Model Score 不是 Conformance Evidence。 |
| User Outcome | Task Success、Error Recovery、Comprehension、Trust、Complaint/Escalation、Long-term Harm | 在合法情況下負責任地 Segment；不可只優化 Conversion。 |
| AI Reliability | Unsupported Claim、Grounded-answer Rate、Tool-call Failure、Refusal Quality、Latency、Drift | Model-based Evaluation 必須與 Human Expert 校準。 |
| Governance | Approved-tool Use、DLP/Privacy Incident、Traceability、Stale Source、Gate Coverage | Governance 是基本要求，不代表已達 Adept。 |
| Operations / FinOps | Rollback Success/Time、RTO/RPO、Alert Quality、Cost per Validated Outcome、Export/Decommission Test | 包括 Vendor Switching 及 Deletion Cost。 |
| Human Capability | Edit Quality、Rejection/Override Decision、Escalation、Scenario Assessment | Prompt Count 及 Raw Usage 不是良好 Competency Measure。 |

---

## 9. 實施次序

| 時間 | 目標 | Action | Exit Evidence |
|---|---|---|---|
| **0–30 日** | Governed Baseline | 核准 Core Stack、D0–D3 Matrix、System Owner、Source Manifest、Prompt/Output Checklist；Map Figma ↔ Storybook Component ID。 | G0 運作、Owner 受訓、Baseline 已量度、Fallback 已文件化。 |
| **31–90 日** | Adopt | Pilot 兩項 Low-risk Task：Evidence-to-flow、Figma-to-design-documentation；只在 Allowed Data 使用 Managed Copilot/ChatGPT/Claude/Gemini/Figma AI。 | 兩個 Traceable Cycle、Time/Quality 有改善、沒有 Material Guardrail Loss。 |
| **3–6 個月** | Adapt | 加入 Governed Rovo Retrieval、Reusable Research/Design Template、Dovetail/Testing Integration、Design-system-aware Figma Workflow、Coding-agent Test Set。 | Versioned Configuration、Representative Evaluation、Named Owner、Validated Benefit。 |
| **6–18 個月** | Selective Adept | 先加入 Read-only Agent/MCP，再加入 Tightly Bounded Action；Monitoring、Confirmation UX、Red-team Test、Canary、Rollback、FinOps、Vendor Exit。 | G3/G4 通過、持續 User/Business Improvement、Recovery 已測試。 |

**建議目標：** Selective Adept，而非 Maximum Automation。Research Interpretation、Accessibility Acceptance、Regulated Content、Causal Analysis 及 Irreversible Release Decision，在由人處理更安全時便應保持 Human-led。

---

## 10. 官方來源索引

### OpenAI

- [OpenAI Developer 及產品文件](https://developers.openai.com/)
- [GPT Image 2](https://developers.openai.com/api/docs/models/gpt-image-2)

### Anthropic

- [Claude Artifacts](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them)
- [Claude Projects](https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects)
- [Claude Custom Connectors / Remote MCP](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp)
- [Claude for Work Data Roles](https://support.anthropic.com/en/articles/9267385-does-anthropic-act-as-a-data-processor-or-controller)

### Microsoft

- [Microsoft 365 Copilot Pages](https://support.microsoft.com/en-us/microsoft-365-copilot/get-started-with-microsoft-365-copilot-pages)
- [Microsoft 365 Copilot Privacy and Protection](https://learn.microsoft.com/en-us/copilot/privacy-and-protections)
- [Microsoft 365 Declarative Agents](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-declarative-agent)
- [Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)

### Figma

- [Get Started with Figma AI](https://help.figma.com/hc/en-us/articles/24039793359767-Get-started-with-Figma-AI)
- [Use AI Tools in Figma Design](https://help.figma.com/hc/en-us/articles/23870272542231-Use-AI-tools-in-Figma-Design)
- [Explore Figma Make](https://help.figma.com/hc/en-us/articles/31304412302231-Explore-Figma-Make)
- [Use Weave Tools in Figma](https://help.figma.com/hc/en-us/articles/40779260614935-Use-Weave-tools-in-Figma)
- [Replace Content](https://help.figma.com/hc/en-us/articles/23796390206743-Replace-text-content-with-AI)
- [Rename Layers with AI](https://help.figma.com/hc/en-us/articles/24004711129879-Rename-layers-with-AI)
- [Make or Edit Images](https://help.figma.com/hc/en-us/articles/24004542669463-Make-or-edit-an-image-with-AI)
- [Add Interactions with AI](https://help.figma.com/hc/en-us/articles/24004778051479-Make-interactions-with-AI)
- [Figma MCP Server](https://help.figma.com/hc/en-us/articles/39216419318551-Get-started-with-the-Figma-MCP-server)

### Knowledge、Research、Testing、Validation

- [Atlassian Rovo](https://support.atlassian.com/rovo/docs/what-is-rovo/)
- [Notion Enterprise Search](https://www.notion.com/help/enterprise-search)
- [Dovetail AI](https://dovetail.com/help/dovetail-ai/)
- [Miro AI](https://help.miro.com/hc/en-us/articles/28765406244498-Miro-AI-overview)
- [Maze AI](https://maze.co/ai/)
- [UserTesting AI Insight Summary](https://help.usertesting.com/hc/en-us/articles/13268691111453-AI-insight-summary)
- [Stark Sidekick](https://www.getstark.co/support/getting-started/using-sidekick/)
- [Storybook Visual Tests](https://storybook.js.org/docs/9/writing-tests/visual-testing)
- [Replit Agent](https://docs.replit.com/core-concepts/agent)

### Google

- [Gemini Notebook Source Behavior](https://support.google.com/notebooklm/answer/16215270)
- [Workspace AI Privacy](https://workspace.google.com/security/ai-privacy/)
- [Gemini Enterprise Agent Platform](https://cloud.google.com/products/gemini-enterprise-agent-platform)
- [Gemini Code Assist](https://developers.google.com/gemini-code-assist/docs/write-code-gemini)
- [Gemini in BigQuery](https://docs.cloud.google.com/bigquery/docs/write-sql-gemini)

---

## Final Operating Principle 最終運作原則

Master Question 不再是「哪一個 Google AI Tool 可以生成這個 Artifact？」而是：

> **哪一個已核准的 Source、Assistant、Creation Surface、Validation Surface 及 Action Layer 組合，可以產生可追溯、可存取、可回復的設計成果——而 Accountable Human 能否提供證明？**

