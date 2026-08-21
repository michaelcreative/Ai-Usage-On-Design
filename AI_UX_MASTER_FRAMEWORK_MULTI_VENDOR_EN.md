# AI Usage in the Design Workflow — Multi-Platform Master 3A × 3K Framework

**Final draft:** 2026-08-21  
**Lifecycle:** Discover → Research → Prototype → Pilot → Production → Observe → Optimize → Scale  
**Framework:** 3A AI Maturity × 3K Knowledge Dimensions  
**Primary context:** UX/UI product design in a regulated bank  
**Scope:** Google, Figma, OpenAI, Anthropic, Microsoft, Atlassian and selected specialist UX platforms

---

## 1. Executive summary

This is the vendor-neutral master version. The earlier Google-only framework remains useful as a Google ecosystem deep dive, but a real design workflow should select tools by task, evidence quality, system integration and risk—not force one vendor into every step.

- **3A measures operating maturity.** **Adopt** integrates approved assistance; **Adapt** standardizes and customizes a repeatable workflow; **Adept** redesigns work around evaluated, observable and reversible automation.
- **3K measures practitioner knowledge.** **Know-how** is execution skill; **Know-what** is strategic judgment; **Know-where** is correct contextual application, sourcing and data routing.
- A product may contain an autonomous agent while the organization is still only at **Adopt**. Maturity depends on governance, repeatability, evaluation, ownership and measured outcomes—not product marketing.
- The preferred architecture separates the **system of record**, **AI reasoning assistant**, **creation surface**, **validation surface** and **action layer**. One product should not silently become all five.
- AI can accelerate evidence handling, divergent exploration, documentation, prototype construction, test analysis and code drafting. Humans retain accountability for research consent, problem framing, design decisions, accessibility acceptance, model-risk thresholds and production release.

> **Human-accountability rule:** AI may propose, summarize, generate, compare or flag. The named designer, researcher, analyst, engineer or product owner verifies the evidence and owns the decision.

### 1.1 3A maturity definition

| Level | Operating definition | Evidence required | Does not prove maturity |
|---|---|---|---|
| **Adopt — integrate** | Approved, off-the-shelf AI assists bounded and reversible tasks; a person transfers context and approves each output. | Named use case, trained users, baseline, review checklist, manual fallback. | Using a powerful model; generating many artifacts. |
| **Adapt — customize** | Teams use governed source packs, reusable instructions, schemas, rubrics, connectors or design-system context. | Versioned configuration, owner, representative test set, controlled data routing, measured gain. | A one-off custom prompt, Project, Gem or template without lifecycle control. |
| **Adept — master/innovate** | Evaluated automation coordinates approved systems with observability, least privilege and human-controlled release. | Production evaluation, logs, drift/cost monitoring, confirmation points, rollback and demonstrated user benefit. | An unattended prototype or broad deployment without evidence. |

### 1.2 3K knowledge definition

| Dimension | Required question |
|---|---|
| **Know-how** | Can the designer execute the task, inspect the evidence, edit the artifact and recover from failure? |
| **Know-what** | Can the designer identify the right problem, required human judgment, risk and success evidence? |
| **Know-where** | Can the designer route each input and output to the approved account, source, system of record and decision point? |

---

## 2. Tool-selection architecture

### 2.1 Five distinct roles

| Role | Purpose | Examples | Control rule |
|---|---|---|---|
| **System of record** | Canonical research, requirements, decisions, components or code | Confluence, Jira, Dovetail, Figma Libraries, Storybook, Git | AI may read approved content; it does not silently replace ownership, versioning or approval. |
| **Reasoning assistant** | Search, synthesize, compare, draft and critique | ChatGPT Work, Claude for Work, Gemini, Microsoft 365 Copilot, Rovo, Notion AI | Require source scope, citations/evidence links, uncertainty and human verification. |
| **Creation surface** | Directly manipulate flows, screens, prototypes, media or documents | Figma agent, Figma Make, Figma Weave, Miro AI, Claude Artifacts, Copilot Pages | Generated artifacts remain editable; preserve provenance and canonical design-system mapping. |
| **Validation surface** | Test accessibility, components, visual changes, research results or telemetry | Stark Sidekick, Storybook/Chromatic, Maze, UserTesting, GA4, BigQuery/Looker | Automated checks cover only defined rules; human testing and expert acceptance remain mandatory. |
| **Action/agent layer** | Retrieve from or act across systems | Rovo Agents, Copilot Studio, ChatGPT connectors/agents, Claude connectors/MCP, Figma MCP, Codex, Claude Code | Least privilege, read-only default, explicit confirmation, logs, allowlists, stop conditions and rollback. |

### 2.2 Data classes

| Class | Examples | Default rule |
|---|---|---|
| **D0 — public/synthetic** | Published material, fabricated personas, cleared placeholder content | May enter an approved tool; still check copyright, product status and source quality. |
| **D1 — internal** | Non-sensitive process notes and draft requirements | Managed enterprise account only; owner and retention required. |
| **D2 — confidential** | Unreleased product, proprietary research, code and design-system assets | Approved enterprise tenancy/project with IAM, DLP, retention, logging and minimum-necessary data. |
| **D3 — personal/regulated** | Participant/customer/employee data, recordings, financial or transaction data | Prohibited by default; requires purpose-specific Privacy, Legal and Security approval, consent/lawful basis, minimization and deletion lineage. |

---

## 3. Multi-platform product and surface catalogue

**Reading rule:** “AI may assist” states a practical design use—not a claim that the tool can make the design decision. Availability, edition, data handling, region and beta status must be rechecked before procurement or production use.

| Capability lane | Product / surface | Vendor | AI may assist | Best workflow stages | Bank boundary / human control | Status note and official source |
|---|---|---|---|---|---|---|
| General work assistant | **ChatGPT Work — Projects, deep research, file analysis, connectors and visual work surfaces** | OpenAI | Search and synthesize approved sources; compare briefs; analyze files; draft research plans, flows, specifications and review checklists. | Discover, Research, Observe, Scale | Enterprise workspace and approved connectors only for D1–D3; designer opens sources and validates conclusions. | Capabilities vary by workspace and admin controls. [OpenAI developer/product documentation](https://developers.openai.com/) |
| Image generation/editing | **GPT Image 2** | OpenAI | Generate synthetic concept imagery, edit cleared assets, create mood-board directions and placeholder visuals. | Prototype, Pilot, Optimize | D0/cleared references by default; Brand/Legal reviews representation, likeness, text and IP. | Current image generation/editing model; do not plan new work around deprecated DALL·E surfaces. [GPT Image 2](https://developers.openai.com/api/docs/models/gpt-image-2) |
| Coding agent | **Codex** | OpenAI | Read an approved repository, implement UI drafts, create tests, inspect diffs and support review. | Production, Scale | Developer owns code; tests, security, accessibility and merge gates remain mandatory. | Use within approved repository and environment. [OpenAI developer/product documentation](https://developers.openai.com/) |
| General reasoning | **Claude for Work — Projects, Artifacts, web search and connectors** | Anthropic | Maintain project context; synthesize evidence; create editable documents, diagrams, flowcharts, React prototypes and critique artifacts. | Discover, Research, Prototype, Scale | Use Work plan for company data; check connector scopes. Artifacts are prototypes, not production or accessibility proof. | Artifacts support documents, SVG, diagrams, websites and React components. [Claude Artifacts](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them) · [Projects](https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects) |
| Connected assistant | **Claude connectors / remote MCP** | Anthropic | Retrieve approved content from tools such as Google Drive, Atlassian or other enabled services and act through permitted connectors. | Discover, Research, Production, Scale | Owner-enabled connectors, least privilege and read-only default; custom MCP can introduce prompt-injection or malicious-tool risk. | Connector behavior and availability vary by plan. [Custom connectors](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp) |
| Coding agent | **Claude Code** | Anthropic | Inspect a codebase, draft UI implementation, tests and documentation, and use Figma MCP context where configured. | Production, Scale | Developer reviews every diff; no unattended merge/deploy. | Commercial agreements and security configuration apply. [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/overview) |
| Managed productivity | **Microsoft 365 Copilot Chat and Copilot Pages** | Microsoft | Ground discussion in permitted Microsoft 365 content; turn responses into persistent, editable and shareable problem briefs, research summaries and decision pages. | Discover, Research, Pilot, Scale | Copilot follows existing permissions, which means over-shared content remains a governance risk; owners validate sources and access. | Pages are an editable collaborative canvas. [Copilot Pages](https://support.microsoft.com/en-us/microsoft-365-copilot/get-started-with-microsoft-365-copilot-pages) · [Privacy and protection](https://learn.microsoft.com/en-us/copilot/privacy-and-protections) |
| Enterprise agent builder | **Copilot Studio / Microsoft 365 declarative agents** | Microsoft | Build a governed design-knowledge or policy assistant using instructions, approved knowledge and bounded actions. | Adapt/Adept across all stages | Use for scoped retrieval/simple workflows; complex multistep decisions need custom orchestration and human gates. | Declarative agents inherit M365 controls but have architectural limits. [Declarative agents](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-declarative-agent) · [Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio) |
| Managed Google work | **Gemini in Workspace / managed Gemini app** | Google | Draft and summarize Docs/Sheets/Slides, analyze approved files and support discovery, research, reporting and communication. | Discover, Research, Pilot, Observe, Scale | Managed account only for bank data; availability and controls vary by edition/region. | [Workspace AI privacy](https://workspace.google.com/security/ai-privacy/) |
| Source-grounded notebook | **Gemini Notebook (formerly NotebookLM)** | Google | Build a cited evidence notebook from approved briefs, policies and research; generate briefing guides and surface contradictions. | Discover, Research, Scale | Imported copies can become stale; require source owner, canonical URI, sync state and expiry. | [Source behavior](https://support.google.com/notebooklm/answer/16215270) |
| Google enterprise/API | **Gemini Enterprise Agent Platform / Gemini API** | Google | Build evaluated grounded assistants, multimodal analysis or governed product AI where off-the-shelf chat is insufficient. | Adapt/Adept across all stages | Platform team supplies IAM, redaction, observability, evaluation, region, retention and rollback. | API/feature status may vary between GA and Preview. [Enterprise Agent Platform](https://cloud.google.com/products/gemini-enterprise-agent-platform) |
| Google coding | **Gemini Code Assist Standard/Enterprise** | Google | Draft UI code, tests and explanations inside an approved development environment. | Production, Scale | Engineering review and canonical component mapping are mandatory. | [Gemini Code Assist](https://developers.google.com/gemini-code-assist/docs/write-code-gemini) |
| Knowledge/search | **Confluence + Atlassian Rovo Search, Chat and Agents** | Atlassian | Search Confluence/Jira and connected sources; answer with accessible organizational context; draft or review design documentation; run specialized onboarding or design-policy agents. | Discover, Research, Production, Scale | Rovo respects user permissions but cannot fix over-sharing or stale content; every page needs owner, metadata and review date. | Rovo includes Search, Chat, Agents and Studio workflows. [What is Rovo?](https://support.atlassian.com/rovo/docs/what-is-rovo/) · [Agent profiles](https://support.atlassian.com/rovo/docs/browse-agents/) |
| Knowledge/search alternative | **Notion AI Enterprise Search and Research Mode** | Notion | Search workspace, databases, connected apps and web; create cited project reports; compare GPT, Claude and Gemini where enabled. | Discover, Research, Scale | Use only if Notion is an approved system; scope sources deliberately and verify model-dependent connector behavior. | Business/Enterprise feature availability. [Enterprise Search](https://www.notion.com/help/enterprise-search) · [Research Mode](https://www.notion.com/help/research-mode) |
| Research repository | **Dovetail AI — contextual chat, Magic summary/highlight/cluster/redact** | Dovetail | Transcribe approved sessions, draft summaries, highlight evidence, cluster themes, query research and produce an initial insight report linked to source data. | Research, Pilot, Observe, Scale | Researcher checks raw evidence, negative cases and sampling; D3 requires consent, retention and deletion lineage. | Some capabilities and language quality vary by plan. [Dovetail AI](https://dovetail.com/help/dovetail-ai/) |
| Collaborative synthesis | **Miro AI — Create with AI, clustering, summaries, diagrams and prototypes** | Miro | Generate editable sticky notes and flowcharts; cluster by keyword/sentiment; summarize workshops; turn selected board content into diagrams or prototype drafts. | Discover, Research, Prototype | Facilitator preserves outliers and participant meaning; AI clusters are hypotheses, not research findings. | [Miro AI overview](https://help.miro.com/hc/en-us/articles/28765406244498-Miro-AI-overview) · [Create with AI](https://help.miro.com/hc/en-us/articles/20164358139794-Create-with-AI) |
| Design creation | **Figma agent in Figma Design** | Figma | Conversationally create, edit and refine designs, apply a design system, obtain feedback, or build reusable plugins/shaders. | Prototype, Optimize, Scale | Designer checks component provenance, layout, content, states and accessibility. Admin AI controls apply. | **Open beta / gradual rollout** as of this draft. [Get started with Figma AI](https://help.figma.com/hc/en-us/articles/24039793359767-Get-started-with-Figma-AI) |
| Functional prototyping | **Figma Make** | Figma | Turn prompts or attached Figma designs/components into functional prototypes, web apps and interactive UI; point at a preview area and iterate. | Prototype, Pilot | Treat output as a prototype until code, data, security, accessibility and performance are reviewed. | Full functionality/availability depends on plan/seat. [Explore Figma Make](https://help.figma.com/hc/en-us/articles/31304412302231-Explore-Figma-Make) |
| Media workflows | **Figma Weave and Weave tools in Figma** | Figma | Build node-based AI media workflows; generate variations, mockups and vector illustration; transfer style; replace background; change lighting or apply a palette. | Prototype, Optimize | D0/cleared assets by default; preserve brand/IP review and disclose synthetic content where required. | Weave tools in Figma are **open beta**; standalone Figma Weave remains a separate product. [Use Weave tools](https://help.figma.com/hc/en-us/articles/40779260614935-Use-Weave-tools-in-Figma) |
| Figma AI productivity | **Replace content; Rewrite; Translate; Shorten; Rename layers** | Figma | Populate realistic UI content, revise UX copy and organize layers in bulk. | Prototype, Production | UX writer/designer verifies product truth, legal text, terminology, locale and naming conventions. | [Replace content](https://help.figma.com/hc/en-us/articles/23796390206743-Replace-text-content-with-AI) · [Rename layers](https://help.figma.com/hc/en-us/articles/24004711129879-Rename-layers-with-AI) |
| Figma AI imagery | **Make image; Edit image; Remove background; Upscale; Expand or remove objects** | Figma | Create or edit supporting imagery without leaving the design canvas. | Prototype, Optimize | Brand, representation and rights review; never use generated imagery as factual evidence. | [Make or edit an image](https://help.figma.com/hc/en-us/articles/24004542669463-Make-or-edit-an-image-with-AI) |
| Figma AI prototyping | **Add interactions with AI** | Figma | Connect selected frames, link navigation and create simple prototype flows. | Prototype, Pilot | Designer tests every route, back behavior, keyboard order, error/recovery and dead ends. | [Make interactions with AI](https://help.figma.com/hc/en-us/articles/24004778051479-Make-interactions-with-AI) |
| Design-to-code/context | **Figma Dev Mode, Code Connect and Figma MCP server** | Figma | Give coding agents structured components, variables and layout context; map design components to production components; read or, where enabled, write editable Figma primitives. | Production, Scale | Canonical IDs and code mappings are required; agent output needs diff, test and merge review. | Some MCP write capabilities are beta/seat-limited. [Figma MCP server](https://help.figma.com/hc/en-us/articles/39216419318551-Get-started-with-the-Figma-MCP-server) |
| Component source of truth | **Storybook + Chromatic visual tests** | Storybook/Chromatic | Document production components and states; compare screenshots against baselines to detect visual changes. AI coding agents can consume the component contract as context. | Production, Scale | It does not automatically prove UX quality or full accessibility; reviewers approve intentional diffs. | Storybook visual testing uses Chromatic. [Visual tests](https://storybook.js.org/docs/9/writing-tests/visual-testing) |
| Accessibility assistant | **Stark Sidekick for Figma/Sketch** | Stark | Scan designs and suggest fixes for contrast, typography, alt text and other potential accessibility issues. | Prototype, Pilot, Production | “Potential” issues require manual checking; conduct keyboard, screen-reader, zoom/reflow, motion and cognitive testing on rendered UI. | [Stark Sidekick](https://www.getstark.co/support/getting-started/using-sidekick/) |
| Research/testing | **Maze AI — study creation, bias suggestions, dynamic follow-ups, AI moderator and theme/sentiment analysis** | Maze | Draft a study, identify potentially leading questions, ask adaptive follow-ups, summarize sessions and surface themes. | Research, Pilot, Optimize | Researcher approves objectives, sampling and question wording; disclose AI moderation and do not treat generated themes as causal proof. | Some features are beta, Enterprise or add-on. [Maze AI](https://maze.co/ai/) |
| Research/testing alternative | **UserTesting AI insight summary** | UserTesting | Summarize patterns across supported task results using transcript and behavioral data and link back to source/contributor evidence. | Pilot, Observe | Researcher reviews sessions and contradictory cases; feature limits depend on study type and contributor count. | [AI insight summary](https://help.usertesting.com/hc/en-us/articles/13268691111453-AI-insight-summary) |
| App/prototype builder | **Replit Agent and Design Canvas** | Replit | Explore mockups, compare visual directions, convert an approved Figma frame into an interactive app and iterate before applying a direction to code. | Prototype, Pilot | Prototype environment only until enterprise, security, code, accessibility and deployment reviews pass. | Capabilities/entitlements vary by plan. [Replit Agent](https://docs.replit.com/core-concepts/agent) · [Design systems](https://docs.replit.com/teams/custom-design-system) |
| Analytics | **GA4 / Gemini in BigQuery / Looker Conversational Analytics** | Google | Detect anomalies, draft reviewed SQL, explore governed semantic data and help communicate validated observations. | Observe, Optimize | Analyst owns event taxonomy, consent, joins, denominators, power and causal interpretation. | Preview and GA surfaces must be distinguished. [Gemini in BigQuery](https://docs.cloud.google.com/bigquery/docs/write-sql-gemini) |

### 3.1 Figma AI feature names — explicit reference list

Use exact feature names in requirements and procurement records; avoid the vague phrase “Figma AI.”

| Figma surface | Named feature | Practical design use | Important limitation |
|---|---|---|---|
| Figma Design | **Figma agent** | Create/edit/refine designs, apply design-system context, request feedback, build custom plugins/shaders. | Open beta and gradual rollout; output still needs design review. |
| Figma Make | **Prompt-to-app functional prototyping** | Generate and iterate working prototypes or web apps from prompts and attached Figma context. | Prototype does not equal production-ready application. |
| Figma Design/Sites | **Replace content** | Replace placeholder copy with realistic examples. | Not product truth; verify terminology and regulatory copy. |
| Figma products | **Rewrite text / Translate text / Shorten text** | Rapid UX-copy alternatives and localization drafts. | Require UX writing, localization and compliance review. |
| Figma Design | **Rename layers with AI** | Contextually name default layers in bulk. | Does not enforce the organization’s full component naming policy. |
| Figma products | **Make image / Edit image** | Generate or modify imagery in canvas. | Rights, factuality, likeness and bias remain human checks. |
| Figma Design | **Add interactions with AI** | Connect selected frames and common navigation actions. | Only a starting flow; validate all states and routes. |
| Figma Design | **Asset/visual search** | Find relevant assets/components using visual or semantic context where available. | Search result is not proof that an asset is current or approved. |
| Figma Design | **Weave tools** | Generate mockup, Transfer style, Replace background, Change lighting, Text to vector illustration, Apply color palette. | Open beta; standalone Weave has separate account/credit behavior. |
| Dev workflow | **Figma MCP server — read/write context** | Expose structured design context to approved agents; create/update editable Figma primitives where enabled. | Beta/seat limitations; confirm every write and inspect diffs. |
| Dev workflow | **Dev Mode + Code Connect** | Inspect design intent and map Figma components to real code components. | Requires maintained mappings; not itself an AI compliance check. |

---

## 4. Eight-stage multi-vendor workflow

### 4.1 Discover — align problem, outcomes, stakeholders and evidence

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — establish sources** | Designer lists the brief, policy, past research, analytics and stakeholder owners. | Confluence + Rovo; Microsoft 365 Copilot; Notion AI; Gemini Notebook; ChatGPT or Claude with approved connectors | Retrieve related material, show source links, summarize contradictions and identify missing owners/dates. | Which source is authoritative; whether access and reuse are permitted. | Source register with owner, URI, update date and data class. |
| **Step 2 — frame the problem** | Designer and PO/DPO define users, jobs, business outcome, constraints and decision rights. | Copilot Pages; ChatGPT Project; Claude Project/Artifact; Gemini in Docs | Draft a problem statement, assumptions log, stakeholder map and questions. | Product strategy, regulatory interpretation, scope and success criteria. | Approved problem frame and assumption backlog. |
| **Step 3 — visualize alignment** | Convert the approved frame into an editable system or journey overview. | Miro AI; Figma/FigJam; Claude Artifacts | Generate a first flowchart, stakeholder map or journey structure from approved text. | Whether the map represents reality; unresolved conflicts and exclusions. | Editable overview diagram linked to evidence. |

**3A × 3K:** Adopt uses bounded summarization; Adapt uses reusable discovery rubrics and source manifests; Adept uses evaluated read-only retrieval agents. Know-how is prompting and source inspection, Know-what is strategic framing, and Know-where is correct routing to canonical evidence.

### 4.2 Research — plan, conduct, synthesize and preserve evidence

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — plan** | Researcher defines learning objectives, sample, method, consent and exclusions. | ChatGPT Work; Claude; Gemini; Microsoft 365 Copilot; Maze | Draft a guide, critique leading questions, build a traceability matrix from objective to question. | Sampling, ethics, method, compensation, consent and stopping rule. | Approved research plan and script. |
| **Step 2 — collect** | Researcher conducts or supervises sessions and records only permitted data. | Maze AI moderator/follow-ups; UserTesting; Dovetail transcription | Transcribe, ask bounded follow-ups, tag session metadata and flag possible PII. | Whether AI moderation is appropriate; disclosure; participant safety; when to intervene. | Consent-linked raw evidence with retention/deletion record. |
| **Step 3 — synthesize** | Researcher reviews transcripts, clips, observations and behavioral evidence. | Dovetail AI; Miro AI clustering; Gemini Notebook; ChatGPT/Claude | Suggest highlights, summaries, clusters, counterexamples and open questions; link statements to sources. | Theme meaning, evidence strength, dissent, bias, translation and saturation. | Evidence matrix, findings and limitations. |
| **Step 4 — translate to design inputs** | Designer turns validated findings into needs, tasks, scenarios and acceptance risks. | Figma/FigJam; Miro; Confluence/Rovo; Copilot Pages | Draft jobs, opportunity areas, user stories, edge cases and research-to-requirement links. | Priority, feasibility and which insight justifies each requirement. | Traceable design brief. |

**3A × 3K:** Adapt adds a versioned coding framework and prompt/evidence schema. Adept may continuously classify approved feedback, but it must preserve traceability and surface low-confidence/outlier evidence for human review.

### 4.3 Prototype — convert evidence into flows, wireframes and connected screens

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — sync latest context** | Designer retrieves the current research, PRD, policy and design-system guidance. | Confluence + Rovo; ChatGPT/Claude connectors; Copilot; Gemini Notebook; Figma agent MCP connectors | Summarize only current approved content, list conflicts and attach citations/owners. | Which version is valid; what must be clarified with PO/DPO, Research or Compliance. | Signed context pack with version IDs. |
| **Step 2 — create user-flow logic** | Designer converts requirements into the main path plus alternate, error, empty, timeout and recovery paths. | Miro AI; FigJam/Figma agent; Claude Artifacts; ChatGPT visual workspace | Generate an editable horizontal flowchart and identify missing states or decision branches. | Information architecture, decision logic, risk and user-control points. | Approved user-flow diagram. |
| **Step 3 — create each wireframe screen** | Build screens one by one from each node in the approved flow. | Figma agent; Figma Design; Miro prototype; Figma Make; Replit Canvas | Draft screens, content alternatives, layout variations and responsive directions using canonical components where possible. | Screen hierarchy, task clarity, component choice, disclosure and cognitive load. | Numbered low/mid-fidelity wireframes linked to flow nodes. |
| **Step 4 — connect and review the map** | Connect every wireframe into one interaction map so the designer and PO/DPO can review end to end. | Figma **Add interactions with AI**; Figma prototyping; Figma Make | Add basic connections and highlight unreachable screens, missing back paths or inconsistent labels. | Whether the flow solves the user need and operational/regulatory constraints. | Connected prototype map and gap log. |
| **Step 5 — enrich assets and content** | Add only the imagery and copy required for realistic testing. | Figma Replace/Rewrite/Translate/Shorten; GPT Image 2; Figma Make/Edit image; Figma Weave tools | Create placeholder imagery, UX-copy alternatives, translations and asset variations. | Product truth, brand, rights, representation, locale and legal wording. | Test-ready content and asset provenance record. |
| **Step 6 — initial accessibility review** | Check design-level risks before testing. | Stark Sidekick; Figma inspection; approved contrast/token tools | Flag contrast, typography, alt-text and other potential issues. | Acceptance; manual assessment of focus, reading order, zoom, motion and cognition. | Accessibility issue log and remediation plan. |

### 4.4 Pilot — test with real users and controlled operational scenarios

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — prepare** | Define tasks, participants, devices, assistive technology and risk scenarios. | Maze; UserTesting; ChatGPT/Claude/Gemini/Copilot for script drafting | Draft task wording, test-data matrix and note-taking template; flag likely bias. | Recruitment, accessibility coverage, test fidelity and stop rules. | Pilot protocol. |
| **Step 2 — execute** | Observe task completion and recovery on the connected prototype. | Figma prototype/Make; Maze; UserTesting | Capture paths, transcript, follow-ups and supported behavioral evidence. | When to probe, stop or protect a participant; severity and root cause. | Session evidence. |
| **Step 3 — analyze** | Triangulate what users did, said and failed to recover from. | Dovetail AI; Maze themes; UserTesting AI insight summary; ChatGPT/Claude | Produce a first-pass summary, theme candidates, clips and contradiction list. | Finding validity, priority, bias, subgroup harm and go/no-go recommendation. | Pilot report with traceable evidence. |
| **Step 4 — close the loop** | Update flow, screens and decision log. | Figma; Confluence/Rovo; Copilot Pages | Draft change log and map each issue to the changed node/screen. | Which change resolves the evidence and whether retesting is required. | Revised prototype and signed decision record. |

### 4.5 Production — hand off a testable design contract and implement safely

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — prepare design contract** | Mark approved frames and document components, tokens, states, content, breakpoints and accessibility notes. | Figma Dev Mode; Code Connect; Confluence; Storybook | Figma text AI may improve draft descriptions; Rovo/Copilot/ChatGPT/Claude may populate an approved template from inspected context. | Completeness, canonical IDs, state behavior and acceptance criteria. | Versioned handoff contract. |
| **Step 2 — implement** | Engineer pulls structured design and component context into the approved repository. | Figma MCP; Codex; Claude Code; Gemini Code Assist; Replit Agent where approved | Draft UI code and tests, reuse mapped production components, explain diffs. | Architecture, security, data handling, performance and merge decision. | Reviewed pull request. |
| **Step 3 — validate components and visuals** | Exercise every state in isolation and compare rendered output with approved baselines. | Storybook; Chromatic visual tests; Stark; CI | Generate test drafts, flag visual changes and accessibility candidates. | Whether a change is intentional and whether the rendered UI meets acceptance. | Component/visual/accessibility evidence. |
| **Step 4 — release safely** | Run localization, telemetry, security, performance, accessibility and rollback checks. | Existing CI/CD and monitoring; Copilot Studio or agents only for bounded support | Draft release notes, summarize evidence and flag missing approvals. | Canary exposure, production release, stop/rollback and incident ownership. | Signed release candidate and audit trail. |

### 4.6 Observe — turn telemetry and feedback into validated insight

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — validate instrumentation** | Confirm taxonomy, consent, identity assumptions, schema, missing/duplicate events and metric owners. | GA4; BigQuery; approved analytics stack | Draft SQL or tagging QA checks. | Metric definition, data quality and lawful collection. | Instrumentation QA record. |
| **Step 2 — detect and explore** | Review product behavior, feedback, complaints and incidents together. | Gemini in BigQuery/Looker; Dovetail Channels; UserTesting; ChatGPT/Claude file analysis | Identify anomalies, segment candidates, common feedback and possible explanations. | Whether an observation is real, material and actionable; correlation vs causation. | Validated observation with supporting evidence. |
| **Step 3 — route action** | Link an insight to affected flow, screen, component, owner and risk. | Confluence/Rovo; Copilot Pages; Figma; Jira | Draft the issue, affected-state list and evidence summary. | Priority, response, incident escalation and need for new research. | Traceable action recommendation. |

### 4.7 Optimize — improve through valid experiments and guarded iteration

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — define hypothesis** | State evidence, target behavior, primary metric, guardrails, subgroup checks and stopping rule. | Copilot Pages; ChatGPT/Claude/Gemini; Confluence | Critique logic, list confounds and draft preregistration. | Whether testing is ethical, powered and useful. | Approved experiment plan. |
| **Step 2 — generate bounded variants** | Create only variants justified by the hypothesis and canonical system. | Figma agent; Figma Make; Figma Weave; GPT Image 2; Miro AI | Produce alternative layouts, interaction or content treatments. | Which variants are coherent, accessible, non-manipulative and on-brand. | Reviewable variant set. |
| **Step 3 — run and analyze** | Execute through the approved experimentation platform and monitor guardrails. | Analytics stack; BigQuery/Looker assistance | Draft reviewed queries, check anomalies and summarize results. | Power, sample-ratio mismatch, multiple comparisons, causality, subgroup disparity and rollback. | Validated experiment result. |
| **Step 4 — institutionalize learning** | Update design, evidence and decision records. | Figma; Storybook; Confluence/Rovo; Dovetail | Draft the change and learning record. | Whether to ship, iterate, reject or retest. | Versioned learning and approved change. |

### 4.8 Scale — institutionalize reusable knowledge, components and governed agents

| Step | Context and direct action | Product / surface | AI may assist | Human must decide | Approved output |
|---|---|---|---|---|---|
| **Step 1 — govern canonical sources** | Assign owner, version, expiry, permissions and deprecation status to research, policy, component and code assets. | Confluence/Rovo; Dovetail; Figma Libraries; Storybook; Git | Detect missing metadata, stale content and conflicts. | Canonical status and remediation owner. | Governed source inventory. |
| **Step 2 — package repeatable assistance** | Store approved prompts, instructions, schemas, examples and evaluation cases outside a vendor chat. | ChatGPT Projects/agents; Claude Projects/connectors; Gemini/Gems; Copilot agents; Rovo Agents | Deploy bounded role assistants from governed configuration. | Scope, permissions, supported tasks, escalation and release version. | Versioned assistant package. |
| **Step 3 — connect systems selectively** | Add read-only connectors first; add actions only when value and controls are proven. | Figma MCP; Rovo; Copilot Studio; Claude MCP; OpenAI connectors/agents; Miro MCP | Retrieve approved context, draft changes or open reviewable proposals. | Which systems can be accessed or changed; confirmation and rollback design. | Least-privilege integration with logs. |
| **Step 4 — evaluate and operate** | Monitor quality, accessibility, retrieval drift, incidents, latency, cost and human override behavior. | Vendor eval/observability plus internal dashboards | Run test sets, flag drift and summarize operational evidence. | Promotion/downgrade, suspension, vendor exit and competency requirements. | Revalidation and operating record. |

---

## 5. 3A × 3K application across the workflow

| Maturity | Know-how — execution | Know-what — judgment | Know-where — context/routing | Typical tool pattern |
|---|---|---|---|---|
| **Adopt** | Use one approved assistant for a bounded task; inspect sources; edit the output; record tool and reviewer. | Choose tasks with low blast radius and clear verification; know when no AI is needed. | D0–D1 only in the approved enterprise account; manually move the approved artifact into its system of record. | Copilot/ChatGPT/Claude/Gemini for drafting; Figma AI for bounded canvas work; Dovetail/Maze for first-pass analysis. |
| **Adapt** | Use source packs, templates, schemas, prompt releases, canonical component IDs and repeatable evaluation. | Decide which context improves quality and which increases privacy, injection or cognitive-load risk. | Connect only approved sources; use versioned manifests, owners, expiry and permission-aware retrieval. | Rovo/Notion/Notebook for governed retrieval; Figma agent/Make with design-system context; Storybook/Code Connect for implementation contract. |
| **Adept** | Operate evaluated agents that retrieve or propose changes across systems; inspect logs; exercise rollback and exception paths. | Redesign work only where automation improves validated user/business outcomes without weakening guardrails. | Least-privilege actions in approved environments; human confirmation before consequential change; vendor-exit path. | Copilot Studio, enterprise Gemini, approved OpenAI/Anthropic agents or coding agents plus Figma/Miro MCP and CI—selectively, not universally. |

### Promotion rule

A workflow advances only when it has: two or more repeatable cycles; a named owner; external versioned configuration; representative evaluation; controlled data routing; measured benefit; no material accessibility/privacy/safety loss; and a tested fallback. A vendor feature moving from beta to GA does not automatically promote the workflow.

---

## 6. Recommended stack for the HSB design context

This recommendation preserves the existing tool preferences—**Figma, Confluence, Storybook, Copilot, GPT, Claude and Gemini**—and adds optional specialist tools only where they solve a clear gap.

### 6.1 Core stack

| Need | Recommended core | Exact use |
|---|---|---|
| Central knowledge | **Confluence + Rovo** | Canonical design/research/decision pages with owner, metadata and review date; permission-aware search/chat; verified design-knowledge agents only after evaluation. |
| Daily enterprise assistant | **Microsoft 365 Copilot** | Work across permitted Word, PowerPoint, Excel, Outlook, Teams and SharePoint context; use Copilot Pages for persistent collaborative briefs and decisions. |
| Deep reasoning and alternative critique | **ChatGPT Work + Claude for Work + managed Gemini** | Use one primary model and one controlled challenger for high-impact critique; do not paste the same D2/D3 material into unapproved consumer accounts. |
| Design and prototyping | **Figma Design + Figma agent + Figma Make** | Context sync → flow → screen-by-screen wireframe → connection map → functional prototype, always mapped back to canonical components and reviewed by the designer. |
| Media exploration | **Figma Weave / Weave tools** | Cleared D0 visual variants, mockups, style/palette/lighting/background work; Brand/Legal approval before use. |
| Handoff and component truth | **Figma Dev Mode + Code Connect + Storybook** | Map Figma components to production components, document all states and keep design/code references aligned. |
| Implementation assistance | **Codex, Claude Code or Gemini Code Assist** | Choose the coding agent approved for the repository; draft implementation/tests, inspect diffs and require human merge. |
| Visual regression | **Chromatic with Storybook** | Compare component screenshots to approved baselines and review every intentional change. |

### 6.2 Optional specialist additions after Security, Privacy and Procurement review

| Gap | Optional tool | Why add it |
|---|---|---|
| Research repository and evidence traceability | **Dovetail AI** | Stronger transcript/highlight/theme/source workflow than a general chatbot. |
| Rapid remote testing and adaptive follow-up | **Maze AI** or **UserTesting** | Adds participant workflow, behavioral evidence and test-specific analysis. |
| Workshop synthesis and editable diagrams | **Miro AI** | Makes research walls, flows and collaborative diagrams directly editable. |
| Design-stage accessibility assistance | **Stark Sidekick** | Flags candidate design issues early; complements rather than replaces rendered/manual testing. |
| Alternative application prototype | **Replit Agent / Design Canvas** | Useful for functional exploration when Figma Make is not the approved route; still requires production review. |
| Alternative knowledge environment | **Notion AI Enterprise Search** | Consider only if Notion is already approved and adopted; avoid duplicating Confluence as a second uncontrolled source of truth. |

### 6.3 Avoid tool sprawl

Do not license every tool in the catalogue. For each capability lane, select:

1. One canonical system of record.
2. One default enterprise assistant.
3. One challenger model for high-impact critique where justified.
4. One primary design/prototype surface.
5. One research-testing stack.
6. One approved coding-agent route.
7. One validation and release evidence path.

The organization should record why an alternative is needed, which data it may receive, who owns it, how quality is measured and how content will be exported or deleted at exit.

---

## 7. Mandatory workflow controls

### 7.1 Source-freshness record

Every AI-used source needs: source ID/title, owner, canonical URI/system, imported timestamp, authoritative last-update timestamp, sync state, expiry/review date, permitted use/data class, and conflict/revocation status. Stale, unowned, failed-sync or revoked content blocks decision use.

### 7.2 Human gates

| Gate | Timing | Required evidence | Stop condition |
|---|---|---|---|
| **G0 — pre-use** | Before any tool receives data | Product/edition/status, account, data class, region, retention/training terms, DLP/IAM, IP, vendor owner, fallback. | Personal/unpaid route for bank data; unknown terms, status or owner. |
| **G1 — research/data ingestion** | Before notes, recordings or internal sources enter AI | Consent/lawful basis, minimization, reuse, translation, deletion lineage, source freshness, connector threat model. | Consent/purpose unclear; stale source; deletion cannot propagate. |
| **G2 — pre-pilot** | Before controlled users | Participant/device/AT plan, prototype fidelity, severity model, log/retention, stop rule. | No real-user plan; AI-only evaluation; unapproved D2/D3 or beta use. |
| **G3 — pre-production** | Before release | Design contract, security/accessibility/localization evidence, telemetry QA, inventory, canary, kill switch, rollback, on-call. | Untested rollback; no owner; failed critical test. |
| **G4 — operate/revalidate** | Scheduled and triggered | KPI, incident, drift, source/model/status, access, cost and vendor-exit evidence. | Failed evaluation, material harm, stale sources, access incident or policy change. |

### 7.3 Universal checklist

- [ ] State the task, user, decision, constraints and output schema.
- [ ] Classify data and confirm approved account, region, retention and product status.
- [ ] Attach only source-manifest-approved content.
- [ ] Separate trusted instructions from retrieved/user-controlled data.
- [ ] Use source/tool allowlists, minimum scope and read-only connectors by default.
- [ ] Request citations/evidence IDs and uncertainty; open the source.
- [ ] Preserve outliers, contradictions and unknowns rather than smoothing them away.
- [ ] Test happy, empty, error, loading, timeout, refusal, recovery and escalation states.
- [ ] Test language, literacy, disability, device/connectivity, bias and representational harm.
- [ ] Record product, model where exposed, configuration, prompt/instruction release, sources, reviewer and decision.
- [ ] Keep a manual fallback and stop if evidence is stale, consent is unclear or risk exceeds approval.

### 7.4 Accessibility boundary

AI and automated scanners may flag candidates, generate alt-text drafts or propose fixes. Conformance requires the rendered product plus expert/manual testing: keyboard and focus behavior, screen reader, zoom/reflow, contrast, motion, input/error recovery, cognitive comprehension, localization and representative disabled-user research. No LLM, Figma feature, Stark scan, Lighthouse result or model-based score alone certifies accessibility.

---

## 8. KPI and evaluation framework

| Dimension | Measures | Guardrail |
|---|---|---|
| Efficiency | Brief-to-flow time, documentation lead time, component retrieval time, handoff rework | Include human review time and correction cost. |
| Evidence quality | Citation accuracy, source-freshness pass, quote fidelity, dissent retention, translation defects | Block publication if source/consent lineage is incomplete. |
| Design quality | Canonical component use, state coverage, drift defects, visual-regression failures, localization defects | AI output volume is not success. |
| Accessibility/inclusion | Manual AT defects, subgroup task parity, comprehension, motion/zoom/reflow failures | Automated/model scores are not conformance evidence. |
| User outcome | Task success, error recovery, comprehension, trust, complaint/escalation and long-term harm | Segment responsibly where lawful; do not optimize conversion alone. |
| AI reliability | Unsupported claims, grounded-answer rate, tool-call failure, refusal quality, latency and drift | Calibrate model-based evaluation against human experts. |
| Governance | Approved-tool use, DLP/privacy incidents, traceability, stale sources and gate coverage | Governance is mandatory hygiene, not proof of Adept maturity. |
| Operations/FinOps | Rollback success/time, RTO/RPO, alert quality, cost per validated outcome and export/decommission test | Include vendor switching and deletion cost. |
| Human capability | Quality of edits, rejection/override decisions, escalation and scenario assessment | Prompt count and raw usage are poor competency measures. |

---

## 9. Practical implementation sequence

| Horizon | Goal | Action | Exit evidence |
|---|---|---|---|
| **0–30 days** | Governed baseline | Approve the core stack, D0–D3 matrix, system owners, source manifest and prompt/output checklist. Map Figma ↔ Storybook component IDs. | G0 operating, owners trained, baseline measured, fallback documented. |
| **31–90 days** | Adopt | Pilot two low-risk tasks: evidence-to-flow and Figma-to-design-documentation. Use managed Copilot/ChatGPT/Claude/Gemini and Figma AI only with allowed data. | Two traceable cycles, measured time/quality, no material guardrail loss. |
| **3–6 months** | Adapt | Add governed Rovo retrieval, reusable research/design templates, Dovetail or testing integration, design-system-aware Figma workflow and coding-agent test set. | Versioned configuration, representative evaluation, named owners and validated benefit. |
| **6–18 months** | Selective Adept | Add read-only agents/MCP, then tightly bounded actions; monitoring, confirmation UX, red-team tests, canary, rollback, FinOps and vendor exit. | G3/G4 passed, sustained user/business improvement and tested recovery. |

**Recommended target:** selective Adept, not maximum automation. Research interpretation, accessibility acceptance, regulated content, causal analysis and irreversible release decisions should remain human-led whenever that is safer.

---

## 10. Official source index

### OpenAI

- [OpenAI developer and product documentation](https://developers.openai.com/)
- [GPT Image 2](https://developers.openai.com/api/docs/models/gpt-image-2)

### Anthropic

- [Claude Artifacts](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them)
- [Claude Projects](https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects)
- [Claude custom connectors / remote MCP](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp)
- [Claude for Work data roles](https://support.anthropic.com/en/articles/9267385-does-anthropic-act-as-a-data-processor-or-controller)

### Microsoft

- [Microsoft 365 Copilot Pages](https://support.microsoft.com/en-us/microsoft-365-copilot/get-started-with-microsoft-365-copilot-pages)
- [Microsoft 365 Copilot privacy and protection](https://learn.microsoft.com/en-us/copilot/privacy-and-protections)
- [Microsoft 365 declarative agents](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-declarative-agent)
- [Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)

### Figma

- [Get started with Figma AI](https://help.figma.com/hc/en-us/articles/24039793359767-Get-started-with-Figma-AI)
- [Use AI tools in Figma Design](https://help.figma.com/hc/en-us/articles/23870272542231-Use-AI-tools-in-Figma-Design)
- [Explore Figma Make](https://help.figma.com/hc/en-us/articles/31304412302231-Explore-Figma-Make)
- [Use Weave tools in Figma](https://help.figma.com/hc/en-us/articles/40779260614935-Use-Weave-tools-in-Figma)
- [Replace content](https://help.figma.com/hc/en-us/articles/23796390206743-Replace-text-content-with-AI)
- [Rename layers with AI](https://help.figma.com/hc/en-us/articles/24004711129879-Rename-layers-with-AI)
- [Make or edit images](https://help.figma.com/hc/en-us/articles/24004542669463-Make-or-edit-an-image-with-AI)
- [Add interactions with AI](https://help.figma.com/hc/en-us/articles/24004778051479-Make-interactions-with-AI)
- [Figma MCP server](https://help.figma.com/hc/en-us/articles/39216419318551-Get-started-with-the-Figma-MCP-server)

### Knowledge, research, testing and validation

- [Atlassian Rovo](https://support.atlassian.com/rovo/docs/what-is-rovo/)
- [Notion Enterprise Search](https://www.notion.com/help/enterprise-search)
- [Dovetail AI](https://dovetail.com/help/dovetail-ai/)
- [Miro AI](https://help.miro.com/hc/en-us/articles/28765406244498-Miro-AI-overview)
- [Maze AI](https://maze.co/ai/)
- [UserTesting AI insight summary](https://help.usertesting.com/hc/en-us/articles/13268691111453-AI-insight-summary)
- [Stark Sidekick](https://www.getstark.co/support/getting-started/using-sidekick/)
- [Storybook visual tests](https://storybook.js.org/docs/9/writing-tests/visual-testing)
- [Replit Agent](https://docs.replit.com/core-concepts/agent)

### Google

- [Gemini Notebook source behavior](https://support.google.com/notebooklm/answer/16215270)
- [Workspace AI privacy](https://workspace.google.com/security/ai-privacy/)
- [Gemini Enterprise Agent Platform](https://cloud.google.com/products/gemini-enterprise-agent-platform)
- [Gemini Code Assist](https://developers.google.com/gemini-code-assist/docs/write-code-gemini)
- [Gemini in BigQuery](https://docs.cloud.google.com/bigquery/docs/write-sql-gemini)

---

## Final operating principle

The master question is no longer “Which Google AI tool can generate this artifact?” It is:

> **Which approved combination of source, assistant, creation surface, validation surface and action layer produces a traceable, accessible and reversible design outcome—and can the accountable human prove it?**

