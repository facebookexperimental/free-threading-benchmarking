# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (8d2d7bb)](results/bm-20251220-3.15.0a3%2B-8d2d7bb/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (8d2d7bb)](results/bm-20251220-3.15.0a3%2B-8d2d7bb-PYTHON_UOPS/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-12-20](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL) | python/8d2d7bb2e754f8649a68 | 8d2d7bb (NOGIL) | 1.035x ↓<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.svg)[🧠](results/bm-20251220-3.15.0a3%2B-8d2d7bb-NOGIL/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base-mem.svg) |
| [2025-12-20](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT) | python/8d2d7bb2e754f8649a68 | 8d2d7bb (JIT) | 1.119x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.svg) | 1.081x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.svg) | 1.035x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.svg)[🧠](results/bm-20251220-3.15.0a3%2B-8d2d7bb-JIT/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base-mem.svg) |
| [2025-12-20](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG) | python/8d2d7bb2e754f8649a68 | 8d2d7bb (CLANG) | 1.128x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.svg) | 1.091x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.svg) | 1.048x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.svg)[🧠](results/bm-20251220-3.15.0a3%2B-8d2d7bb-CLANG/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base-mem.svg) |
| [2025-12-20](results/bm-20251220-3.15.0a3%2B-8d2d7bb) | python/8d2d7bb2e754f8649a68 | 8d2d7bb | 1.075x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20251220-3.15.0a3%2B-8d2d7bb/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.md)[📈](results/bm-20251220-3.15.0a3%2B-8d2d7bb/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.svg) |  |
| [2025-12-19](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL) | python/e46f28c6afce9c85e4bc | e46f28c (NOGIL) | 1.031x ↓<br>[📄](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.12.6.md)[📈](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.13.0rc2.md)[📈](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-base.md)[📈](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-base.svg)[🧠](results/bm-20251219-3.15.0a3%2B-e46f28c-NOGIL/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-base-mem.svg) |
| [2025-12-19](results/bm-20251219-3.15.0a3%2B-e46f28c) | python/e46f28c6afce9c85e4bc | e46f28c | 1.068x ↑<br>[📄](results/bm-20251219-3.15.0a3%2B-e46f28c/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.12.6.md)[📈](results/bm-20251219-3.15.0a3%2B-e46f28c/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20251219-3.15.0a3%2B-e46f28c/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.13.0rc2.md)[📈](results/bm-20251219-3.15.0a3%2B-e46f28c/bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.13.0rc2.svg) |  |
| [2025-12-18](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL) | python/1391ee664c8f019996e0 | 1391ee6 (NOGIL) | 1.029x ↓<br>[📄](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.12.6.md)[📈](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.13.0rc2.md)[📈](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-base.md)[📈](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-base.svg)[🧠](results/bm-20251218-3.15.0a3%2B-1391ee6-NOGIL/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-base-mem.svg) |
| [2025-12-18](results/bm-20251218-3.15.0a3%2B-1391ee6) | python/1391ee664c8f019996e0 | 1391ee6 | 1.073x ↑<br>[📄](results/bm-20251218-3.15.0a3%2B-1391ee6/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.12.6.md)[📈](results/bm-20251218-3.15.0a3%2B-1391ee6/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20251218-3.15.0a3%2B-1391ee6/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.13.0rc2.md)[📈](results/bm-20251218-3.15.0a3%2B-1391ee6/bm-20251218-vultr-x86_64-python-1391ee664c8f019996e0-3.15.0a3%2B-1391ee6-vs-3.13.0rc2.svg) |  |
| [2025-12-18](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL) | Fidget-Spinner/jit_ft | 00ae7b5 (JIT) (NOGIL) | 1.003x ↑<br>[📄](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.12.6.md)[📈](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.12.6.svg) | 1.030x ↓<br>[📄](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.13.0rc2.md)[📈](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-3.13.0rc2.svg) | 1.034x ↑<br>[📄](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-base.md)[📈](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-base.svg)[🧠](results/bm-20251218-3.15.0a3%2B-00ae7b5-JIT%2CNOGIL/bm-20251218-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-00ae7b5-vs-base-mem.svg) |
| [2025-12-17](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL) | python/8b64dd853ded593e1f0c | 8b64dd8 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base.svg)[🧠](results/bm-20251217-3.15.0a3%2B-8b64dd8-NOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base-mem.svg) |
| [2025-12-17](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL) | python/8b64dd853ded593e1f0c | 8b64dd8 (JIT) (NOGIL) | 1.035x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base.svg)[🧠](results/bm-20251217-3.15.0a3%2B-8b64dd8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base-mem.svg) |
| [2025-12-17](results/bm-20251217-3.15.0a3%2B-8b64dd8) | python/8b64dd853ded593e1f0c | 8b64dd8 | 1.075x ↑<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20251217-3.15.0a3%2B-8b64dd8/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.md)[📈](results/bm-20251217-3.15.0a3%2B-8b64dd8/bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-f96af45-JIT) | Fidget-Spinner/jit_lower_trace_limi | f96af45 (JIT) | 1.162x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base-mem.svg) |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL) | python/dc62b622524bf49eb539 | dc62b62 (NOGIL) | 1.109x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg) | 1.020x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base-mem.svg) |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT) | python/main | dc62b62 (JIT) | 1.166x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base-mem.svg) |


<!-- END table -->

`*` indicates that the exact same versions of pyperformance was not used.

![Longitudinal speed improvement](/longitudinal.svg)

Improvement of the geometric mean of key merged benchmarks, computed with `pyperf compare`.
The results have a resolution of 0.01 (1%).

![Configuration speed improvement](/configs.svg)

## Documentation

### Running benchmarks from the GitHub web UI

Visit the 🔒 [benchmark action](../../actions/workflows/benchmark.yml) and click the "Run Workflow" button.

The available parameters are:

- `fork`: The fork of CPython to benchmark.
  If benchmarking a pull request, this would normally be your GitHub username.
- `ref`: The branch, tag or commit SHA to benchmark.
  If a SHA, it must be the full SHA, since finding it by a prefix is not supported.
- `machine`: The machine to run on.
  One of `linux-amd64` (default), `windows-amd64`, `darwin-arm64` or `all`.
- `benchmark_base`: If checked, the base of the selected branch will also be benchmarked.
  The base is determined by running `git merge-base upstream/main $ref`.
- `pystats`: If checked, collect the pystats from running the benchmarks.

To watch the progress of the benchmark, select it from the 🔒 [benchmark action page](../../actions/workflows/benchmark.yml).
It may be canceled from there as well.
To show only your benchmark workflows, select your GitHub ID from the "Actor" dropdown.

When the benchmarking is complete, the results are published to this repository and will appear in the [complete table](RESULTS.md).
Each set of benchmarks will have:

- The raw `.json` results from pyperformance.
- Comparisons against important reference releases, as well as the merge base of the branch if `benchmark_base` was selected. These include
  - A markdown table produced by `pyperf compare_to`.
  - A set of "violin" plots showing the distribution of results for each benchmark.

The most convenient way to get results locally is to clone this repo and `git pull` from it.

### Running benchmarks from the GitHub CLI

To automate benchmarking runs, it may be more convenient to use the [GitHub CLI](https://cli.github.com/).
Once you have `gh` installed and configured, you can run benchmarks by cloning this repository and then from inside it:

```bash session
gh workflow run benchmark.yml -f fork=me -f ref=my_branch
```

Any of the parameters described above are available at the commandline using the `-f key=value` syntax.

### Collecting Linux perf profiling data

To collect Linux perf sampling profile data for a benchmarking run, run the `_benchmark` action and check the `perf` checkbox.
Follow this by a run of the `_generate` action to regenerate the plots.

## License

This repo is licensed under the BSD 3-Clause License, as found in the LICENSE file.
