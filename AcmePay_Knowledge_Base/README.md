# AcmePay Synthetic Company Knowledge Base

This is a fictional, synthetic dataset created for learning Retrieval-Augmented Generation (RAG), multimodal RAG, retrieval evaluation, agentic RAG, and enterprise security patterns.

## Important
- AcmePay is fictional.
- All employee names, policies, financial figures, incidents, and project details are synthetic.
- The dataset is not legal, HR, financial, or operational advice.
- Do not use the example access-control matrix as a complete production authorization design.

## Contents
- `raw/hr/`: HR policies, handbook, FAQ and onboarding.
- `raw/engineering/`: architecture, API guide, runbooks, incident report, service catalog and schema notes.
- `raw/finance/`: synthetic XLSX and CSV financial data plus definitions.
- `raw/customer_support/`: troubleshooting, FAQs, refund policy and escalation matrix.
- `raw/meetings/`: meeting transcripts and project status.
- `raw/security/`: classification policy, access matrix and prompt-injection test cases.
- `raw/diagrams/`: PNG architecture diagrams.
- `processed/`: document manifest in JSON and CSV.
- `evaluation/`: questions, ground truth and a flat CSV evaluation dataset.

## Suggested learning path
1. Start with `.txt` and `.md` files only.
2. Add PDF and DOCX parsing.
3. Add XLSX and CSV structured data handling.
4. Add PNG image understanding / OCR / visual retrieval.
5. Build metadata-aware chunking and retrieval.
6. Add hybrid search and reranking.
7. Use the evaluation files to compare retrieval and answer quality.
8. Add access filtering before retrieval using the document metadata.
9. Add live data tools and agent workflows later.

## Data access note
The `access_level` and department metadata are teaching examples. Implement authorization in your application and test it independently; never trust a metadata label supplied by an end user.
