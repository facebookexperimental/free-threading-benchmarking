# Results

- fork: Fidget-Spinner/jit_ft
- version: 3.15.0a3+
- config: JIT,NOGIL
- commit hash: [5d987e8](https://github.com/Fidget%2dSpinner/cpython/commit/5d987e8)
- commit date: 2026-01-10T00:10:48Z
- commit merge base: [95259116ecb4346b570b9f87fd825d1d5901c4f1](https://github.com/python/cpython/commit/95259116ecb4346b570b9f87fd825d1d5901c4f1)
- ref: jit_ft

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20869668843)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260110-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-5d987e8.json)

### vs. 3.12.6

- Geometric mean: 1.188x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260110-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-5d987e8-vs-3.12.6.md)
- [📈time plot](bm-20260110-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-5d987e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.103x faster (HPT: reliability of 99.74%, 1.01x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260110-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-5d987e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260110-macm4pro-arm64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-5d987e8-vs-3.13.0rc2.svg)

