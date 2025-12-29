# Results

- fork: Fidget-Spinner/jit_ft
- version: 3.15.0a3+
- config: JIT,NOGIL
- commit hash: [0678505](https://github.com/Fidget%2dSpinner/cpython/commit/0678505)
- commit date: 2025-12-28T23:57:53Z
- commit merge base: [daa9aa4c0a8490f09b01339b6928434d7fe02843](https://github.com/python/cpython/commit/daa9aa4c0a8490f09b01339b6928434d7fe02843)
- ref: jit_ft

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20561353582)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505.json)

### vs. 3.12.6

- Geometric mean: 1.165x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-3.12.6.md)
- [📈time plot](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x faster (HPT: reliability of 98.35%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-3.13.0rc2.md)
- [📈time plot](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-base-mem.svg)
- [📄table](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-base.md)
- [📈time plot](bm-20251228-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-0678505-vs-base.svg)

