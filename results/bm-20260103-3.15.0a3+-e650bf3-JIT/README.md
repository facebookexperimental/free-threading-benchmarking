# Results

- fork: Fidget-Spinner/loop_peeling
- version: 3.15.0a3+
- config: JIT
- commit hash: [e650bf3](https://github.com/Fidget%2dSpinner/cpython/commit/e650bf3)
- commit date: 2026-01-03T12:29:08Z
- commit merge base: [b538c2832d582a428a6f4ddc818680c5e05a0745](https://github.com/python/cpython/commit/b538c2832d582a428a6f4ddc818680c5e05a0745)
- ref: loop_peeling

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20677295211)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3.json)

### vs. 3.12.6

- Geometric mean: 1.261x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-3.12.6.md)
- [📈time plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.168x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-3.13.0rc2.md)
- [📈time plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_websockets
- [🧠memory plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-base-mem.svg)
- [📄table](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-base.md)
- [📈time plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-loop_peeling-3.15.0a3%2B-e650bf3-vs-base.svg)

