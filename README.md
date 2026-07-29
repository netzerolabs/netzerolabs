<div align="center">

# NetZero Labs

### Open climate intelligence, built in public.

**AI mở cho khí hậu, môi trường và phát triển bền vững.**

[![Focus: Climate AI](https://img.shields.io/badge/focus-climate%20AI-176B4D)](#curated-projects)
[![Open Models](https://img.shields.io/badge/open-models-246BCE)](#what-open-means-here)
[![Reproducible RAG](https://img.shields.io/badge/RAG-reproducible-6F42C1)](#reference-stack)
[![Contributions welcome](https://img.shields.io/badge/contributions-welcome-EA7C24)](CONTRIBUTING.md)

</div>

NetZero Labs is a curated home for transparent, reproducible AI built for climate science, environmental analysis, energy transition, sustainability, and climate policy.

We track domain language models, retrieval-augmented generation systems, datasets, evaluation tools, and practical building blocks that researchers and developers can inspect, adapt, and—where licensing permits—self-host.

## Why this exists

“Climate AI” should mean more than a demo. A useful public-interest project should make its technical choices, sources, limitations, and reuse terms visible.

NetZero Labs prioritizes projects with:

- public source code or a reproducible implementation;
- downloadable model weights when a model is released;
- an explicit license for each important artifact;
- traceable climate or environmental data sources;
- documentation sufficient to reproduce meaningful results;
- model cards, evaluation results, citations, and known limitations.

## What “open” means here

| Status | Meaning |
|---|---|
| **Open** | Core code and relevant artifacts have clear licenses that permit reuse and modification. |
| **Open pipeline** | The data/retrieval pipeline is public, but generation may depend on a hosted or proprietary model. |
| **Source-available** | Code or weights are public, but a custom, non-commercial, or otherwise restrictive license applies. |
| **Mixed** | Different artifacts have different terms, or an important repository does not declare a license. |

Publicly downloadable does not automatically mean open source. Always review the upstream license before production or commercial use.

## Curated projects

| Project | What it provides | Public artifacts | Status |
|---|---|---|---|
| **ClimateGPT — ECI** | A family of climate-specialized generative models, including 7B, 13B, and 70B variants designed for climate QA and retrieval augmentation. | [Models](https://huggingface.co/eci-io) · [Paper](https://arxiv.org/abs/2401.09646) · [Evaluation](https://github.com/eci-io/climategpt-evaluation) | **Source-available** — public weights under the ClimateGPT Community License; evaluation repository does not declare a license. |
| **ClimateGPT — MBZUAI Oryx** | A Vicuna-based climate and sustainability conversational model, with training code, weights, and the Clima500 dataset. | [Code](https://github.com/mbzuai-oryx/ClimateGPT) · [Model](https://huggingface.co/mbzuai-oryx/ClimateGPT) · [Dataset](https://huggingface.co/datasets/mbzuai-oryx/Clima500) · [Paper](https://aclanthology.org/2023.findings-emnlp.941/) | **Source-available** — CC BY-NC-SA 4.0; non-commercial restriction. |
| **ClimateBERT** | Domain-adapted DistilRoBERTa models for climate text, including detection, sentiment, specificity, commitments, and disclosure classification. | [Models](https://huggingface.co/climatebert) · [Training code](https://github.com/ClimateBert/language-model) · [Paper](https://arxiv.org/abs/2110.12010) | **Open** — Apache 2.0 code and primary model; check each downstream model card separately. |
| **Environmental Claims** | A ClimateBERT classifier, dataset, and inference code for detecting real-world environmental claims. | [Code & data](https://github.com/dominiksinsaarland/environmental_claims) · [Model](https://huggingface.co/climatebert/environmental-claims) · [Dataset](https://huggingface.co/datasets/climatebert/environmental_claims) · [Paper](https://arxiv.org/abs/2209.00507) | **Mixed** — model is Apache 2.0; the code repository does not declare a license. |
| **ChatClimate / ChatIPCC** | An IPCC AR6-grounded RAG research prototype and reproducible notebook for climate question answering. | [Demo](https://www.chatclimate.ai/) · [Notebook](https://github.com/saeedashraf/chatipcc) · [Paper](https://www.nature.com/articles/s43247-023-01084-x) | **Open pipeline** — notebook is public, but it requires an OpenAI API key and the repository does not declare a license. |
| **semantic_RAG** | A production-oriented Climate Academy RAG backend with semantic chunking, ChromaDB, local embeddings, and inline citations. | [Code](https://github.com/semanticClimate/semantic_RAG) | **Open code** — Apache 2.0; default generation runs Llama 3.1 through AWS Bedrock. |
| **KISSKI RAG for IPCC** | A climate-literature RAG notebook using Llama 3, FAISS, and semantic HTML chunking, with an option to replace the hosted endpoint with a local model. | [Code](https://github.com/semanticClimate/KISSKI-RAG-4-IPCC) | **Source-available** — non-commercial license. |

For a broader research-oriented inventory, see [Language Models for Climate Change Texts](https://github.com/volkanovska/Language-models-for-climate-change-texts).

## Reference stack

A fully controllable climate RAG system can be assembled from replaceable open components:

| Layer | Recommended capability |
|---|---|
| **Sources** | Versioned IPCC reports, COP decisions, peer-reviewed literature, policy documents, and observational datasets |
| **Ingestion** | Structure-aware parsing, metadata retention, deduplication, and source-level provenance |
| **Retrieval** | Open embeddings plus Chroma, Qdrant, FAISS, or another self-hosted vector store |
| **Generation** | A locally deployable LLM such as Llama, Mistral, or Gemma, subject to its own license |
| **Grounding** | Passage-level citations, abstention when evidence is weak, and visible source excerpts |
| **Evaluation** | Retrieval recall, citation correctness, groundedness, climate-domain accuracy, latency, and energy use |

## What we plan to build

- **Climate model index** — machine-readable metadata for models, datasets, code, licenses, tasks, and deployment requirements.
- **IPCC RAG starter** — a fully local reference implementation with citations and replaceable components.
- **Climate evaluations** — reproducible tests for retrieval, factual grounding, and domain-specific QA.
- **Data pipelines** — documented ingestion workflows for authoritative climate and environmental sources.

These are roadmap items, not claims of completed releases.

## Contribute a project

Know a project that belongs here? [Open a project submission](https://github.com/netzerolabs/netzerolabs/issues/new?template=project-submission.yml).

A submission should include links to code, weights or datasets, licenses, documentation, and evidence of climate/environment relevance. See [CONTRIBUTING.md](CONTRIBUTING.md) for the review criteria.

## Tiếng Việt

NetZero Labs tuyển chọn, đánh giá và xây dựng các dự án AI phục vụ khí hậu và môi trường theo hướng minh bạch, có thể kiểm chứng và tái lập.

Danh mục ưu tiên dự án có mã nguồn công khai, trọng số hoặc dữ liệu có thể tải xuống, giấy phép rõ ràng, nguồn dữ liệu đáng tin cậy và tài liệu đủ để triển khai lại. Mỗi dự án được phân loại theo mức độ mở thực tế, không chỉ dựa trên cách dự án tự giới thiệu.

Bạn có thể đề xuất dự án mới bằng [mẫu issue này](https://github.com/netzerolabs/netzerolabs/issues/new?template=project-submission.yml).

---

**Independent community directory.** Inclusion does not imply endorsement or affiliation. Project names and trademarks belong to their respective owners. License notes are informational—verify the upstream terms for your use case.

_Last reviewed: 29 July 2026._
