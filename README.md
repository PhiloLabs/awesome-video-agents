# Awesome Video Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI agents and agentic frameworks for video editing, video production, and video understanding-for-production.

Video creation is rapidly shifting from single-shot model inference toward **agentic systems** that plan, decompose tasks, use tools, orchestrate specialized roles (director, screenwriter, editor, cinematographer), and self-correct. This list tracks the projects driving that shift.

## Scope & Inclusion Criteria

A project qualifies if it is an **agent or agentic framework** whose primary purpose is video editing, video production, or video understanding-in-service-of-production. It must satisfy at least one of:

- Multi-step planning / tool-use for video tasks (storyboarding, shot selection, editing decisions, post-production)
- Multi-agent orchestration for video pipelines (director / writer / editor / producer roles)
- Agents that interact with video editing software, video APIs, or composition primitives
- LLM/VLM-driven controllers wrapping video generation, editing, or understanding models

Out of scope (and curated elsewhere):

- Pure video-generation foundation models with no agent layer (Sora, Veo, Kling, Runway core models) — see [awesome-any2any-models](https://github.com/PhiloLabs/awesome-any2any-models) for unified multimodal models
- Benchmarks and evaluation suites for multimodal agents — see [awesome-multimodal-agent-benchmarks](https://github.com/PhiloLabs/awesome-multimodal-agent-benchmarks)
- Generic NLE software, video diffusion architectures, or tracking/segmentation libraries

## Contents

- [All-in-One Agentic Frameworks](#all-in-one-agentic-frameworks)
- [Multi-Agent Pipelines (Director / Writer / Editor)](#multi-agent-pipelines-director--writer--editor)
- [Video Editing Agents](#video-editing-agents)
- [Video Generation / Production Agents](#video-generation--production-agents)
- [Video Understanding Agents (for Production)](#video-understanding-agents-for-production)
- [NLE & Software-Control Integrations (MCP & Tools)](#nle--software-control-integrations-mcp--tools)
- [Related Surveys & Papers](#related-surveys--papers)
- [Contributing](#contributing)
- [License](#license)

---

## All-in-One Agentic Frameworks

End-to-end systems that span understanding, editing, and generation under a single agentic controller.

- [HKUDS/VideoAgent](https://github.com/HKUDS/VideoAgent) — All-in-one agentic framework for video understanding, editing, and remaking with intent-to-agent workflow routing. `code`
- [video-db/Director](https://github.com/video-db/Director) — Open-source framework for building video agents that reason across search, edit, compile, and generate over a VideoDB backend. `code`
- [HKUDS/ViMax](https://github.com/HKUDS/ViMax) — 12 specialized agents (director, screenwriter, producer, etc.) for end-to-end multi-shot video generation with RAG long-script design. `code`
- [diffusionstudio/agent](https://github.com/diffusionstudio/agent) — Agentic video editing framework built on a browser-based WebCodecs compositing engine. `code`

## Multi-Agent Pipelines (Director / Writer / Editor)

Systems that explicitly simulate film-crew roles via multi-agent collaboration.

- [showlab/MovieAgent](https://github.com/showlab/MovieAgent) — Automated movie generation via multi-agent CoT planning across director, screenwriter, storyboard, and location agents. [`paper`](https://arxiv.org/abs/2503.07314) `code`
- [HITsz-TMG/FilmAgent](https://github.com/HITsz-TMG/FilmAgent) — LLM multi-agent collaboration for end-to-end film automation in virtual 3D spaces (SIGGRAPH Asia 2024). [`paper`](https://arxiv.org/abs/2501.12909) `code`
- [HITsz-TMG/Anim-Director](https://github.com/HITsz-TMG/Anim-Director) — Large multimodal model agent that autonomously directs controllable animation video generation (SIGGRAPH Asia 2024). [`paper`](https://arxiv.org/abs/2408.09787) `code`
- [Anim-Director/AniMaker](https://github.com/HITsz-TMG/Anim-Director/tree/main/AniMaker) — Multi-agent animated storytelling with MCTS-driven candidate clip generation (SIGGRAPH Asia 2025). [`paper`](https://arxiv.org/abs/2506.10540) `code`
- [Vchitect/Vlogger](https://github.com/Vchitect/Vlogger) — LLM-as-director decomposes vlog generation into Script, Actor, ShowMaker, and Voicer roles (CVPR 2024). [`paper`](https://arxiv.org/abs/2401.09414) `code`
- [HL-hanlin/VideoDirectorGPT](https://github.com/HL-hanlin/VideoDirectorGPT) — LLM-guided planning for consistent multi-scene video generation with a layout-grounded video module (COLM 2024). [`paper`](https://arxiv.org/abs/2309.15091) `code`
- [X-PLUG/MM_StoryAgent](https://github.com/X-PLUG/MM_StoryAgent) — Open-source multi-agent paradigm for immersive narrated storybook video across text, image, and audio. [`paper`](https://arxiv.org/abs/2503.05242) `code`
- [DreamFactory](https://arxiv.org/abs/2408.11788) — Multi-agent framework with director / art-director / screenwriter / artist roles for multi-scene long video generation. `paper`
- [AesopAgent](https://aesopai.github.io/) — Agent-driven evolutionary RAG system from DAMO that turns story proposals into scripted, scored, voiced videos. [`paper`](https://arxiv.org/abs/2403.07952)
- [multimodal-art-projection/AutoMV](https://github.com/multimodal-art-projection/AutoMV) — Multi-agent music video generation from raw audio plus lyrics with screenwriter, director, and verifier agents. [`paper`](https://arxiv.org/abs/2512.12196) `code`
- [Co-Director](https://co-director-agent.github.io/) — Hierarchical multi-agent framework for generative video storytelling along creative-strategy / narrative-mode / aesthetic axes. [`paper`](https://arxiv.org/abs/2604.24842)

## Video Editing Agents

Agents focused on editing existing footage — cut planning, trimming, montage, color, captions.

- [browser-use/video-use](https://github.com/browser-use/video-use) — Edit videos with Claude Code: word-boundary cuts, color grading, subtitles, self-evaluating output. Designed as a Claude Code skill. `code`
- [GVCLab/CutClaw](https://github.com/GVCLab/CutClaw) — Autonomous multi-agent framework for hours-long montage editing with music synchronization (Playwriter / Editor / Reviewer agents). [`paper`](https://arxiv.org/abs/2603.29664) `code`
- [EditDuet](https://arxiv.org/abs/2509.10761) — Editor + Critic multi-agent system for non-linear video editing from natural language (SIGGRAPH 2025, Adobe Research). `paper`
- [LAVE](https://www.dgp.toronto.edu/~bryanw/lave/) — LLM-powered plan-and-execute agent for video editing with language-augmented UI (IUI 2024). [`paper`](https://arxiv.org/abs/2402.10294)
- [GLANCE](https://arxiv.org/abs/2604.05076) — Global-local coordination multi-agent framework for music-grounded non-linear mashup editing. `paper`
- [Prompt-Driven Agentic Video Editing](https://memories.ai/research/Agentic-Video-Editing) — Modular pipeline using hierarchical semantic indexing for long-form, story-driven editing. [`paper`](https://arxiv.org/abs/2509.16811)

## Video Generation / Production Agents

Agents that wrap or compose generative video models for controllable, multi-shot, or long-form output.

- [lichao-sun/Mora](https://github.com/lichao-sun/Mora) — Generalist video generation via a multi-agent framework that composes specialized visual agents to cover T2V / I2V / editing tasks. [`paper`](https://arxiv.org/abs/2403.13248) `code`
- [DuNGEOnmassster/VideoGen-of-Thought](https://github.com/DuNGEOnmassster/VideoGen-of-Thought) — Step-by-step multi-shot video synthesis from one sentence via dynamic storyline modeling (NeurIPS 2025 Workshop). [`paper`](https://arxiv.org/abs/2503.15138) `code`
- [GenMAC](https://karine-h.github.io/GenMAC/) — Iterative DESIGN / GENERATION / REDESIGN multi-agent loop for compositional text-to-video (AAAI 2025). [`paper`](https://arxiv.org/abs/2412.04440)
- [Video-as-Agent/VideoAgent](https://github.com/Video-as-Agent/VideoAgent) — Self-improving video generation that refines plans with VLM and execution feedback (for embodied planning). [`paper`](https://arxiv.org/abs/2410.10076) `code`
- [Vibe AIGC](https://arxiv.org/abs/2602.04575) — Paradigm paper on agentic orchestration as a bridge between high-level creator intent and stochastic generative models. `paper`

## Video Understanding Agents (for Production)

Understanding agents whose outputs feed editing, search, indexing, or selection — included when used agentically (planning, tool-use, memory), not as static VLM inference.

- [wxh1996/VideoAgent](https://github.com/wxh1996/VideoAgent) — LLM as central agent that iteratively calls VLM tools to answer queries about long-form video (ECCV 2024, Stanford). [`paper`](https://arxiv.org/abs/2403.10517) `code`
- [YueFan1014/VideoAgent](https://github.com/YueFan1014/VideoAgent) — Memory-augmented multimodal agent with structured temporal + object memory for video understanding (ECCV 2024). [`paper`](https://arxiv.org/abs/2403.11481) `code`
- [z-x-yang/DoraemonGPT](https://github.com/z-x-yang/DoraemonGPT) — Dynamic-scene understanding agent with symbolic task memory, sub-task tools, and MCTS planning (ICML 2024). [`paper`](https://arxiv.org/abs/2401.08392) `code`
- [Ziyang412/VideoTree](https://github.com/Ziyang412/VideoTree) — Query-adaptive hierarchical tree representation for long-video LLM reasoning (CVPR 2025). [`paper`](https://arxiv.org/abs/2405.19209) `code`
- [HKUDS/VideoRAG](https://github.com/HKUDS/VideoRAG) — Retrieval-augmented generation over extreme long-context video corpora; powers the Vimo desktop chat-with-video app (KDD 2026). `code`
- [yiwengxie/Chat-Video](https://github.com/yiwengxie/Chat-Video) — Tracklet-centric versatile video understanding system enabling instance-level chat with videos. [`paper`](https://arxiv.org/abs/2304.14407) `code`
- [VCA: Video Curious Agent](https://arxiv.org/abs/2412.10471) — Curiosity-driven self-exploration agent with tree-search over video segments for efficient long-video QA. `paper`

## NLE & Software-Control Integrations (MCP & Tools)

Agents and MCP servers that let LLMs drive professional editors (Premiere, DaVinci) or compose FFmpeg pipelines.

- [mikechambers/adb-mcp](https://github.com/mikechambers/adb-mcp) — Reference MCP interface that exposes Adobe Photoshop and Premiere to LLM clients. `code`
- [ayushozha/AdobePremiereProMCP](https://github.com/ayushozha/AdobePremiereProMCP) — Premiere Pro MCP server with 1,000+ tools across timeline, color, audio, effects, and export. `code`
- [hetpatel-11/Adobe_Premiere_Pro_MCP](https://github.com/hetpatel-11/Adobe_Premiere_Pro_MCP) — Premiere Pro MCP covering project ops, ingest, sequence creation, transitions, effects, exports. `code`
- [leancoderkavy/premiere-pro-mcp](https://github.com/leancoderkavy/premiere-pro-mcp) — MCP server for Adobe Premiere Pro via CEP/ExtendScript with 269 tools across 28 modules. `code`
- [samuelgursky/davinci-resolve-mcp](https://github.com/samuelgursky/davinci-resolve-mcp) — MCP server integration for DaVinci Resolve Studio scripting API. `code`
- [lordhoell/davinci-resolve-mcp](https://github.com/lordhoell/davinci-resolve-mcp) — Claude Code skill + MCP exposing 440+ DaVinci Resolve tools for AI-assisted editing, color, and rendering. `code`
- [wizenheimer/vibestudio](https://github.com/wizenheimer/vibestudio) — Headless zero-runtime FFmpeg MCP server in pure Bash for agent-driven editing pipelines. `code`
- [burningion/video-editing-mcp](https://github.com/burningion/video-editing-mcp) — MCP interface for Video Jungle that produces OpenTimelineIO projects for DaVinci Resolve. `code`
- [blitzreels/agent-skills](https://github.com/blitzreels/agent-skills) — Skills for agents to inspect, edit, validate, and export video through BlitzReels MCP and CLI. `code`
- [remyxai/FFMPerative](https://github.com/remyxai/FFMPerative) — LLM-powered chat copilot that composes FFmpeg edits from natural language. `code`
- [BAAI-Agents/Cradle](https://github.com/BAAI-Agents/Cradle) — Generalist computer-control agent (screen-in, keyboard/mouse-out) that can drive CapCut, Meitu, and other editors. [`paper`](https://arxiv.org/abs/2403.03186) `code`
- [showlab/Kiwi-Edit](https://github.com/showlab/Kiwi-Edit) — Unified open-source framework for instruction-guided and reference-guided video editing in natural language. [`paper`](https://arxiv.org/abs/2603.02175) `code`

## Related Surveys & Papers

- [VideoGen-Eval](https://github.com/AILab-CVC/VideoGen-Eval) — Agent-based system for video generation evaluation; useful prior art for agent-as-judge in production pipelines. [`paper`](https://arxiv.org/abs/2503.23452) `code`
- [yunlong10/Awesome-LLMs-for-Video-Understanding](https://github.com/yunlong10/Awesome-LLMs-for-Video-Understanding) — Companion survey of video-LMM literature (IEEE TCSVT).
- [yunlong10/Awesome-Video-LMM-Post-Training](https://github.com/yunlong10/Awesome-Video-LMM-Post-Training) — Tracks reasoning-oriented post-training of video LMMs (relevant when fine-tuning agent backbones).
- [wentianli/awesome-video-editing](https://github.com/wentianli/awesome-video-editing) — Paper list on cinematographic video editing and related CV tasks; broader than the agentic slice tracked here.

---

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for inclusion criteria and entry format. The bar is: agentic (planning / tool-use / multi-role / controller), video-focused, and substantive (paper, working code, or production system).

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, contributors have waived all copyright and related rights to this work.
