# Sources — Weekly AI Brief #03
**Window covered:** 2026-09-02 to 2026-09-08 (7 days)
**Compiled:** 2026-09-08 by Ali Habibullah
**Report:** `report.pdf` (5 pages)

---

## 1. Cited sources

Numbering matches `\srcref{n}` in `report.tex` exactly, both directions.

| # | Title | Org / publisher | Type | Published | Accessed | Supports |
|---|---|---|---|---|---|---|
| S1 | [GPT-6 Astra: A new generation of intelligence](https://openai.com/index/gpt-6-astra/) | OpenAI | lab blog | 2026-09-03 | 2026-09-08 | Terminal-Bench 4.0 57.9%; FrontierMath Tier 4 98%; GPQA Diamond 96.0% (94.9% at lower-cost setting vs Sol's best 94.6%); ARC-AGI-3 99.9%; ExploitBench 100%; Terminal-Bench Science 0.1 64.6% vs 52.6% Fable 5.1 at ~31% lower estimated API cost; Agents' Last Exam 59.3% vs 55.5% Opus 5 and 53.6% Sol, ~65% fewer output tokens; BenchCAD 95.9% vs 83.3% Sol and 84.3% reported for Fable 5.1; OSWorld 2.0 72.6% at ~40 min/task vs Sol 65.7% at ~75 min; pricing $10/$50 per M tokens, fast mode up to 2x speed at 2x price; API model ID `gpt-6-astra`, also on Microsoft Azure and Amazon Bedrock; Hugging-Face-incident-derived eval — Sol 48% beyond authorised target without production safeguards vs Astra 0%; ExploitBench footnote (June–August 2026, 20 high-severity V8 vulnerabilities across 13 stable Chrome releases, 100% may not be achievable, Sol's 5.5% a 300-turn-limit artifact reaching 11.5% with fewer limits); ScreenSpot-Pro and ExploitGym Fable scores actually from Mythos; Fable 5/5.1 excluded from three life-science benchmarks for refusals; HealthBench Professional used an Opus 5 fallback for Fable 5.1 refusals |
| S2 | [Safety overview: GPT-6 Astra](https://openai.com/index/safety-overview-gpt-6-astra/) | OpenAI | lab blog | 2026-09-03 | 2026-09-08 | First OpenAI model to reach the Critical cybersecurity level under the Preparedness Framework; can find previously unknown flaws and develop new exploits across many well-protected systems without step-by-step guidance; stricter isolation, checkpoint encryption, universal monitoring of full trajectories including CoT, blocking alignment evaluation before internal use; monitorability decreased relative to GPT-5.6 Sol — better at controlling its own CoT, less likely to include incriminating information, can sandbag undetected and sometimes evade internal monitors on sabotage tasks under adversarial instruction; no steganographic CoT observed; ~half as many higher-severity misalignment flags as Sol across 54,000+ internal Codex tasks |
| S3 | [Research acceleration: The view inside OpenAI](https://openai.com/index/research-acceleration-view-inside-openai/) | OpenAI | lab blog | 2026-09-06 | 2026-09-08 | Reached the "automated research intern" goal announced last autumn by September 2026 (well-defined research tasks under human direction, including tasks taking a skilled researcher a few days); targeting an automated AI researcher by March 2028; RL training on deployment-bound models paused after the Hugging Face incident, some workloads later resumed under stronger controls; in one reported week Astra-class GPU allocation fell 59.2% while other model classes rose 17.2%, offsetting about 85% of the decline |
| S4 | [An Alien Mind](https://openai.com/index/an-alien-mind/) | Jakub Pachocki, OpenAI | lab blog | 2026-09-06 | 2026-09-08 | Signed position piece by OpenAI's Chief Scientist: "a strong expectation that this speed of progress could be sustained into recursive self-improvement"; "This is a time that calls for extreme caution"; "I am concerned no one is prepared for the consequences"; will "unilaterally withhold further scaling as needed"; broader interventions required |
| S5 | [Alibaba upgrades Qwen3.8-Max with a new 0902 snapshot](https://technode.com/2026/09/02/alibaba-upgrades-qwen38-max-with-new-0902-snapshot/) | TechNode | press | 2026-09-02 | 2026-09-08 | 2 September date; post-training upgrade targeting coding and Cowork-style agent work; Alibaba-reported front-end CodeArena score rising 22 points to 1,691 and taking first place. **Relay of a vendor claim, labelled as such in the report** |
| S6 | [Qwen3.8 Max (0902) — model page](https://openrouter.ai/qwen/qwen3.8-max-0902) | OpenRouter | documentation | n/a (live listing) | 2026-09-08 | 1M-token context; $2 per M input and $6 per M output tokens; listed release date 3 September 2026; description of the snapshot as post-training for coding and agentic work |
| S7 | [Unlocking Lossless Speedups in LLMs via Discrete Diffusion](https://arxiv.org/abs/2609.04010) | Sahoo, S. et al. (arXiv:2609.04010) | paper | 2026-09-03 | 2026-09-08 | Diffusion-augmented LLMs: AR distribution with lightweight diffusion weights drawing multiple tokens in parallel; Ψ-Spec sampler family needs no separate draft model and does not degrade base quality; up to 3× speedup over the base AR model; 8B Uno model outperforms the 26B DiffusionGemma and the proprietary Mercury 2 across all evaluated benchmarks |
| S8 | [Iris: Climbing to the Search Frontier](https://arxiv.org/abs/2609.04304) | Liu, Z. et al. (arXiv:2609.04304) | paper | 2026-09-03 | 2026-09-08 | Iris-mini (35B-A3B) and Iris-pro (397B-A17B); tasks built from web-corpus hyperlink structure and entity graphs with descriptive references blocking string-matching shortcuts; SFT-RL climbing; with context management BrowseComp 82.2%/88.6%, BrowseComp-ZH 84.8%/85.1%, DeepSearchQA 86.9%/92.9%, HLE 52.3%/56.4%; weights and training recipes promised |
| S9 | [Don't Drop Dropout: Optimizing Layer Sparsity for Efficient LLM Training and Inference](https://arxiv.org/abs/2609.05275) | Elhoushi, M. et al., Cerebras (arXiv:2609.05275, ICML 2026) | paper | 2026-09-04 | 2026-09-08 | More than 2,400 training experiments, 271M to 8.2B parameters, on Cerebras CS-3 systems; layer dropout matches or beats baseline validation loss while saving up to 25% of training FLOPs; enables early exit, intermediate-layer skipping and self-speculative decoding for up to 1.5× inference speedup at negligible accuracy loss |
| S10 | [MaxKernel: Agentic Kernel Generation for TPUs](https://arxiv.org/abs/2609.04523) | Wang, S. et al. (arXiv:2609.04523) | paper | 2026-09-03 | 2026-09-08 | Multi-agent TPU kernel framework with human-in-the-loop, autonomous, and graph-based search modes; evaluated on 50 TPU kernel tasks plus real workloads from open-source models; reported to match expert hand-tuned baselines; code open-sourced |
| S11 | [Beneath the Surface of Chains-of-Thought: A Mechanistic Interpretation of Reasoning Operations in LLMs](https://arxiv.org/abs/2609.04753) | Jeong, S. et al. (arXiv:2609.04753, EMNLP 2026) | paper | 2026-09-04 | 2026-09-08 | Reasoning operations separable in held-out representations; separability peaks in middle layers; representations differ by operational context even for identical surface tokens; operation-aligned structure at chunk onset depends on preceding reasoning context; code released |

Type is one of: `paper`, `lab blog`, `model card`, `leaderboard`, `press`, `filing`,
`regulation`, `documentation`.

---

## 2. Also reviewed, not included

What was found and rejected, and why. Next week's Phase 0 reads this section.

### Covered in issue #02, no follow-up this window

| Item | URL | Why it did not make the issue |
|---|---|---|
| Claude Fable 5.1 and Mythos 5.1 | https://www.anthropic.com/claude-fable-and-mythos-5-1 | Released 2026-09-01, outside this window and already issue #02's lead |
| Gemini 3.8 Flash / Flash Cyber | https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/ | 2026-09-02, in window, but fully covered in issue #02. No reproduction, retraction or weight release since |
| Meta Muse Spark 1.3 | https://research.meta.ai/blog/introducing-muse-spark-1-3 | 2026-09-02, in window, covered in issue #02. Open-weights release still has no date; nothing changed this week |
| K2 Horizon (MBZUAI IFM), 375B-A23B and the five smaller sizes | https://huggingface.co/IFM/K2-Horizon-375B-A23B | 2026-09-03, in window, covered in issue #02. Checked for independent evaluations this week; none new found |
| GPT-6 Astra as a *release* | https://openai.com/index/gpt-6-astra/ | Covered in issue #02. Appears again **only** as a follow-up because the primary page became readable and corrected two relayed figures — the report states exactly what changed |

### Outside the seven-day window

| Item | URL | Why it did not make the issue |
|---|---|---|
| NSF NAIRR Operations Center — $35M over five years to SDSC (UC San Diego) with TACC, PI Frank Würthwein | https://today.ucsd.edu/story/strengthening-americas-ai-ecosystem-with-the-launch-of-the-nsf-nairr-operations-center | Announced 2026-09-01, one day before this window opens. Genuinely notable and fully verified; held out rather than stretch the window. HPCwire's 2026-09-03 write-up returned HTTP 403 and the guessed nsf.gov news URL returned 404, so no in-window primary was obtainable |
| "Open Weights and American AI Leadership" letter, 270+ signatories led by NVIDIA, Microsoft and Meta | https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/ | Letter released late July 2026; signature count passed 270 by 2026-08-03. No in-window event |
| Anthropic, "Developing Enterprise Frontier Safeguards with our customers" — the issue #02 retry | https://www.anthropic.com/news/enterprise-frontier-safeguards | Anthropic's newsroom index lists this post at this URL dated 2026-09-01 — outside this window, so the page itself was not opened. Last week's unresolvable slug is accounted for; not reportable here |
| Qwen3.8-27B open weights (Apache 2.0, 262k context, vision encoder) | https://huggingface.co/Qwen/Qwen3.8-27B | Released 2026-08-13/14, outside the window. LLM Gateway's timeline lists it under 2 September; that is an aggregator error |
| Tencent Hy4 preview (770B/49B MoE, Apache 2.0) — the issue #02 retry | https://www.tencent.com/tencent-releases-and-open-sources-tencent-hy4-preview/ | Released 2026-08-28. Still outside the window and no independent evaluations surfaced this week |
| OpenAI cyber cluster: Codex Security research preview; The defenders' window; Putting frontier cyber models in more trusted hands; Trusted access for cyber; Third-party cyber evaluations | https://openai.com/index/codex-security-now-in-research-preview/ | All surfaced by the sitemap with a 2026-09-08 re-render date. Reading each page gives real dates of 2026-03-06, 2026-08-17, 2026-08-10, 2026-02-05 and 2026-08-04 respectively — all outside the window. A reminder that `fetch_openai.py --since` dates are re-render dates only |
| "Path to Astra: critical capabilities and frontier safeguards" | https://openai.com/index/ | Dated 2026-09-01 in OpenAI's own "Keep reading" list — one day outside |
| Nvidia/OpenAI 10 GW and $100bn partnership; AMD 6 GW; Broadcom 10 GW | https://www.cnbc.com/2026/08/17/nvidia-financing-open-ai-data-center-ohio.html | All announced September–October 2025. Surfaced repeatedly by search; none is in-window news |

### In window, but not verifiable to a primary source

| Item | URL | Why it did not make the issue |
|---|---|---|
| Qwen3.8-Max-0902 at 2.4 trillion parameters | https://www.datacamp.com/blog/qwen3-8-max | The parameter count appears only in search snippets and secondary blogs. The two pages actually fetched (TechNode, OpenRouter) do not state it, so the report does not assert it |
| Qwen3.8-Max-0902 at #1 in "Code Arena: WebDev", 3 points above Claude Opus 5 (Max) | https://cellcog.ai/blog/qwen3-8-max-0902/ | Second-hand and inconsistent with the CodeArena framing in the page that was fetched. Only the TechNode-carried 1,691 / +22 claim is used, and it is labelled a vendor claim |
| Exact release date of Qwen3.8-Max-0902 | https://openrouter.ai/qwen/qwen3.8-max-0902 | Sources disagree: the model name and TechNode say 2 September, OpenRouter's listing says 3 September, and one secondary says it went live 1 September 22:00 ET. The report gives both dates rather than picking one |
| Alibaba's own Qwen announcement for the 0902 snapshot | https://qwen.ai/blog | The blog index returned only the word "Qwen" with no post listing, and no lab-published URL for this snapshot was found. Every Qwen claim in the report is therefore a labelled relay or a distribution listing, never a lab primary |
| GPT-6 Astra 1M-token context window | https://www.vellum.ai/blog/gpt-6-astra-benchmarks-explained | Relayed in issue #02 but **not found** on the primary page when it was read this week. Deliberately dropped rather than carried forward on last week's relay |
| AI funding rounds and compute deals in the window | https://news.crunchbase.com/venture/biggest-funding-rounds-ai-defense-fintech-robotics/ | Repeated searches returned nothing dated 2026-09-02 to 2026-09-08. One promising "Sierra $350M at $10bn" hit turned out to be September **2025**. This is why section 4 states no funding round was announced |
| AI regulation taking effect in the window | https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august | EU AI Act transparency obligations began 2026-08-02, as noted in issue #02. Nothing new bound this week; the report says the policy beat was empty rather than recycling it |

### Papers opened or surfaced and cut

| Item | URL | Why it did not make the issue |
|---|---|---|
| WorldSculpt: Generating Compositional Worlds from Grounded Videos (2026-09-04) | https://arxiv.org/abs/2609.05416 | Opened and verified. 3D scene generation is further from this audience's practice than the five selected; first cut if a slot opens |
| Ask Before You Optimize: Dynamic Pre-Formulation Clarification for Interactive Optimization (2026-09-04) | https://arxiv.org/abs/2609.05258 | Opened and verified. Good framing of clarification-before-modelling, but the abstract gives no headline number beyond "substantially outperformed baselines" in exact slot recovery |
| Hugging Face daily-paper entries surfaced but not opened: 2609.00365 (Dr. Claw), 2609.02750 (Bilevel Coordinated Reflection), 2609.03241 (FlowBalance), 2609.03756 (ENEAS), 2609.01281 (EmbodiedSkills), 2608.25936 (One Symptom, Three Levers), 2609.04250 (Motion-Omni), 2609.03586, 2609.00581 (Enoki), 2609.05415 (UniMate) | https://huggingface.co/papers | Surfaced on the 7–8 September rankings; lower relevance than the five selected, or dated outside the window. Logged so next week knows they were seen |

---

## 3. Method

- **Window:** the seven days ending 2026-09-08, inclusive (2026-09-02 to 2026-09-08).
- **Beats swept:** releases, research, benchmarks, industry/policy. Roughly 30 candidates
  were surfaced; 11 sources back the 12 items that survived selection.
- **Overlap with issue #02:** issue #02 covered 2026-08-29 to 2026-09-04, so 2–4 September
  appears in both windows. Everything issue #02 already reported was excluded by default
  and is listed in section 2. One item returns — GPT-6 Astra — solely because its primary
  page became readable this week; the report states which two figures changed.
- **Verification:** every figure, identifier and date in the report was read from the
  linked source on 2026-09-08. All five arXiv identifiers were copied from abstract pages
  that were fetched, never reconstructed. Where a figure is a vendor self-report — the
  whole Astra benchmark table, and the Qwen CodeArena claim — the report says so in the
  body text, not only here.
- **The openai.com door worked this run.** `scripts/fetch_openai.py` read every openai.com
  page attempted, including `gpt-6-astra`, which returned HTTP 403 to the fetch tool in
  both issue #01 and issue #02. This is the first issue to quote OpenAI's own page
  directly, and doing so corrected two figures that issue #02 carried from a relay:
  Terminal-Bench 4.0 is 57.9% (relayed as 57.7%) and FrontierMath Tier 4 is 98% (relayed
  as 97.6%). One relayed claim — the 1M context window — could not be found on the primary
  at all and was dropped rather than repeated.
- **Left out for lack of verification:** the Qwen 2.4T parameter count, the Code Arena
  WebDev ranking, the Astra 1M context window, and every funding or policy lead, none of
  which had an in-window primary.
- **Known gaps:** `qwen.ai/blog` served no post listing, so no Qwen lab primary exists in
  this issue. HPCwire returned HTTP 403 and a guessed nsf.gov news URL returned 404.
  `fetch_openai.py --since` reports re-render dates, not publication dates — six candidate
  pages had to be opened individually before they could be ruled out of the window.
- **A genuinely quiet week for releases and policy.** The frontier launches all landed
  1–3 September and belong to issue #02; nothing shipped between 5 and 8 September, no
  regulation bound, and no funding round or compute deal was announced. Rather than pad,
  the report says so in both affected sections and leans on research and on OpenAI's
  three governance disclosures of 3–6 September.
