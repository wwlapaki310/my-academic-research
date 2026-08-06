# 先行研究・関連研究マップ

## 調査日: 2026-08-06

---

## 1. 研究構想の位置づけ（概念的ギャップ）

現在の学術研究には、以下の3領域がそれぞれ独立に存在する。

1. **OSSニューカマー障壁研究** — Steinmacher系列の「58 barriers model」を中心に、OSSへの初参入障壁を体系化
2. **LLM for SE** — コード生成・バグ報告自動化・ドキュメント理解など、タスク単位のAI支援
3. **OSSエコシステム持続性** — プロジェクトヘルス、メンテナ負荷、コミュニティ衰退の計量的研究

**しかし、これらを統合し「LLMを介して非専門利用者とOSSコミュニティの間に持続的な知識循環をつくる」研究はまだない。**

これが新しい概念を掲げる余地：

> **AI-Mediated Knowledge Circulation between OSS End-Users and Maintainer Communities**

---

## 2. 最重要の先行研究群

### 2.1 OSSニューカマー障壁（Steinmacher系列）

この分野の基盤。Igor Steinmacher（NAU/USP）とMarco Gerosa（NAU）が中心。

| 論文 | 会議/誌 | 要点 |
|------|---------|------|
| Steinmacher et al. (2015) "A systematic literature review on the barriers faced by newcomers to OSS projects" | IST | 58の障壁を5カテゴリに整理したモデル |
| Steinmacher et al. (2015) "Social barriers faced by newcomers placing their first contribution" | CSCW | 社会的障壁（応答なし、作法不明）に焦点 |
| Steinmacher et al. (2016) "Overcoming open source project entry barriers with a portal for newcomers" | ICSE | FLOSScoachポータルの提案・評価 |
| Steinmacher et al. (2019) "Overcoming Social Barriers When Contributing to OSS Projects" | JCSCW | FLOSScoachの日記研究。ポータルがコミュニケーション必要性を減少 |
| Balali et al. (2018) "Newcomers' Barriers... Is That All?" | JCSCW | メンター側の障壁も分析 |

**この構想との関係**: Steinmacher系列は「初回貢献」に焦点。**長期的な知識循環・非専門利用者（開発者でない人）・LLM介在はまだ扱われていない**。ここに新規性がある。

### 2.2 LLMとOSSコミュニティ参加

| 論文 | 会議/誌 | 要点 |
|------|---------|------|
| "LLMs in Wikipedia" (2025, arXiv:2509.07819) | CHI系 | LLMがWikipediaコミュニティ参加に与える影響。新規参加者にはLLMが「暗黙知の壁」を高める逆効果も。設計含意としてscaffolding提案 |
| Tao Xiao et al. (2026) "Self-Admitted GenAI Usage in Open-Source Software" | TSE | OSS開発者によるGenAI利用の実態調査 |
| AI Slopageddon (RedMonk, 2026) | 業界報告 | curl等でAI生成バグ報告がメンテナ負荷を激増。2024-2026で深刻化 |

**この構想との関係**: Wikipedia論文は最も近い先行研究。ただしWikipediaに限定されOSSのコード・Issue文脈は異なる。AI Slopageddon問題は「RQ3: メンテナ負荷」に直結する現実課題。

### 2.3 バグ報告品質とLLM

| 論文 | 会議/誌 | 要点 |
|------|---------|------|
| Acharya & Ginde (2025) "Can We Enhance Bug Report Quality Using LLMs?" | EASE | LLMによるバグ報告生成の品質評価 |
| Bo et al. (2024) "ChatBR: Automated assessment and improvement of bug report quality using ChatGPT" | ASE | ChatGPTによるバグ報告品質の自動評価・改善 |
| Saha & Chaparro (2025) "SPRINT: An Assistant for Issue Report Management" | MSR | Issue報告管理のアシスタントツール |
| Bettenburg et al. (2008) "What Makes a Good Bug Report?" | FSE | バグ報告品質の古典的研究 |

**この構想との関係**: 技術的なバグ報告品質は研究されているが、「非専門利用者が高品質Issueを書けるようにする」「それを通じて利用者がコミュニティに参加し成長する」というHCI的視点は不在。

### 2.4 OSSプロジェクトヘルス・持続性

| 論文/ツール | 会議/誌 | 要点 |
|-------------|---------|------|
| OSSPREY (ASE 2025 Demo) | ASE | AI駆動のOSSプロジェクト持続性予測ダッシュボード |
| Linåker et al. (2026) "Assessing OSS health in organizations' intake processes" | EMSE | 組織がOSSを導入する際のヘルス評価（質的研究） |
| Karim et al. (2026) "AI in OSS Engineering: A Foundation for Sustainability" | arXiv | AI×OSS持続性のサーベイ。メンテナ負荷軽減がテーマ |
| CHAOSS metrics | コミュニティ | OSSコミュニティヘルスの標準指標群 |
| Kula & Robles "The Life and Death of Software Ecosystems" | 書籍章 | OSSエコシステムの衰退・成長のダイナミクス |

**この構想との関係**: プロジェクト側のヘルスは研究されているが、「利用者側の長期運用持続性」「利用者とコミュニティの関係が持続するか」は未踏。

### 2.5 Human-AI Collaboration in SE

| 論文 | 会議/誌 | 要点 |
|------|---------|------|
| Treude & Gerosa (2025) "How Developers Interact with AI: A Taxonomy of Human-AI Collaboration in SE" | FORGE | SEにおけるHuman-AI協調の分類体系 |
| "Bug detective and quality coach" (2026) | ScienceDirect | AIコード品質ツールにおける開発者のメンタルモデル。HCAI視点 |
| "Understanding the LLM-ification of CHI" (2025) | CHI | HCIにおけるLLM研究の現状・偏り。理論的貢献の不足を指摘 |
| "Reporting and Reviewing LLM-Integrated Systems in HCI" (2026) | arXiv | LLM統合システムの査読・報告における課題 |

**この構想との関係**: Human-AI協調のフレームワークは発展中だが、「OSS利用者-メンテナ間の媒介」という文脈は未開拓。

### 2.6 Cross-Community Knowledge Flow

| 論文 | 会議/誌 | 要点 |
|------|---------|------|
| "Building Digital Societies as Ecosystems" (2026) | arXiv | OSSにおける cross-community contributor の役割。boundary workのコストを分析 |
| Zhang et al. (2026) "Knowledge sharing intention in OSS communities" | J. Innovation & Knowledge | OSSコミュニティにおける知識共有意図の構成的分析 |

---

## 3. 打ち立てるべき「新しい概念」の候補

既存研究のギャップから、以下の概念を提案できる可能性がある：

### 概念候補A: **AI-Mediated Community Participation（AI媒介コミュニティ参加）**
- LLMが単なるツールではなく、人とコミュニティの「媒介者」として機能する
- Steinmacherの障壁モデルをLLM時代に拡張する理論的貢献

### 概念候補B: **Knowledge Circulation Interface（知識循環インターフェース）**
- 「利用者→コミュニティ」「コミュニティ→利用者」の双方向知識フローを設計するUIパターン
- 既存の「情報アクセス改善」を超え、「関係構築」を目的にした設計原則

### 概念候補C: **Participatory Scaffolding（参加的足場かけ）**
- 教育学のscaffoldingをOSSコミュニティ参加に適用
- LLMが段階的に「自分でできる」ように支援し、最終的にAI支援なしでコミュニティ参加できる
- Wikipedia×LLM論文のscaffolding提案を発展させる

### 概念候補D: **Open Source Translation Layer（OSS翻訳層）**
- 技術的翻訳（エラー→Issue）、言語的翻訳（日本語→英語）、社会的翻訳（作法・文化）を統合する概念
- 「翻訳」はHCI/CSCWで既に使われる概念だが、OSSの文脈で体系化されていない

---

## 4. 関連する研究者・研究室マップ

### 4.1 日本国内

| 研究者 | 所属 | 関連領域 | 適合度 |
|--------|------|----------|--------|
| **Raula Gaikovina Kula** | 大阪大学（旧NAIST） | Software Ecosystems, Human-AI Interaction, OSSエコシステム | ★★★★★ 最有力 |
| **Hideaki Hata** | 信州大学 | OSS Ecosystems, Software Economics, GenAI in OSS | ★★★★☆ |
| **亀井靖高 (Yasutaka Kamei)** | 九州大学 | Empirical SE, Mining Software Repositories | ★★★★☆ |
| **石尾隆 (Takashi Ishio)** | 和歌山大学 → NAIST | OSSコード再利用、開発支援 | ★★★☆☆ |
| **松本健一 (Kenichi Matsumoto)** | NAIST | ソフトウェア工学全般 | ★★★☆☆ |
| **NII系** | 国立情報学研究所 | ソフトウェア品質、AI活用 | ★★★☆☆ |

**特筆**: **Raula Gaikovina Kula教授**（大阪大学）は、Software Ecosystems + Human-AI Interactionを研究テーマに掲げており、この構想と最も親和性が高い。Steinmacher、Treude、Kameiらと広い共同研究ネットワークを持つ。

### 4.2 海外

| 研究者/グループ | 所属 | 関連領域 | 適合度 |
|-----------------|------|----------|--------|
| **Igor Steinmacher** | NAU (USA) | OSSニューカマー障壁、FLOSScoach | ★★★★★ 先行研究の中心人物 |
| **Marco Gerosa** | NAU (USA) | CSCW, OSS, Human-AI Collaboration in SE | ★★★★★ |
| **Christoph Treude** | SMU (Singapore) | SE情報アクセス、LLM×SE、ドキュメント | ★★★★☆ |
| **Arie van Deursen / Andy Zaidman** | TU Delft (NL) | SERG, AI4SE, software testing | ★★★★☆ |
| **Alexander Serebrenik** | TU Eindhoven (NL) | Social Software Engineering | ★★★★☆ |
| **Margaret-Anne Storey** | U of Victoria (CA) | Developer Experience, CSCW, SE | ★★★★☆ |
| **Sean Goggins** | U of Missouri (USA) | CHAOSS, OSS sustainability, AI for OSS | ★★★☆☆ |
| **Software Sustainability Institute** | UK | Research Software Engineering, sustainability | ★★★☆☆ |

### 4.3 推奨するアプローチ

**主指導**: Raula Gaikovina Kula（大阪大学）が最有力。社会人博士の受入実績、OSS Ecosystems + Human-AI Interaction、Steinmacher・Treudeとの共同研究ネットワーク。

**副指導・共同研究**: Steinmacher/Gerosa（NAU）、Treude（SMU）、Kamei（九州大学）

---

## 5. 投稿先ターゲットと研究フェーズ

| フェーズ | 内容 | ターゲット会議 |
|----------|------|----------------|
| 研究1: 質的調査 | 非専門利用者の障壁マッピング | CSCW, CHI |
| 研究2: システム提案 | AI媒介Issue作成・知識循環システム | ICSE, FSE, CHI |
| 研究3: 比較実験 | LLM支援なし vs 汎用チャット vs 提案システム | ICSE, ASE |
| 研究4: フィールド研究 | NuttX等での長期評価 | CSCW, MSR |
| 可視化・応用 | 知識循環の可視化 | SIGGRAPH Asia, IEEE VIS |

---

## 6. 次のアクション

1. [ ] Wikipedia×LLM論文 (arXiv:2509.07819) を精読し、scaffolding設計含意を抽出
2. [ ] Steinmacherの58障壁モデルを「非専門利用者」に拡張した予備調査を設計
3. [ ] Raula Gaikovina Kula教授の最新論文リストを確認し、コンタクトを検討
4. [ ] AI Slopageddon問題（curl, Python等）のケーススタディデータを収集
5. [ ] 概念候補A-Dの中から、2ページの研究構想書に使う概念を1つ選ぶ
6. [ ] Apache NuttXのIssue/PR データを予備分析（非専門者の障壁の定量的エビデンス）
