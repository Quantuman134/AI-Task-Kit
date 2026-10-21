---
name: recent-cv-cg-paper-scout
description: Search and rank recent research papers in world models, generative models, and VLMs within computer vision or computer graphics. Prioritize technically important and actively discussed work, and distinguish true methodological contributions from papers that merely use these models.
---

# Recent CV/CG Paper Scout

## Goal

Find a small, high-quality set of recent papers that are genuinely worth reading.

## Requirements

1. By default, only consider work posted or published within the **last 3 months** from the current date.
2. Return **15–20 papers** by default.
3. Rank papers by **reading priority**, not simply by publication date.

## Primary Scope

A paper must primarily belong to at least one of these areas:

1. **Generative Models**
   - diffusion models
   - flow matching / rectified flow
   - DiT or related generative architectures
   - image, video, 3D, or 4D generation
   - generative-model training objectives
   - sampling / inference / distillation
   - representation or latent-space design
   - scaling, efficiency, controllability, or reasoning mechanisms inside generative models
   - and any possible new or interesting or impactful topic in this scope

2. **Vision-Language Models (VLMs)**
   - visual understanding and reasoning
   - multimodal representation learning
   - VLM agents
   - vision-language grounding
   - spatial / 3D / video reasoning
   - multimodal generation only when the VLM component is technically central
   - and any possible new or interesting or impactful topic in this scope

3. **World Models**
   - learned environment dynamics
   - action-conditioned prediction
   - interactive or embodied world simulation
   - long-horizon video/world prediction
   - 3D/4D world representations
   - world models for robotics, agents, games, or simulation
   - and any possible new or interesting or impactful topic in this scopen


The broader research area must be primarily **Computer Vision (CV)** or **Computer Graphics (CG)**.

## Search Procedure

1. Search recent papers from sources such as:
   - arXiv
   - Hugging Face Papers
   - conference / project pages
   - research-lab pages
   - GitHub repositories
   - other credible research sources

2. Verify the **actual posting/publication date**. Do not rely only on search-result timestamps.

3. Read enough of the abstract, introduction, and method description to determine the paper's **primary technical contribution**.

4. Reject papers that are only loosely connected to the requested scopes.

5. Check whether the paper is receiving unusual attention. Useful signals include:
   - Hugging Face Paper-of-the-Day ranking or upvotes
   - GitHub stars / forks / rapid repository activity
   - broad discussion in the research community
   - follow-up implementations or reproductions
   - strong attention from multiple independent sources

6. Treat attention signals as evidence of interest, **not proof of scientific quality**.

7. If prior recommendations are available in the current chat or memory, avoid repeating them unless:
   - there is a major new version,
   - an important new result appeared, or
   - the user explicitly asks for them again.

## Ranking Criteria

Rank papers mainly by:

1. **Relevance to the requested scope**
2. **Technical novelty / conceptual importance**
3. **Potential research impact**
4. **Current community attention**
5. **Recency**

Do not rank a paper highly only because it comes from a famous lab or has many social-media mentions.

## Output Format

Start with a concise sentence describing the strongest trend you found.

Then provide a ranked table with:

| Rank | Paper | Date | Category | Main contribution | Why read it | Attention signal |
|---|---|---|---|---|---|---|

For every paper:

- attach the **paper link directly to the title**
- give the exact posting/publication date when possible
- assign one or more categories:
  - World Model
  - Generative Model
  - VLM
- summarize the main technical contribution in **1–2 concise sentences**
- explain why it is worth reading
- give concrete evidence when calling it important or “hot”

After the table, add:

### My top 3

Choose the three papers that are most worth reading and briefly explain why.

### Methodological classification

When useful, explicitly distinguish:

- **New generative-model methodology**
- **World-model methodology**
- **VLM methodology**
- **Uses generative models but does not advance generative modeling**

This distinction is important and should not be blurred.

## Quality Checks

Before finalizing, verify:

- Every paper is within the requested time window, unless clearly marked as an intentional exception.
- Every paper is primarily relevant to CV/CG.
- Every paper fits at least one requested scope.
- “Generative Model” labels refer to actual generative-model contributions, not incidental model usage.
- Claims about popularity or importance have concrete supporting evidence.
- Links point to the actual paper/project/repository.
- Do not use citation count as the main importance signal for papers only a few weeks or months old.
- Prefer 5 strong papers over 10 weak or borderline papers.

## User Overrides

If the user specifies a different:
- time window,
- number of papers,
- subfield,
- venue,
- output format,
- or ranking preference,

follow the user's request instead of the defaults above.
