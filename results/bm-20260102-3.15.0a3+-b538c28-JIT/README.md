# Results

- fork: python/b538c2832d582a428a6f
- version: 3.15.0a3+
- config: JIT
- commit hash: [b538c28](https://github.com/python/cpython/commit/b538c28)
- commit date: 2026-01-02T20:43:00Z
- commit merge base: [136f6d835588e0f72cecdff855afc8f424381ed5](https://github.com/python/cpython/commit/136f6d835588e0f72cecdff855afc8f424381ed5)
- ref: b538c2832d582a428a6f

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20677295211)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28.json)

### vs. 3.12.6

- Geometric mean: 1.245x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.12.6.md)
- [📈time plot](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.155x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.13.0rc2.md)
- [📈time plot](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-base-mem.svg)
- [📄table](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-base.md)
- [📈time plot](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-base.svg)

