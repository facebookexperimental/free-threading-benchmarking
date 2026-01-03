# Results

- fork: Fidget-Spinner/integration_generato
- version: 3.15.0a3+
- config: JIT
- commit hash: [d8a322c](https://github.com/Fidget%2dSpinner/cpython/commit/d8a322c)
- commit date: 2026-01-03T16:03:02Z
- commit merge base: [b538c2832d582a428a6f4ddc818680c5e05a0745](https://github.com/python/cpython/commit/b538c2832d582a428a6f4ddc818680c5e05a0745)
- ref: integration_generato

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20679636368)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c.json)

### vs. 3.12.6

- Geometric mean: 1.247x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: async_tree_eager_memoization, asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-3.12.6.md)
- [📈time plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.155x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: async_tree_eager_memoization, asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 86.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 async_tree_eager_memoization, asyncio_websockets
- [🧠memory plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-base-mem.svg)
- [📄table](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-base.md)
- [📈time plot](bm-20260103-macm4pro-arm64-Fidget%252dSpinner-integration_generato-3.15.0a3%2B-d8a322c-vs-base.svg)

