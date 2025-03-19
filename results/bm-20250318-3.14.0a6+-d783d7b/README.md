# Results

- fork: python/d783d7b51d31db568de6
- version: 3.14.0a6+
- config: 
- commit hash: [d783d7b](https://github.com/python/cpython/commit/d783d7b)
- commit date: 2025-03-18T23:37:12Z
- commit merge base: [01b5abbc53b2a9ee8d85e0518c98efce27dbd061](https://github.com/python/cpython/commit/01b5abbc53b2a9ee8d85e0518c98efce27dbd061)
- ref: d783d7b51d31db568de6

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13936099299)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 76.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.svg)

