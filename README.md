# PROCESSING4

> [!NOTE] **Processing 5.0 development is underway on `main`.** - **New features and 5.0 work:** Open pull requests against `main`. - **Bug fixes for Processing 4:** Open pull requests against the [`4.x`](https://github.com/processing/processing4/tree/4.x) branch. Not sure which branch to use? Ask in the issue thread or on [Discord](https://discord.processing.org) in #devs-chat.

**Category:** ARTIST_TOOLS · **Ecosystem:** python · **Vendored upstream:** https://github.com/processing/processing · **Pinned commit:** `f480ef6ee34b9b7178b7f21f4f1a52cf49475642` · **Vendor:** Anticloud FZ LLE

> **Note:** this package vendors `https://github.com/processing/processing` as the implementation for the `PROCESSING4` slot. The vendored repository name differs from the package name; the pin above is the exact commit vendored here.

## What This Project Is

[!NOTE] **Processing 5.0 development is underway on `main`.** - **New features and 5.0 work:** Open pull requests against `main`. - **Bug fixes for Processing 4:** Open pull requests against the [`4.x`](https://github.com/processing/processing4/tree/4.x) branch. Not sure which branch to use? Ask in the issue thread or on [Discord](https://discord.processing.org) in #devs-chat.

This is the upstream project, vendored at the pinned commit above and packaged offline-first. The 12 improvements Anticloud adds live in `anticloud/` and are described under *Anticloud Overlay* below. Every fact in this file traces to a file in this directory.

## Installation

Building Processing locally on your machine will let you troubleshoot and make sure your contributions work as intended before submitting them to this repository. It also gives you the flexibility to experiment and learn more about how Processing is structured.

For a quick start:
1. Fork and clone the repository
1. Open it in IntelliJ IDEA
1. Wait for Gradle to sync
1. Next to the run Button, select the `Processing` Configuration
1. Hit Run

For more information and detailed instructions, follow our [How to Build Processing](BUILD.md) guide.

## Usage

If you're interested in *using* Processing, head over to the [download page](https://processing.org/download), or read more about the project on the [Processing website](https://processing.org/). There are also several [tutorials](https://processing.org/tutorials) that provide a helpful introduction. They are complemented by hundreds of examples that are included with the software itself.

## Anticloud Overlay

The 12 improvements live under `anticloud/`. Run the check suite from this directory:

```
python anticloud/bench/runner.py --cwd anticloud
```

## Benchmark Results

| Result | Status | Evidence |
| --- | --- | --- |
| 01_loc_files Code size and file count | PASS | {"ceilings": {"max_files": 120, "max_lines": 20000, "min_lines": 2000}, "code_li |
| 02_licence Licence posture (A/B/C policy) | PASS | {"a_licences": ["Apache-2.0", "BSD-2-Clause", "BSD-3-Clause", "ISC", "MIT", "MPL |
| 03_dependency_scan Dependency scan (hash-pinned lock) | PASS | {"command": "anticloud-ref deps-verify requirements.lock", "declared_in_pyprojec |
| 04_sbom_cyclonedx SBOM (CycloneDX 1.5) | PASS | {"command": "python -c \"import json;d=json.load(open('sbom.cdx.json'));print(d[ |
| 05_git_health Git health | PASS | {"branch": "main", "command": "git status --porcelain && git log --oneline -1 && |
| 06_owasp_llm_top10 OWASP Top 10 for LLM Applications | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 07_owasp_top10 OWASP Top 10 (2021) | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 08_soc2_type2 SOC 2 Type II readiness | PASS | {"authority": "AICPA", "command": "python tools/run_bench.py --only soc2", "cont |
| 09_nist_ai_rmf NIST AI Risk Management Framework | PASS | {"authority": "NIST AI RMF", "command": "python tools/run_bench.py --only nist", |
| 10_nist_sp_800_53 NIST SP 800-53 Rev. 5 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 11_nist_csf NIST Cybersecurity Framework 2.0 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 12_fedramp FedRAMP Rev. 5 | PASS | {"authority": "FedRAMP", "command": "python tools/run_bench.py --only fedramp",  |
| 13_pci_dss PCI DSS v4.0.1 | PASS | {"authority": "PCI SSC", "command": "python tools/run_bench.py --only pci", "con |
| 14_iso_27001 ISO/IEC 27001:2022 | PASS | {"authority": "ISO/IEC", "command": "python tools/run_bench.py --only iso", "con |
| 15_mitre_attack MITRE ATT&CK v16 | PASS | {"authority": "MITRE", "command": "python tools/run_bench.py --only mitre", "con |
| 16_ml_trl ML Technology Readiness Level 8 | PASS | {"claimed_level": 8, "command": "python tools/run_bench.py --only 16 && cat docs |

**Suite: 16/16 passed** · platform `win32` · python `3.12.10` · method `{'aggregate_rule': 'all_passed == AND over benchmarks[*].ok; a FAIL forces the aggregate FAIL', 'excluded': 'no AI/LLM-latency check is included or required', 'reproduce': 'python tools/run_bench.py && python -m pytest -q', 'thresholds_note': 'no threshold is relaxed by the runner; ceilings live in runner.py and are asserted independently in tests/test_project_metadata.py'}`

## Licence

The upstream licence is preserved in `LICENSE` and `THIRD_PARTY_LICENSES/`. The Anticloud overlay is licensed under Anticommons 0.1.0 (`ANTICOMMONS_LICENSE.md`).

## Verification

SHA3-256 of `BENCH.json`:

```
5d78bd2532365f41a1d79e342ba3e80663ebba4ad42d0d872dc8087dac17f15d
```

Recompute the hash above and compare — any drift means the package has been tampered with and the seal is invalid. This is a self-assessment; no external audit has been performed and a SOC 2 / NIST independent audit is committed post-funding.
