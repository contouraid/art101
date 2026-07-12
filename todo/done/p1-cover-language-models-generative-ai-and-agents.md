# DONE: Cover Language Models, Generative AI, and Agents

**Section:** `fundamentalAI/`
**Priority:** High
**Owner:** Codex
**Opened:** 2026-07-11
**Completed:** 2026-07-12

## Gap

The VLM page explains image-language systems, but the book lacks a foundation for text-only large language models, clinical NLP, retrieval-augmented generation, tool use, and agentic workflows. These systems are increasingly discussed for documentation, information retrieval, guideline navigation, coding, plan/chart checking, patient communication, and workflow orchestration. Readers need terminology and evidence standards that distinguish a language model, chatbot, search system, tool-using agent, and clinically integrated product.

Without this material, the book's terminology is incomplete and readers may overinterpret fluent output, benchmark scores, or demonstrations as reliable clinical reasoning.

## What Is Needed

1. Add novice-level explanations of tokenization, embeddings, pretraining, instruction tuning, context windows, prompting, inference, and the difference between discriminative NLP and generative language models.
2. Explain retrieval-augmented generation, citations and provenance, structured outputs, function/tool calling, memory, workflow agents, and deterministic guardrails.
3. Map radiotherapy use cases across documentation, information extraction, cohort discovery, guideline retrieval, plan/chart QA, patient-facing communication, and research workflows.
4. Cover hallucination, omission, prompt injection, data exfiltration, unreliable citations, knowledge cutoffs, model/version drift, overreliance, and the limits of verbalized confidence.
5. Teach task-appropriate evaluation: factuality, evidence attribution, extraction accuracy, calibration/abstention, clinical error severity, human editing burden, subgroup performance, and prospective human-AI outcomes.
6. Distinguish peer-reviewed clinical evidence from general-medical benchmarks, vendor claims, and radiation-oncology preprints; cross-link rather than duplicate VLM safety and evaluation content.

## Acceptance Criteria

- [x] Readers can distinguish NLP, an LLM, a chatbot, RAG, tool use, an agent, and a VLM
- [x] The generation and retrieval pipeline is illustrated from source document to reviewed clinical output
- [x] At least four radiotherapy use cases are evaluated in terms of evidence maturity, failure modes, and required oversight
- [x] Prompt injection, privacy leakage, fabricated attribution, version drift, and automation bias are addressed
- [x] Evaluation includes source-grounded factuality and clinically weighted human-AI assessment, not only lexical similarity or preference
- [x] Claims about clinical capability rely on verified evidence and preprints are clearly labeled
- [x] Generic multimodal material is linked to `fundamentalAI/vlm.md` rather than duplicated

## What Was Done

1. Added `docs/fundamentalAI/llm.md` as the canonical text-only language-model and agent companion to Chapter 2.
2. Defined NLP, discriminative models, LLMs, generative AI, chatbots, RAG, tool use, agents, and VLMs, then explained tokenization, embeddings, pretraining, instruction tuning, context windows, prompting, decoding, and inference.
3. Added a source-to-reviewed-output pipeline showing corpus governance, retrieval, trust boundaries, constrained generation, claim/citation validation, clinician review, and audit logging.
4. Covered RAG, citations and provenance, structured outputs, tool contracts, state and memory, multi-step agents, and deterministic guardrails including least privilege and confirmation before writes.
5. Added an evidence-maturity table for documentation, extraction and cohort discovery, guideline retrieval, plan/chart checking, patient communication, research workflows, and workflow agents, with failure modes and minimum oversight for each.
6. Covered hallucination, omission, fabricated references, prompt injection, data exfiltration, privacy, knowledge cutoffs, configuration drift, unreliable verbal confidence, automation bias, and overreliance.
7. Added task-specific evaluation for extraction, retrieval, generation, attribution, abstention, clinical severity, editing burden, subgroup performance, and prospective human-AI outcomes.
8. Used peer-reviewed foundational, security, medical-evaluation, and radiation-oncology evidence; treated vendor demonstrations and unpublished RT preprints as hypotheses rather than clinical evidence.
9. Cross-linked the page from Chapter 2, VLM, QA, and workflow content while leaving multimodal architecture and image-specific evaluation in `vlm.md`.

## Verification

- Verified all 11 references against DOI, ACL, NeurIPS, ACM, Nature, or JAMA publication pages.
- Confirmed all seven acceptance criteria in the rendered source and verified the text/VLM canonical boundary.
- Ran `git diff --check`, a citation/reference consistency check, and a clean strict Sphinx build with warnings treated as errors.
