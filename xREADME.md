### Hasan Tatar

Full-stack engineer working in Python and TypeScript, with applied-AI work running in production on the Anthropic Claude API. Based in Istanbul — completing a B.Sc. in Computer Engineering (expected 2027).

Recent work: the orchestration layer of an AI customer-service pipeline handling live webhook traffic across four messaging channels, a bus-fleet operations platform on AWS AppSync, and a tool that fills real German regulatory PDF forms. First author on an IEEE SIU 2026 paper measuring how a vision-language-action model degrades on Turkish commands.

---

#### What I'm building

**[quantum](https://github.com/wazder/quantum)** — a Windows compatibility layer for macOS on Apple Silicon, in Rust

A translation stack written from scratch with no Wine, no MoltenVK, and no third-party crates in the dependency tree: a PE/COFF loader, an x86-64 instruction decoder, an AArch64 emitter validated against clang-assembled golden output, a register-pinned JIT lifter, and a DXBC shader parser emitting Metal Shading Language into a D3D11-to-Metal device layer. Four end-to-end tests hand-assemble real Win64 PE byte buffers and run them through the whole pipeline on real silicon — `ExitProcess`, `WriteFile` to stdout, backward branches, and PUSH/POP through a guest stack. This is a read-the-code project, and it is unfinished: the D3D11 path stops before it draws a pixel.

**[xtask — regulatory compliance for German PV installers](https://wazder.github.io/powerbird/)** — live demo

Fills the official 23-page VDE-AR-N 4105 grid-connection AcroForm — 557 fields across four forms — from project data, verified by automated field assertions, and exports XRechnung 3.0 UBL invoices with the § 12 UStG VAT split applied. Runs entirely client-side against a seeded dataset, so everything in the demo actually works. The hard part was not the domain logic: extracting a page subset drops the document-level AcroForm, so keeping sub-documents interactive meant rebuilding it through reference-based widget copying around a pdf-lib limitation. Repo private (client work).

**[cognitive-drone](https://github.com/wazder/cognitive-drone)** — vision-language model benchmark

Evaluated Qwen2.5-VL-3B/7B and LLaVA-1.5-7B on autonomous drone gate selection over the full 218-entry CognitiveDroneBench, ablating CLIP-B/32, CLIP-L/14, SigLIP, Sentence-BERT, and CLIP-free direct selection. Best configuration reached 94.5% against a 71.6% CLIP-only baseline reproduced in the same harness. Note the caveat recorded in the repo: the reproduction is text-grounded rather than image-grounded, which makes the setup easier than the original paper's.

**CamelLayer** — [camellayer.com](https://camellayer.com)

A Turkish-to-English prompt-compression engine for AI coding tools, iterated across 17 versions against measured tokenizer counts, with integration hooks for the Claude, Gemini, Codex, and Copilot CLIs. Closed source; the API is currently offline pending a rewrite.

---

#### Research

H. Tatar, U. Gökmen, I. Akkoyun, and S. Kahraman, "Performance Analysis of Vision-Language-Action Models: Evaluating Turkish Command Understanding in OpenVLA," in *Proc. 2026 34th Signal Processing and Communications Applications Conference (SIU)*, İstanbul, Türkiye, Jul. 2026. [doi:10.1109/SIU71813.2026.11636432](https://doi.org/10.1109/SIU71813.2026.11636432)

First and corresponding author. 300 OpenVLA-7B inferences over 50 matched Turkish/English command pairs: mean L2 action error 0.501, cosine similarity 0.372 (p < 0.001), command complexity uncorrelated with degradation, and 30.8% more tokens for Turkish after BPE segmentation.

---

#### Stack

Python · TypeScript · Rust · FastAPI · Next.js · React · PostgreSQL · SQLAlchemy · Anthropic Claude API · PyTorch · AWS CDK · Cloudflare Workers · Google Cloud · Docker

---

[wazder.com](https://wazder.com) · [linkedin.com/in/wazder](https://linkedin.com/in/wazder) · contact@wazder.com
