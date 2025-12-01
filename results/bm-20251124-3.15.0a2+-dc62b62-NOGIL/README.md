# Results

- fork: python/dc62b622524bf49eb539
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [dc62b62](https://github.com/python/cpython/commit/dc62b62)
- commit date: 2025-11-24T22:07:45Z
- commit merge base: [369ce2b139a5b76c9c093cba1cee287cb6ffeec1](https://github.com/python/cpython/commit/369ce2b139a5b76c9c093cba1cee287cb6ffeec1)
- ref: dc62b622524bf49eb539

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19653928175)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 58.02%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x slower (HPT: reliability of 99.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base-mem.svg)
- [📄table](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.svg)

