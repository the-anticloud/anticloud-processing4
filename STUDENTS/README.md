# Students — PROCESSING4

**Project:** PROCESSING4  
**Category:** ARTIST_TOOLS  
**Upstream:** https://github.com/processing/processing4  
**Pinned commit:** `be0ee8266e07857f65937ec0a033707b9f6a286b`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f5b4a5cf8d3df25c0215138160189761366aaa2a26cfcd84191924e4775f02d0`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `be0ee8266e07857f65937ec0a033707b9f6a286b`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `f5b4a5cf8d3df25c0215138160189761366aaa2a26cfcd84191924e4775f02d0`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
