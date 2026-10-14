# Ethics — PROCESSING4

**Project:** PROCESSING4  
**Category:** ARTIST_TOOLS  
**Upstream:** https://github.com/processing/processing4  
**Pinned commit:** `be0ee8266e07857f65937ec0a033707b9f6a286b`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f5b4a5cf8d3df25c0215138160189761366aaa2a26cfcd84191924e4775f02d0`  
**Date:** October 2026

## Position

PROCESSING4 is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
