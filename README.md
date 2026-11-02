# Retrieved training documents for OLMo-2-1124-13B-Instruct answers

Infini-gram traces of answer spans against `v4_olmo-mix-1124_llama` (the OLMo 2 stage-1
pretraining corpus), gzip-compressed to stay under GitHub's 100 MB file limit.

| File | Answers | Uncompressed | SHA-256 (uncompressed) |
|---|---|---|---|
| `retrieved_docs/span_sources_all.clean.json.gz` | 460 | 202 MB | `d33e073b71657a8027d10a73e9e64aee24ca78c726dc331f106dd2c6948964cc` |
| `retrieved_docs/span_sources_tracing.clean.json.gz` | 800 | 381 MB | `013b9f2535184cf467171f0e11d488673153022481e2ec3189da7757808b347a` |

Each file is `{"metadata": {...}, "results": [...]}`. `doc_text` is the Infini-gram window
(up to 4,000 characters around the matched span), not the full source document.

Decompress: `gunzip -k retrieved_docs/*.json.gz`
