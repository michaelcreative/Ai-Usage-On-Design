# Figma「Building with AI」文章整理

> Source: [Figma Building with AI Resource Library](https://www.figma.com/resource-library/building-with-ai/)  
> Reviewed: 2026-08-21  
> Language: English article titles with Cantonese / Traditional Chinese summaries

我按 Figma 官方資源庫於 **2026 年 8 月 21 日**顯示的內容，整理了以下三個分類，共 **24 篇文章**。

| 分類 | 文章數量 | 核心目的 |
|---|---:|---|
| AI tools & workflows | 21 | AI 設計工具、Prompt、Agent、MCP、Design System、測試與設計到開發流程 |
| AI research & testing | 1 | 用 AI 加速市場研究、用戶研究、競品監察及研究分析 |
| AI for product managers | 2 | 協助 PM 做 Discovery、研究、策略、PRD、優先排序及原型驗證 |

> **分類備註：** 雖然 A/B testing 和 usability testing 都屬於研究活動，但 Figma 官方目前將這兩篇文章放在 **AI tools & workflows**；正式的 **AI research & testing** 分類暫時只有一篇文章。

---

## 1. AI tools & workflows

這個分類主要說明：如何把 AI 從一次性的內容生成工具，提升為一套包含 **設計背景、Design System、Agent、MCP、測試和 Human-in-the-loop** 的工作流程。

- [Figma 官方分類頁](https://www.figma.com/resource-library/ai-tools-workflows/)

| # | Figma 官方文章 | 文章重點 | 可應用的 UX/UI 工作 | 對應 8-Stage Workflow |
|---:|---|---|---|---|
| 1 | [How to turn your design system into a Claude Skill](https://www.figma.com/resource-library/claude-skill-design-system/) | 把元件、Design Token、命名規則和使用規範寫入 **SKILL.md**，讓 Claude 不再生成偏離 Design System 的介面。 | 建立 HSB Design System AI 使用規則；要求 AI 先搜尋現有元件再建立新元件。 | Production、Scale |
| 2 | [7 of the best AI tools for graphic design](https://www.figma.com/resource-library/ai-tools-for-graphic-design/) | 比較 Figma Weave、Adobe Firefly、Midjourney、Runway、Canva、Krea、Magnific；涵蓋圖像生成、影片、放大及 Node-based workflow。 | Campaign KV、Moodboard、概念圖、視覺方向和大量品牌素材製作。 | Discover、Prototype、Production |
| 3 | [How to use visual prompt engineering with AI design tools](https://www.figma.com/resource-library/visual-prompt-engineering/) | 使用參考圖片配合文字指令；指出要保留和改變的視覺元素，再逐輪檢查輸出。 | 用現有 App／Web 畫面作 reference，指定 layout、spacing、tone、component 和不要更改的元素。 | Prototype、Pilot |
| 4 | [The AI creative process: How to ideate and refine faster](https://www.figma.com/resource-library/ai-creative-process/) | AI 創作重心由「產生一個答案」轉變為「大量探索、篩選、組合及精煉」。 | 快速生成多個方向，由設計師策展、比較及選擇最合適方案。 | Discover、Prototype |
| 5 | [What is design context in AI workflows?](https://www.figma.com/resource-library/design-context-ai/) | AI 要有品牌、用戶、產品、元件、Token、內容及程式背景，才能生成符合實際產品的設計。 | Prompt 前提供 persona、user problem、Design System、現有畫面、業務限制及成功指標。 | Discover、Research、Prototype、Production |
| 6 | [What is an agentic framework?](https://www.figma.com/resource-library/agentic-framework/) | 解釋 Agent 的規劃、推理、工具調用、記憶、協調及自我修正；涵蓋 LangGraph、CrewAI、Microsoft Agent Framework、OpenAI Agents SDK 等。 | 建立「讀取需求 → 搜尋研究 → 生成流程 → 建立 UI → QA」的多步驟 AI Loop。 | 全流程 |
| 7 | [How to create a skill in Claude Code for your design system](https://www.figma.com/resource-library/how-to-create-a-skill-in-claude-code/) | 教你建立可重用的 Claude Code Skill，讓 AI 按指定的元件、Token 和規範工作。 | 建立 **/hsb-design-review**、**/handoff-checklist** 或 **/research-synthesis** 等內部技能。 | Production、Scale |
| 8 | [Generative AI design: What it is and how to use it](https://www.figma.com/resource-library/generative-ai-design/) | 說明文字、圖像及多媒體生成如何配合 Figma Weave，在保持品牌方向下大量生產素材。 | Campaign 視覺變體、場景圖、產品素材及多渠道內容。 | Prototype、Production、Scale |
| 9 | [MCP for designers: What it is and how to use it](https://www.figma.com/resource-library/mcp-for-designers/) | MCP 讓 AI Agent 讀取 Figma 的 frame、component、variable、style 和 Code Connect，並可把結果寫回 Canvas。 | Figma ↔ Claude／Codex／Cursor；設計搜尋、元件重用、Design QA、設計到程式同步。 | Prototype、Production、Scale |
| 10 | [10 Claude Skills for design to add to your workflow](https://www.figma.com/resource-library/claude-skills-for-design/) | 介紹 **/figma-use**、**/figma-generate-design**、**/audit-design-system**、**/create-voice**、**/sync-figma-token** 等 Skills。 | 生成畫面、Design System Audit、Token 同步、無障礙規格及設計交付。 | Prototype、Production、Scale |
| 11 | [How to start vibe coding](https://www.figma.com/resource-library/how-to-start-vibe-coding/) | 由自然語言需求開始，讓 AI 建立 App，再透過提示、視覺編輯和測試逐步改善。 | 設計師／PM 在沒有完整工程資源前建立可互動 PoC 或 MVP。 | Prototype、Pilot |
| 12 | [15 of the best AI coding tools and assistants for developers](https://www.figma.com/resource-library/ai-coding-tools/) | 比較 AI Coding Assistant、Agent、IDE、Prompt-to-code 和設計到程式工具。 | 與工程團隊評估 Figma Make、Claude Code、Cursor 等工具的 handoff 和 prototype 能力。 | Prototype、Production |
| 13 | [11 of the best workflow design tools for product teams](https://www.figma.com/resource-library/workflow-design-tools/) | 比較流程圖、協作白板、工作管理及自動化工具；強調 FigJam 的共同建構能力。 | User Flow、Service Blueprint、AI Agent Flow、Stakeholder Alignment。 | Discover、Research、Prototype |
| 14 | [7 AI for A/B testing tools to ship winning designs](https://www.figma.com/resource-library/ai-for-ab-testing-tools/) | 建議流程：標準化 Design System → 用 Figma Make 建立變體 → 接駁實驗平台 → 設定指標及 Guardrails。 | 快速建立實驗方案；比較 Optimizely、Statsig、AB Tasty、Eppo、VWO、Kameleoon。 | Pilot、Observe、Optimize |
| 15 | [AI usability testing guide: Modern workflow and tools](https://www.figma.com/resource-library/ai-usability-testing/) | 把研究由設計後的單次活動，轉變為持續測試、快速整理及反覆驗證的循環。 | AI 協助測試計劃、訪談整理、行為分析、問題分類及洞察綜合；研究員負責確認證據。 | Research、Pilot、Optimize |
| 16 | [5 of the best AI product design tools for 2026](https://www.figma.com/resource-library/ai-product-design/) | 比較 Figma Design、Figma Make、Relume、Visily、Midjourney，並說明如何建立可擴展的 AI Design Stack。 | 由概念、IA、Wireframe、UI 到 Prototype 的工具選擇。 | Discover、Prototype |
| 17 | [7 of the best AI app builders for 2026](https://www.figma.com/resource-library/ai-app-builders/) | 比較 Figma Make、Replit、Lovable、FlutterFlow、Softr、Bubble、Anything。 | 建立高擬真 Prototype、內部工具、Dashboard 或 MVP，及測試產品概念。 | Prototype、Pilot |
| 18 | [Top AI tools for UX designers in 2026](https://www.figma.com/resource-library/ai-tools-for-ux-designers/) | 比較 Figma Make、Figma Design、Uizard、Stitch、Jasper、Firefly、Attention Insight、UX Pilot、Khroma。 | Wireframe、UI、UX Copy、視覺注意力預測、色彩探索及 Prototype。 | Research、Prototype、Pilot |
| 19 | [AI in design: Transforming the way we create](https://www.figma.com/resource-library/ai-in-design/) | 概覽 AI 在 layout、圖像、wireframe、prototype、創意探索及重複工作自動化的用途，同時討論一致性與人工判斷。 | 適合作為設計團隊的 AI 基礎教育或 AI 101 閱讀材料。 | 全流程 |
| 20 | [11 of the best AI design tools for 2026](https://www.figma.com/resource-library/ai-design-tools/) | 比較 Figma、Canva、Firefly、Microsoft Designer、Midjourney、Stable Diffusion、Uizard、Synthesia、Runway、Magic Hour、Lummi。 | 根據 UI、圖像、影片、Marketing Asset 和 Prototype 任務選擇工具。 | Discover、Prototype、Production |
| 21 | [How to use AI to create a website](https://www.figma.com/resource-library/how-to-use-ai-to-create-a-website/) | Prompt → 生成版面 → 套用品牌及真實內容 → Responsive 測試及調整。 | Campaign Landing Page、產品頁、Portfolio、活動網站及快速概念驗證。 | Prototype、Pilot、Production |

---

## 2. AI research & testing

Figma 目前在這個正式分類下只有一篇文章，但內容涵蓋三種研究工作：**User Research、Consumer/Trend Research、Competitive Research**。

| # | Figma 官方文章 | 工具與用途 | 建議研究流程 | 對應 8-Stage Workflow |
|---:|---|---|---|---|
| 1 | [11 AI market research tools for modern product teams](https://www.figma.com/resource-library/ai-market-research-tools/) | **Figma Make**：研究洞察轉 Prototype；**Maze**：Usability Test；**Looppanel**：訪談轉錄及標籤；**Dovetail**：Research Repository；**UserTesting**：用戶測試與洞察；**Quantilope**：大型量化研究；**Glimpse**：趨勢分析；**Remesh**：即時定性研究；**Crayon／Visualping／Klue**：競品監察。 | 收集資料 → 轉錄及分類 → 找出 Pattern → 建立洞察 → 生成研究支持的 Prototype → 用戶驗證 → 把結果存入研究知識庫。 | Discover、Research、Prototype、Pilot、Observe |

### 11 個工具快速比較

| 研究類型 | 工具 | 最適合用途 | 主要 AI 能力 |
|---|---|---|---|
| Prototype | Figma Make | 把研究結果轉成高擬真 Prototype | Prompt-to-design、快速產生多個方案 |
| User research | Maze | Usability Testing | Figma Prototype 測試、訪談、測試結果 |
| User research | Looppanel | Interview synthesis | 多語言轉錄、Auto-tagging、可搜尋 Repository |
| Research repository | Dovetail | 集中管理研究資料 | Feedback 分析、主題分類、Dashboard |
| User testing | UserTesting | 即時用戶回應 | AI Insight Synthesis、企業級研究服務 |
| Quantitative research | Quantilope | 大型問卷及統計 | Automated Tracking、Research Copilot |
| Trend research | Glimpse | 消費者及市場趨勢 | Trend Tracking、Benchmark、Forecast |
| Qualitative research | Remesh | 大規模即時對話 | Real-time probing、Sentiment Analysis |
| Competitive research | Crayon | 競品市場變化 | 競爭情報及內容監察 |
| Competitive research | Visualping | 網頁和視覺改動監察 | 自動 Alert、圖像差異分析 |
| Competitive research | Klue | 競品知識庫 | Win-loss Analysis、Compete Agent、Battlecards |

---

## 3. AI for product managers

這個分類重點是將 AI 放入完整產品週期，而不只是用 Chatbot 寫文件。

| # | Figma 官方文章 | 文章重點 | PM／UX/UI 實際用途 | 對應 8-Stage Workflow |
|---:|---|---|---|---|
| 1 | [AI for product managers: 13 top tools + practical tips](https://www.figma.com/resource-library/ai-for-product-managers/) | AI 可支援 Discovery、策略、數據分析及執行；比較 Figma Make、ChatGPT、Productboard、Mixpanel、Dovetail、Linear、Fireflies、ChatPRD、Lovable、Zeda.io、Motion、Bolt、Vercel。 | 訪談綜合、Feedback Prioritization、Roadmap、PRD、User Story、數據查詢、Meeting Summary、Prototype 和 MVP。 | Discover、Research、Prototype、Production、Observe、Optimize |
| 2 | [How to use AI for product design: 7 use cases](https://www.figma.com/resource-library/ai-for-product-design/) | 七個用途包括研究分析、概念創作、Prototype、Usability Validation、Personalization、生產優化及 Lifecycle／Sustainability。亦提供 Figma Make 六步流程。 | 從研究資料建立 Persona／Journey → 生成多個方案 → 建立互動 Prototype → 測試 → 修改 → 移回 Figma Design 完成設計。 | Discover、Research、Prototype、Pilot、Production、Optimize |

### 13 個 PM 工具分工

| 工作範圍 | 建議工具 | 主要用途 |
|---|---|---|
| Rapid Prototype | Figma Make | Prompt-to-prototype、即時修改、Design System Context |
| Brainstorming／Drafting | ChatGPT | 構思、文件初稿、資料分析、Custom GPT |
| Feedback Prioritization | Productboard | Feedback clustering、PRD 草稿、Customer Insight |
| Product Analytics | Mixpanel | 自然語言查詢、異常偵測、指標解釋 |
| Qualitative Research | Dovetail | 轉錄、Research Repository、Theme Clustering |
| Delivery Management | Linear | Issue、Sub-issue、Duplicate Detection、Slack Input |
| Meeting Documentation | Fireflies.ai | Transcript、Summary、Action Items |
| PRD／Requirements | ChatPRD | PRD 草擬、Logic Audit、多文件 Context |
| Functional MVP | Lovable | Full-stack MVP、GitHub Sync、視覺修改 |
| Strategy | Zeda.io | Opportunity、Revenue Impact、Release Notes |
| Scheduling | Motion | 自動排程、Project Risk Alert |
| Rapid Build | Bolt | Prompt-to-code、快速 Web Prototype |
| Deployment | Vercel | Preview、部署及產品交付 |

---

## 對 HSB UX/UI AI Adoption 最重要的 6 個結論

| 優先方向 | Figma 文章帶出的做法 | HSB 建議 |
|---|---|---|
| 1. AI 必須有 Design Context | 提供品牌、用戶、產品、元件、Token 和限制 | 不要只輸入「建立信用卡頁面」；要同時提供 Design System、目標客群、流程、法規內容及成功指標。 |
| 2. Design System 要 AI-ready | 使用清晰元件、Variable、Token、Code Connect 和 Skill | 先整理元件命名及規範，再嘗試 Figma MCP／Agent 自動化。 |
| 3. AI 用於探索，人類負責選擇 | AI 產生多個方案，設計師策展及驗證 | AI 可以做 First Draft，但 UX、Accessibility、Brand、Compliance 仍由人批准。 |
| 4. Research 要形成持續循環 | Research → Prototype → Test → Insight → Iteration | 將訪談、UT、GA4 和 Session Replay 串成 Observe／Optimize Loop。 |
| 5. Agent 從小型工作開始 | 先執行 bounded、可驗證的任務 | 先做 Layer Naming、Copy Draft、Design System Audit、Research Synthesis；不要一開始全自動發布。 |
| 6. 測試需要 Guardrails | 先定義指標、品牌及 UX 限制 | A/B Test 除 Conversion 外，同時監察 Error、Complaint、Accessibility、Trust 和 Compliance。 |

---

## Bank governance note

上述第三方工具不等於已獲公司批准。任何 Customer Data、訪談錄音、銀行內部文件或未公開設計，都應先通過 Information Security、Privacy、Legal 和 Procurement 審批；AI 輸出亦要保留來源、人工覆核及決策紀錄。

---

## Preferred 8-Stage UX/UI Product Design Lifecycle

1. Discover
2. Research
3. Prototype
4. Pilot
5. Production
6. Observe
7. Optimize
8. Scale
