# Small-Rule Guardrails for Retrieval-Augmented Generation

Public artifact bundle for the preprint:

> **Small-Rule Guardrails for Retrieval-Augmented Generation: Prompt Injection and Vector Poisoning Checks**
> Mukunda Rao Katta. ORCID: [0009-0007-6071-3896](https://orcid.org/0009-0007-6071-3896). License: CC BY 4.0.

[![DOI Zenodo](https://zenodo.org/badge/DOI/10.5281/zenodo.20057632.svg)](https://doi.org/10.5281/zenodo.20057632) [![DOI Figshare](https://img.shields.io/badge/DOI-10.6084%2Fm9.figshare.32193543-blue)](https://doi.org/10.6084/m9.figshare.32193543)

A compact engineering note on small-rule guardrails sitting between retrieval and prompt construction in RAG pipelines, implemented as two zero-dependency npm packages.

## Reference implementations

- [`@mukundakatta/prompt-injection-shield`](https://www.npmjs.com/package/@mukundakatta/prompt-injection-shield) — string-pattern checks for adversarial instructions in retrieved text
- [`@mukundakatta/vector-poison-score`](https://www.npmjs.com/package/@mukundakatta/vector-poison-score) — heuristic risk score for retrieved chunks (oversize, secret-exfil patterns, suspicious links)

## Files in this repo

| File | Purpose |
|---|---|
| `rag-guardrails-small-rule-preprint.pdf` | Submission-ready manuscript |
| `paper.md` | Source draft |
| `paper.bib` | Bibliography |
| `abstract.txt` | Upload-ready abstract |
| `keywords.txt` | Suggested keywords |
| `assets/workflow-figure.svg` | Workflow figure |
| `submission-metadata.json` | Structured submission metadata |
| `render_preprint_pdf.py` | Reproduces the PDF locally |
| `rag-guardrails-figshare-package.zip` | Bundle for Figshare/Zenodo deposit |

## Abstract

Retrieval-augmented generation systems often treat retrieved text as helpful evidence, but retrieved text can also contain adversarial instructions, suspicious link patterns, oversized chunks, or secret-exfiltration requests. This paper presents a small-rule guardrail approach implemented through two zero-dependency JavaScript packages: prompt-injection-shield and vector-poison-score. The method is deliberately lightweight. It scans retrieved documents and tool outputs before they are inserted into model context, reports explicit risk reasons, and supports filtering or line stripping as a simple containment step. The contribution is not a replacement for full security review or large-scale benchmark evaluation. Instead, it offers an inspectable baseline that developers can place between retrieval and prompt construction while building, testing, and auditing agentic RAG workflows.

## Citation

Cite via the Zenodo or Figshare DOI:

```
Katta, M. R. (2026). Small-Rule Guardrails for Retrieval-Augmented Generation: Prompt Injection and Vector Poisoning Checks (Version v1). Zenodo. https://doi.org/10.5281/zenodo.20057632

Figshare mirror: https://doi.org/10.6084/m9.figshare.32193543
```

## License

CC BY 4.0 for the manuscript and figures. MIT for the reference packages.
