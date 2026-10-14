# Educators — PROCESSING4

**Project:** PROCESSING4  
**Category:** ARTIST_TOOLS  
**Upstream:** https://github.com/processing/processing4  
**Pinned commit:** `be0ee8266e07857f65937ec0a033707b9f6a286b`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f5b4a5cf8d3df25c0215138160189761366aaa2a26cfcd84191924e4775f02d0`  
**Date:** October 2026

## Teaching with PROCESSING4

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `f5b4a5cf8d3df25c0215138160189761366aaa2a26cfcd84191924e4775f02d0` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
