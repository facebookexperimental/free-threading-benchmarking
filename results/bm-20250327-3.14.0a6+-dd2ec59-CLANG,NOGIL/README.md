# Results

- fork: Yhg1s/uniqref_critsection
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [dd2ec59](https://github.com/Yhg1s/cpython/commit/dd2ec59)
- commit date: 2025-03-27T00:28:33+01:00
- commit merge base: [af29d5cfd19bf2656955b9bb782cc89c7aa7000f](https://github.com/python/cpython/commit/af29d5cfd19bf2656955b9bb782cc89c7aa7000f)
- ref: uniqref_critsection

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14095469048)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59.json)

### vs. 3.12.6

- Geometric mean: 1.131x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.12.6.md)
- [📈time plot](bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 66.15%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.13.0rc2.svg)

