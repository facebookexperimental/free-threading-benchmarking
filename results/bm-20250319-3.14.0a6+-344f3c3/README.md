# Results

- fork: python/344f3c3fd41091188b7e
- version: 3.14.0a6+
- config: 
- commit hash: [344f3c3](https://github.com/python/cpython/commit/344f3c3)
- commit date: 2025-03-19T23:46:25Z
- commit merge base: [6827c5129c5541a8608323fceda2233d542a5ec2](https://github.com/python/cpython/commit/6827c5129c5541a8608323fceda2233d542a5ec2)
- ref: 344f3c3fd41091188b7e

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13959309305)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.md)
- [📈time plot](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 81.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.svg)

