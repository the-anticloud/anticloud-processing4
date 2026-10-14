# Technical Architecture — PROCESSING4

**Upstream:** [https://github.com/processing/processing4](https://github.com/processing/processing4)
**License:** GPL/LGPL
**Category:** ARTIST_TOOLS
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Creative coding platform for visual artists

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local creative assistant for style transfer and composition
2. Single-binary offline creative suite — no subscription, no cloud required
3. AIOSS provenance chain for original artwork (NFT-ready integrity proof)
4. AES-256 encryption for unreleased work and client projects
5. GPU/CPU equalizer: AI generation scales from laptop CPU to RTX GPU
6. Zero-cloud: all models and assets run locally
7. Zero-telemetry: removes all tracking
8. Open format: exports to standard formats without vendor lock-in

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_processing4.spec` or `go build -o processing4`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |