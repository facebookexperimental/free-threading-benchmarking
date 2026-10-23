# Results

- fork: python/fd657b067473fdf549df
- version: 3.16.0a1+dev
- config: 
- commit hash: [fd657b0](https://github.com/python/cpython/commit/fd657b0)
- commit date: 2026-10-23T00:36:04Z
- commit merge base: [badd5d5ceb25aed7a402a30e265b653920e0dd40](https://github.com/python/cpython/commit/badd5d5ceb25aed7a402a30e265b653920e0dd40)
- ref: fd657b067473fdf549df

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39879451555)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0.json)

### vs. 3.12.6

- Geometric mean: 1.208x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.12.6.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.116x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-fd657b067473fdf549df-3.16.0a1%2Bdev-fd657b0-vs-3.13.0rc2.svg)

