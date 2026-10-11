# 科室研究脉络

给临床医生和研究者看的学科研究地图。每份报告按研究方向回答同一组问题：这个方向从哪里起步，哪些证据或方法让它转了向，哪些路线并存、哪些被否定，近五年在研究什么、用什么数据，还有什么不知道。

这些报告不是系统综述，也不是 Meta 分析：没有重新计算合并效应量，不对任何疗法给出推荐，不能用作患者的诊疗建议。

## 现有一份

| 科室 | 范围 | 研究截止日 | 规模 | 从这里读 |
|---|---|---|---|---|
| 烧伤整形科 | 12 个研究方向，另加中国烧伤整形学科史 | 2026-09-29 | 13 章正文；证据表 1,008 行，涉及 953 个不同的 PMID | [烧伤整形科/README.md](烧伤整形科/README.md) |

## 引用在哪里

- **烧伤整形科**：各章第 9 节是这一章的节点速查表。关键节点、近期代表研究、入口综述等共 1,008 行汇总在 D 关键文献证据表里（按方向分成 13 个 Markdown 文件，另有一份完整的 CSV）。1,008 行里有 1 行查不到标识，其余每行都带 PMID、DOI 或网址；每行都标明这条证据实际读到了哪一层。各章行文里另有几百篇只带 PMID 提到的文献，不在这张表里。

## 用之前请先知道

1. **报告由 AI 代理流程产出，核查也由 AI 代理完成。** 多个 AI 代理分工检索、起草、互相核查后成稿。烧伤整形科报告里说的核查员、抽查员、「第二人」，指的都是 AI 代理，不是人。本仓库没有临床专家审定这些报告的记录。拿它当依据之前，请回到原始文献核对。
2. **每条证据都标了实际读到的程度。** 从 L0（只见到二手转述）到 L4（通读全文）共五层，各报告开头有定义。按报告的写作规则，只见到二手转述或只核到题录的文献，不应写成已经核对过原文；发现例外请指出。
   烧伤整形科的证据表里，1,008 行中有 728 行由另一个 AI 代理逐条核对过，280 行只由写稿的代理自己核对。另做过一次 79 行的分层随机抽查，没有发现实质错误；这只是抽样估计，不代表每一行都被复核过。
3. **覆盖有缺口，报告里逐项写明了。** 最大的几处是：
   - 没有检索中文数据库（知网、万方）。
   - 1950–1970 年代的苏联文献基本没有覆盖；一批付费墙后面的奠基原文只核到题录；13 个条目里有 1 个只算部分完成（创面愈合与慢性创面）。
4. **报告有截止日，截止日之后的文献没有纳入。**

## 发现错误怎么办

欢迎在 [Issues](https://github.com/TerryFYL/research-lineage/issues) 里指出，最好附上 PMID 或 DOI，以及原文的页码或段落。

## 许可与署名

报告的文字、表格和图以 [CC BY 4.0](LICENSE) 许可公开：可以转载、改编和商用，但要署名并注明出处。建议的写法：

> AI Research Army. 科室研究脉络（烧伤整形科）. 2026. https://github.com/TerryFYL/research-lineage

报告里引用的第三方文献，版权归原作者和出版方所有。本仓库收录的是题录信息和对文献内容的转述，另有为核对而保留的少量原文短句。

## 相关项目

这份报告出自 [AI Research Army](https://github.com/TerryFYL/ai-research-army) 项目。

## English summary

Research lineage maps of clinical specialties, written in Chinese: burn and plastic surgery. For each research direction the reports trace where it started, what evidence or methods changed its course, which lines coexist or were abandoned, what the last five years have focused on, which data were used, and what remains unknown. Every piece of evidence carries an explicit reading level (from second-hand mention to full text read). The burn report cites its sources with PMID, DOI or URL (one row out of 1,008 has none). The reports were produced and checked by AI agents; this repository holds no record of review by clinical experts. They are not systematic reviews and not clinical advice. Licensed under CC BY 4.0.
