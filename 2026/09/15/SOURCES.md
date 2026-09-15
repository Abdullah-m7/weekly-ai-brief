# Sources — Weekly AI Brief #04
**Window covered:** 2026-09-09 to 2026-09-15 (7 days)
**Compiled:** 2026-09-15 by Ali Habibullah
**Report:** `report.pdf` (5 pages)

---

## 1. Cited sources

Numbering matches `\srcref{n}` in `report.tex` exactly, both directions.

| # | Title | Org / publisher | Type | Published | Accessed | Supports |
|---|---|---|---|---|---|---|
| S1 | [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution/) | OpenAI | lab blog | 2026-09-08 (updated 2026-09-10) | 2026-09-15 | Internal model "significantly more capable than GPT-6 Astra"; fluid from rest under smooth force develops unbounded velocity in finite time with bounded energy; establishes statements C and D of the Clay formulation; Lean formalization on GitHub (`openai/NavierStokesAndEuler`); effort began 1 September after rumours two Millennium problems were resolved; group "on the order of 10,000 concurrent agents"; result reached Saturday 5 September, ~88 hours after launch; Lean verification 17 hours via GPT-6 Astra; 2.7M messages and ~130B output tokens for Navier–Stokes, 4.9M messages and ~300B tokens across all problems; "nearly 100 agents" for ~50 hours on unforced Euler; OpenAI "do not intend to claim the Millennium Prize"; 10 September update: investigation found Buckmaster's Codex prompts "could not have influenced the system in any way, including through training". Read via `scripts/fetch_openai.py` |
| S2 | [Finite time blowup for Navier–Stokes](https://cdn.openai.com/pdf/32d9f210-8b73-45e0-91bc-82a30aef8a9a/navier-stokes.pdf) | OpenAI | paper | 2026-09-08 | 2026-09-15 | Page count 166 (counted with PyMuPDF); Theorem 1.1: for every viscosity ν > 0, a smooth compactly supported force and zero initial velocity give bounded L² energy and unbounded L∞ velocity as t ↑ 1 |
| S3 | [Statement](https://cims.nyu.edu/~tristanb/statement.pdf) | Tristan Buckmaster, NYU | statement (primary) | 2026-09-08 | 2026-09-15 | Three results released (IPM, Boussinesq, 3D Euler with smooth forcing), Lean-verified; credit to Córdoba and Martínez-Zoroa; Euler/Boussinesq blowup obtained 15 August, Lean-verified 22 August; used "Anthropic's Claude, OpenAI's Codex, especially with GPT-5.6 Sol and, more recently, Astra"; 3 September email to an OpenAI mathematician; two calls on 6 September with Sébastien Bubeck; told proof is "about 100 pages"; two proposals (sequenced release; sole-authored paper without Alpöge), both declined; "I have not seen OpenAI's proof … I am not accusing anyone of anything. I am stating what I was told, when, and what was proposed to me." Date taken from the OpenAI page ("paper on September 8, 2026") and the statement's own "last 24 hours" wording relative to 7 September |
| S4 | [Blowup for the Euler equations with smooth forcing](https://cims.nyu.edu/~tristanb/euler.pdf) | Alpöge, L. and Buckmaster, T. | paper | 2026-09-08 | 2026-09-15 | 112 pages (counted with PyMuPDF); abstract: finite-time singularity for incompressible Euler on R³ with a force smooth in space and time up to and including blowup; continues the Córdoba–Martínez-Zoroa program |
| S5 | [Navier-Stokes announcement](https://www.claymath.org/news/navier-stokes-announcement/) | Clay Mathematics Institute | statement (primary) | 2026-09-11 | 2026-09-15 | "the announcement that the Navier-Stokes problem has apparently been settled"; "The rules governing the prizes describe the process for evaluating what has been achieved and for assigning credit. The process is deliberately unhurried, but we will provide updates."; no author named |
| S6 | [Introducing DeepSeek-V4.1-Flash](https://www.deepseek.com/en/news/deepseek-v4-1-flash/) | DeepSeek | lab blog | 2026-09-10 | 2026-09-15 | Release date; "New Causal Encoder–Decoder architecture"; 552B MoE, 8B active for input / 16B for output; KV cache 1/4 HBM and 1/8 SSD vs previous generation; API model ID `deepseek-flash`; weights on Hugging Face; from 04:00 UTC 14 September all `deepseek-v4-pro` requests route to V4.1-Flash |
| S7 | [DeepSeek-V4.1-Flash model card](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) | DeepSeek | model card | n/a (live page) | 2026-09-15 | MIT licence; 552B backbone, 8B/16B active per token prefill/decode; 40-layer transformer as 20-layer causal encoder + 20-layer decoder; 1M context; 45T-token multimodal pre-training; CSA2 with global KV cache 890 bytes/token, ~1/4 of V4-Flash; instruct results at `reasoning_effort=100`: Terminal-Bench 2.1 90.6 vs Opus-5.0 89.1, GPT-5.6 Sol 88.8, V4-Pro 87.9; Terminal-Bench 4.0 31.2 vs 51.8 / 39.9 / 12.4; DeepSWE v1.1 74.2 vs 74.0 / 73.0 / 62.7; GPQA Diamond 90.9 vs 93.4 / 94.1 / 92.4; HLE 36.8 vs 56.3 / 44.5 / 42.7 |
| S8 | [Models & Pricing](https://api-docs.deepseek.com/quick_start/pricing) | DeepSeek | documentation | n/a (live page) | 2026-09-15 | `deepseek-flash`: context 1M, max output 384K; peak: cache hit $0.006, cache miss $0.30, output $1.20 per 1M tokens; off-peak half of peak; peak hours 01:00–04:00 and 06:00–10:00 UTC Mon–Fri |
| S9 | [DeepSeek V4.1 Flash (max)](https://artificialanalysis.ai/models/deepseek-v4-1-flash) | Artificial Analysis | leaderboard | n/a (live page) | 2026-09-15 | 40 on Artificial Analysis Intelligence Index v4.3 (10 evaluations incl. Terminal-Bench v4.0, HLE, SciCode); released 10 September 2026; 214.4 output tokens/s, TTFT 1.12 s on DeepSeek's API; $0.30 / $1.20 per 1M; #6 of 113 open-weights models on intelligence, #4 of 113 on speed |
| S10 | [DeepSeek V4 Flash 0731 (max)](https://artificialanalysis.ai/models/deepseek-v4-flash) | Artificial Analysis | leaderboard | n/a (live page) | 2026-09-15 | 35 on the same Intelligence Index v4.3; released 31 July 2026 — gives the "five points above the previous Flash" comparison on one index version |
| S11 | [Build more natural voice experiences with GPT-Live-1 in the API](https://openai.com/index/introducing-gpt-live-1-in-the-api/) | OpenAI | lab blog | 2026-09-10 | 2026-09-15 | $0.05 per minute for the front-end voice layer, backend model billed separately; listens and speaks simultaneously; delegates reasoning/tool calls to GPT-6 Astra or a third-party model; telephony, ASR transcripts, keyword biasing, native turn detection; +30 percentage points on Full Duplex Bench over GPT-Realtime-2.1; #1 on Tau3 paired with Astra (medium). Read via `scripts/fetch_openai.py` (needed three attempts — archive fallback returned 429 twice) |
| S12 | [Introducing the Agents API](https://openai.com/index/introducing-the-agents-api/) | OpenAI | lab blog | 2026-09-10 | 2026-09-15 | Public beta; single API call specifying task, model, tools, environment; OpenAI hosts the harness (orchestration, context compaction, recovery, subagents); environments: OpenAI-hosted sandbox, own VPC, or partners Blaxel, Cloudflare, Daytona, DigitalOcean, E2B, Modal, Oracle, Runloop, Vercel; "no additional fees … you simply pay for the tokens and tools"; powered by the open-source Codex harness; SafetyKit testimonial "60% reduction in cost per case". Read via `scripts/fetch_openai.py` |
| S13 | [NCP-ArchPreview Technical Report: Moving towards Latent Space Language Models through Next Concept Prediction](https://arxiv.org/abs/2609.10715) | Intern-NCP Team (arXiv:2609.10715) | paper | 2026-09-09 | 2026-09-15 | 8.9B parameters, 5.73T Dolma-3 tokens; product-quantized concept vocabulary from hidden states; reaches OLMo-3-7B's final pre-training loss with 51.3% of the tokens; +2.45 average downstream, +5.99 GSM8K; abstract does not state a weights release |
| S14 | [An Open Recipe for IMO Gold: Training Nemotron for Olympiad Mathematics](https://arxiv.org/abs/2609.10712) | Moshkov, I. et al. (arXiv:2609.10712) | paper | 2026-09-09 | 2026-09-15 | From Nemotron 3 Ultra via SFT and RL; 30 of 42 points at IMO 2026 (gold) in natural language without formal provers or tools; released: two checkpoints, training data, training and inference code, submitted solutions, Nemotron-IMO-Bench (200 problems) |
| S15 | [ZGCM-1: A Fully Open and Extremely Efficient Foundation Model for Math and Agentic Search](https://arxiv.org/abs/2609.13356) | He, J. et al. (arXiv:2609.13356) | paper | 2026-09-11 | 2026-09-15 | 7B from scratch; 256K context; interleaved gated sliding-window and full attention; FP8 Muon optimizer; ~4.2× efficiency in 16K pre-training time-to-loss; releases weights from pre-/mid-/post-training, intermediate checkpoints, training code, per-stage data and recipes, W&B logs; CC BY 4.0 |
| S16 | [SWE-Bench Pro Verified: A Reliable Benchmark for Software Engineering Agents](https://arxiv.org/abs/2609.08149) | Zheng, P. et al. (arXiv:2609.08149) | paper | 2026-09-08 | 2026-09-15 | Reward hacking via leaked gold solutions / hidden evaluation information; misleading problem statements, improperly scoped tests; anti-hacking safeguards plus task refinement; "some models perform substantially worse than previously reported"; no per-model numbers or artifact link in the abstract. Submitted one day before the window; surfaced on Hugging Face daily papers 2026-09-10, which the report states |
| S17 | [Detecting and countering misuse of AI: September 2026](https://www.anthropic.com/threat-intelligence-report-september-2026) | Anthropic | lab blog | 2026-09-10 | 2026-09-15 | Period December 2025 – August 2026; seven domains (cyber, surveillance, influence, conventional weapons, biological misuse, scams and fraud, illicit distillation); Midnight Blizzard-linked operator, 20+ organisations, 300,000+ national identity records; Chinese-speaking group ~50 organisations, "a dozen possible zero day findings in a single month"; France-based LKM Company ~70 fabricated news sites, 8,913 articles in ~20 languages; "None of the misuse cases involved the use of Claude Fable or Mythos-class models, with the exception of one illicit distillation case." Date from the anthropic.com/news index |
| S18 | [Paul Christiano joins OpenAI Foundation Board](https://openai.com/index/paul-christiano-joins-openai-foundation-board/) | OpenAI | lab blog | 2026-09-09 | 2026-09-15 | Foundation Board appointment; non-voting observer on OpenAI Group PBC board; joins Safety and Security Committee chaired by Zico Kolter; Senior Technical Advisor at CAISI (NIST); footnote: recuses from all OpenAI-related matters and model evaluations. Read via `scripts/fetch_openai.py` |
| S19 | [Saudi AI giant races to fund data center expansion](https://fortune.com/2026/09/09/saudis-humain-turns-to-outside-investment-as-the-kingdom-reins-in-fiscal-spending/) | Fortune | press | 2026-09-09 | 2026-09-15 | Bloomberg-reported (relayed by Fortune) $2.5bn fund for Saudi data-centre expansion; Saudi capacity 467 MW in Q1 2026; Humain target 1.9 GW by 2030; CEO Tareq Amin's plan to list in Saudi Arabia and New York by 2029. **Labelled a reported fundraising, not a closed one, in the body text** |
| S20 | [NVIDIA to Acquire Hugging Face](https://blogs.nvidia.com/blog/nvidia-to-acquire-hugging-face/) | NVIDIA | press release | 2026-09-03 | 2026-09-15 | Deal value $12,930,300,000; "Hugging Face will remain an open platform for the entire AI ecosystem"; "NVIDIA compute will not be required to build on or deploy through Hugging Face". **Outside the window; carried with a sentence saying so because issues #02 and #03 did not record it** |

Type is one of: `paper`, `lab blog`, `model card`, `leaderboard`, `press`, `filing`,
`regulation`, `documentation`, `statement (primary)`.

---

## 2. Also reviewed, not included

What was found and rejected, and why. Next week's Phase 0 reads this section.

### Opened and verified, cut for the page budget

| Item | URL | Why it did not make the issue |
|---|---|---|
| Sakana AI, Fugu Max v1.0 and Fugu Ultra v2 (2026-09-11) | https://sakana.ai/fugu-max-release/ | Primary read: orchestration architecture over open/specialised models incl. NVIDIA Nemotron; Fugu Max $2/$6 per M; "best or joint-best on five of eight benchmarks"; Chartography 48.3 vs Opus 5 27.3 and Fable 5 29.5; DeepSWE 74.3; Ultra v2 cutoff 2026-08-28; "without Fable 5, Fable 5.1, or GPT-6-Astra in its agent pool". Cut because the page gives no full table and no Ultra v2 price, and the build was one page over budget. OpenRouter's Fugu Ultra v2 listing did not render pricing when fetched. First candidate to reinstate if a neutral evaluation appears |
| T1: Terminal Agent Reinforcement Learning for Long-Horizon Tasks (2026-09-10) | https://arxiv.org/abs/2609.11042 | 122B MoE, RL in cloud sandbox, 300+ tool calls; Terminal-Bench 2.1 43.8% → 64.0%; Long-Horizon Terminal Bench 27.9% "surpassing GPT-5.4 and GLM-5.1". Cut for the page budget; baselines are a generation old and no release is stated |
| Terence Tao, blog post on the Alpöge–Buckmaster results (2026-09-07) | https://terrytao.wordpress.com/2026/09/07/finite-time-blowup-with-smooth-forcing-term-for-the-incompressible-porous-medium-boussinesq-and-incompressible-euler-equations/ | Read; "very feasible to complete these goals in the near future"; no mention of OpenAI. Dated two days before the window and cut with the page budget |
| Negative Self-Distillation: Learning to Reason by Avoiding Flaws (2026-09-10) | https://arxiv.org/abs/2609.11699 | Opened; abstract states "outperforms OPSD" with no headline number and no code |
| Benchmark Radar: A Living Database and Search Engine for AI Benchmarks and Evaluation (2026-09-10, v2 2026-09-13) | https://arxiv.org/abs/2609.11115 | Opened; 1,283 source records, 12,916 numeric observations, site at benchmark-radar.org, CC BY-NC-SA 4.0. Useful tool, not a result; cut for space |
| SAS: Simple Attention Sparsification via End-to-End Optimization of Context Ranking (2026-09-11) | https://arxiv.org/abs/2609.13141 | Opened; no headline number in the abstract, no code stated |

### Outside the seven-day window

| Item | URL | Why it did not make the issue |
|---|---|---|
| NeoHorse-1: Towards Recursive Self-Improvement via Agentic Post-Training with Routing Harness | https://arxiv.org/abs/2609.08183 | Submitted 2026-09-08; weights on Hugging Face and code on GitHub; macro-average 58.94 → 64.87 at 4B and 65.60 → 69.04 at 9B. One day outside; strong candidate had the window allowed it |
| Eliciting Weak-to-Strong Generalization with On-Policy Reverse Distillation | https://arxiv.org/abs/2609.08798 | Submitted 2026-09-08, no code stated |
| Grouped Value Attention: Efficient KV Caching via On-Demand Key Reconstruction | https://arxiv.org/abs/2609.13285 | Submitted 2026-09-08; 45–47% fewer persistent cache scalars vs matched GQA at 350M; kernels not yet released |
| Feyospace-v1: How the Cyber Mercury Seven Trained Frontier Cyber Models | https://arxiv.org/abs/2609.08418 | Submitted 2026-09-08; 164,269 trajectories; +23.76% CyberGym; no release stated |
| Cognition AI, $2bn Series E at $48bn valuation | https://cognition.com/blog/series-e | Announced 2026-09-08 (TechCrunch and Cognition's own post both dated 8 September). One day outside; the largest AI round of the fortnight, held out rather than stretch the window |
| Quanta Magazine, "AI Has Solved One of Math's $1 Million Millennium Prize Problems" | https://www.quantamagazine.org/ai-has-solved-one-of-maths-1-million-millennium-prize-problems-20260908/ | 2026-09-08, secondary; the primaries (S1–S5) were used instead |
| Scientific American, "OpenAI claims blockbuster math breakthrough amid swirl of controversy" | https://www.scientificamerican.com/article/openai-claims-blockbuster-math-breakthrough-amid-swirl-of-controversy/ | 2026-09-08, secondary; carries Córdoba ("We're a little bit in shock") and Bubeck ("We did not use their prompt or proofs to prompt our models") quotes. Not used because the primaries carry the same facts |
| Crusoe $3bn+ at ~$30bn (2026-09-03); Gimlet Labs $300m Series B (2026-09-05) | https://blog.mean.ceo/ai-startup-funding-news-september-2026/ | Both outside the window; only surfaced via an aggregator |
| OpenAI "The Work Now Within Reach" and "Supporting journalism from classrooms to newsrooms" | https://openai.com/index/ | Listed on OpenAI's "Keep reading" rail dated 2026-09-08; not opened |
| OpenAI "The next evolution of the Agents SDK" | https://openai.com/index/the-next-evolution-of-the-agents-sdk/ | Sitemap re-render date 2026-09-15; page itself dated 2026-04-15. Not the Agents API |
| OpenAI "Introducing GPT-Live" | https://openai.com/index/introducing-gpt-live/ | Sitemap re-render date 2026-09-15; page dated 2026-07-08. The in-window item is the API release (S11) |
| Claude Fable 5.1 / Mythos 5.1, Gemini 3.8 Flash, Muse Spark 1.3, K2 Horizon, GPT-6 Astra, Qwen3.8-Max-0902 | see issues #02 and #03 | All 1–3 September; no reproduction, retraction or weight release found this week |

### In window, but not verifiable to a primary source

| Item | URL | Why it did not make the issue |
|---|---|---|
| Clay Institute president Martin Bridson quoted as calling the review "deliberately unhurried" and "absolutely rigorous" | https://www.implicator.ai/clay-institute-navier-stokes-openai-proof-claim/ | "Deliberately unhurried" appears in the CMI statement (S5); "absolutely rigorous" and the attribution to Bridson appear only in secondaries and are not used |
| OpenAI proof described as "166-page manuscript" in secondaries | https://kingy.ai/blog/navier-stokes-ai-proof-claims-dispute/ | Confirmed directly instead by downloading the PDF (S2) and counting pages |
| Sakana Fugu Ultra v2 at $5/$30 per M tokens and 1M context | https://openrouter.ai/sakana/fugu-ultra-v2 | The OpenRouter page did not render pricing or context when fetched; the Sakana page states neither. Not asserted |
| DeepSeek V4.1 Flash priced "$0.15/$0.60" | https://venturebeat.com/technology/deepseek-v4-1-flash-debuts-with-0-003-1m-off-peak-cached-input-rate-and-benchmarks-eclipsing-gpt-5-6-sol-claude-opus-5 | Those are the off-peak figures; the report gives the peak rates from DeepSeek's own pricing page (S8) and says off-peak is half |
| Humain "Horizon Ultra" laptop with Qualcomm; Humain–G42 outside capital raising | https://www.agbi.com/ai/2026/09/gulf-ai-giants-humain-and-g42-look-to-raise-outside-capital/ | Search snippets only; not opened, not used |
| Nvidia–Hugging Face EU notification strategy "not finalised" | https://globalcompetitionreview.com/article/nvidia-yet-finalise-eu-notification-strategy-hugging-face-tie | Paywalled and undated in the snippet; no in-window primary on the regulatory review |
| Brazil Senate vote (16 Sept), India review (21 Sept), California deadline (30 Sept) | https://cubbbix.com/blog/ai-regulation-september-2026-global-update | Aggregator only; none is an in-window event and none was checked against a gazette. The policy beat is therefore represented only by the Anthropic and OpenAI governance items |

### Papers surfaced on Hugging Face daily papers (9–15 September) but not opened

| Item | URL | Why it did not make the issue |
|---|---|---|
| 2609.11929 (SenseNova-U1.5), 2609.07064 (SpatialBlock), 2609.11638 (Vidu S2), 2609.14858 (Dream-RSI), 2609.15818 (Atria Dawn), 2609.14973 (PhysBrain 1.5), 2609.11977 (Occamy-1.0, 35B open weights, submitted 2026-09-04), 2609.08936 (AuK), 2609.08977 (Omni Interaction Agent), 2609.10522 (Show-Harness), 2609.10540 (Programmable World Model), 2609.08572 (AgentGrad), 2609.05903 (EvoSafeHarness), 2609.11085, 2609.10445, 2609.09113 (SAEScientist-Bench), 2609.09219, 2609.08126 (SchemeArena), 2609.12641, 2609.12945 (StepAudio 3) | https://huggingface.co/papers | Seen on the 9–15 September rankings; lower relevance than the four selected, or dated outside the window (Occamy-1.0 abstract also gives no numbers). Logged so next week knows they were seen |

---

## 3. Method

- **Window:** the seven days ending 2026-09-15, inclusive (2026-09-09 to 2026-09-15).
- **Beats swept:** releases, research, benchmarks, industry/policy. About 40 candidates
  were surfaced; 20 sources back the 13 items that survived selection.
- **Two items sit outside the window and say so in the body text.** The OpenAI
  Navier–Stokes page is dated 2026-09-08, one day before the window; it is carried because
  issue #03 was compiled on 8 September before it appeared, because OpenAI amended it on
  10 September, and because the Clay statement of 11 September responds to it. The NVIDIA
  acquisition of Hugging Face (2026-09-03) was missed by issues #02 and #03 and is
  recorded in one flagged bullet. SWE-Bench Pro Verified was submitted 2026-09-08 and
  surfaced on 10 September; the report gives both dates.
- **Verification:** every figure, identifier and date in the report was read from the
  linked source on 2026-09-15. All four arXiv identifiers were copied from abstract pages
  that were fetched. Both proof PDFs were downloaded and their page counts taken from the
  files, not from press descriptions. Every openai.com page was read through
  `scripts/fetch_openai.py`; the direct fetch failed once with 403 and the archive
  fallback returned 429, and a retry succeeded — budget for retries.
- **Self-reported versus independent:** the DeepSeek benchmark rows, the OpenAI voice
  benchmark rows and the Nemotron IMO score are vendor or author self-reports and are
  labelled as such in the table's "Who ran it" column. The only independent number is the
  Artificial Analysis index (S9), compared with the previous Flash on the same index
  version (S10) rather than against the older "50" figure Artificial Analysis published for
  V4 Flash 0731 under an earlier index version.
- **The Navier–Stokes section quotes each party's own document** (OpenAI page and PDF,
  Buckmaster's statement and Euler paper, the CMI statement) and takes no position on
  priority. Secondary reporting was read for leads but nothing in the section rests on it.
- **Left out for lack of verification:** Fugu Ultra v2 pricing and context; the Bridson
  "absolutely rigorous" quote; every in-window regulatory lead; the Gulf laptop and
  G42 capital-raising leads.
- **Known gaps:** `fetch_openai.py --since` stamped every slug 2026-09-15 (site-wide
  re-render), so the in-window OpenAI pages were found by search and opened individually.
  `openai.com/news/` itself returned 403 with a 429 archive fallback. The `sakana.ai`
  blog index is reachable but the Fugu page carries no full benchmark table. Searches
  found no in-window model from Google, Anthropic, Meta, Mistral, xAI or Microsoft; the
  report does not claim there was none, only that none was found.
