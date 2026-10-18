# 中医心内科研究脉络报告

> **状态声明**：本报告不是完整版。13 个条目（12 个方向 + 1 个学科史横切条目）中，13 个条目自评与统一评级为"基本完整但有标注缺口"。**全报告最大的共同缺口**：CNKI/万方未检索——本科室文献的大头在中文库，1972–1982 年的奠基文献（冠心2号 1972、精制冠心片 1982、血瘀证标准 1982/1986/1989 等）本轮只到题录或转述层；各章第 8 节有本章的具体影响说明。另一共同缺口：ChiCTR 注册库不可程序化访问，注册终点核对依赖 ClinicalTrials.gov 与论文全文。
>
> **这仍然是一份可用的报告**：87 行证据分层抽查 0 行实质错误（95% 置信上限约 3.4%）、全报告复核与两轮修订的留痕都在各章"## 12 复核修订记录"。
>
> **依据**：`docs/strategy/科室研究脉络-方法论.md`（2026-10-02 版）。这是该方法**第二次实跑**（第一次烧伤整形科，2026-09-29），第一次换科室实跑。执行器为 ZCode（Agent 子代理承担方法论里的五个工作流角色，移植件 `scripts/zcode_prompts*.py`）。

## 三个时间口径

| 口径 | 值 | 用在哪 |
|---|---|---|
| 报告截止日 | **2026-10-17** | 全部"截至"表述 |
| 近期重点窗口 | 2021-10-17 至 2026-10-17 | 只用于各章"近五年重点"与 E 的近期计数 |
| 文献统计窗口 | PubMed 全部年份至 2026-10-17 查询日；年度图只画 1990–2025 完整年份 | 只用于 E 与完整性检查的判断依据 |

## 从哪里读起

- **只想知道"这个方向怎么回事"**：读 `A_科室研究总览.md` 的 A2 表中该行 → 该章第 0 节三分钟速读。
- **要引用数字**：先到 `D_关键文献证据表.csv` 找行 → 按 result_location 回原文 → 注意 reading_level 与 verification_status。
- **要查事件/年份**：`directions/X01_中国中医心内科学科史.md` 第 9 节事件底账（39 行，按核实状态分列）。
- **想知道方向之间怎么互相影响**：`C_时间线与分支图.md`（C1 分支图、C3 关系表、C4 八次转向、C5 因果冲突）。
- **想知道数量与期刊格局**：`E_文献数量与期刊背景.md`。
- **想审这份报告是怎么做出来的**：`F_检索选读排除与覆盖状态.md`（检索日志 908 条、排除 103、待核线索 99、缺口 148、逐方向覆盖表、抽查与复核统计、过程偏差 10 条）。

## 阅读层级与全表统计

L0 仅二手转述 / L1 题录已核 / L2 摘要已读 / L3 原文部分章节已读 / L4 全文已读；一行多层级按最低计。全表 585 行，分布见 `data/evidence_stats.json`（层级分布逐方向列出）；证据行抽查 87 行（分层随机，种子 20261018，10 行无标识强制加入）：**正确 74、小误差 7、实质错误 0、无法核实 6**；跨章事实一致性比对 28 类实体、冲突 14 处（实质 9/表述 5，全部两轮处置）；同一文献跨章比对 23 篇、字段不一致修订后余 5 处（均为作者写法差异）。

## 交付物

| 交付物 | 文件 |
|---|---|
| A 一页总览 | `A_科室研究总览.md` |
| B 各方向章节 | `directions/D01…D12、X01_*.md`（第 0–10 节 + 第 12 节复核修订记录） |
| C 时间线与分支图 | `C_时间线与分支图.md` |
| D 证据表 | `D_关键文献证据表.csv` / `.md`（585 行） |
| E 数量与期刊背景 | `E_文献数量与期刊背景.md`（图 `figures/E1_年度记录数.png`、`E2_年度占比.png`） |
| F 检索与覆盖记录 | `F_检索选读排除与覆盖状态.md` |

## 脚本清单（`scripts/`，全部可重跑）

统计：`run_e_part.sh`（pubmed_counts / pubmed_totals / pubmed_pmids_journals / journal_background / plot_counts）；质检：`qa_chapters.py`、`check_cross_pmid.py`、`check_mermaid.mjs`（mermaid 环境在 `data/_cache/mermaid_check/`）；合成：`build_evidence_table.py`、`build_c_tables.py`、`build_f_records.py`、`build_f5_table.py`、`annotate_c2_levels.py`、`draw_audit_sample.py`、`sample_query_noise.py`；检索式：`queries.py`（噪声抽样记录在文件头）、`report_config.py`；执行层（ZCode 移植件）：`zcode_prompts.py`（逐方向流水线）、`zcode_prompts_qa.py`（全报告复核）、`zcode_prompts_fix.py`（分章修订/完整性检查/最终修订）。`workflows/0x_*.js` 是 Claude Code Workflow 版原件，本次未运行（提示词已在 zcode_prompts*.py 中按本科室改写）。

## 中间材料说明

`data/pipeline/` 存各阶段代理的结构化输出（research/verify/critic/write/fix1/fix2 与 QA 五件）；`data/_cache/` 存 PMID 缓存、mermaid 检查环境与代理中间材料（gitignore，不入库但保留在磁盘）。复核结果：`data/qa_audit_rows.json`、`qa_facts.json`、`qa_relations.json`、`qa_cross_pmid.json`、`qa_chapters.json`、`qa_completeness.json`（第 9 步后）。

## 过程偏差

10 条，见 `F_检索选读排除与覆盖状态.md` 的 F8（要点：D05/D07 两次被模型服务限流/过滤中断后凭逐条检索日志续跑成功；`sample_query_noise.py` 命中 <1000 时需 `--retstart 0`；英文 "blood stasis" 双义导致证候检索式三轮收窄；ZCode 无 Workflow 工具的执行器差异与并发上限 8）。
