# Results

- fork: python/f5394c257ce4118394fe
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [f5394c2](https://github.com/python/cpython/commit/f5394c2)
- commit date: 2025-10-28T01:40:41+05:30
- commit merge base: [364ae607d8035db8ba92486ebebd8225446c1a90](https://github.com/python/cpython/commit/364ae607d8035db8ba92486ebebd8225446c1a90)
- ref: f5394c257ce4118394fe

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18860046714)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 93.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.12.6.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 82.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.029x slower (HPT: reliability of 99.96%, 1.01x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-base-mem.svg)
- [📄table](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-base.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-base.svg)

