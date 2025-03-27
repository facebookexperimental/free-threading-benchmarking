# Results

- fork: Yhg1s/avoid_list_critsect
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [e69e45f](https://github.com/Yhg1s/cpython/commit/e69e45f)
- commit date: 2025-03-27T15:35:33+01:00
- commit merge base: [898e6b395e63ad7f8bbe421adf0af8947d429925](https://github.com/python/cpython/commit/898e6b395e63ad7f8bbe421adf0af8947d429925)
- ref: avoid_list_critsect

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14109454219)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f.json)

### vs. 3.12.6

- Geometric mean: 1.133x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.12.6.md)
- [📈time plot](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 69.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 99.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-base-mem.svg)
- [📄table](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-base.md)
- [📈time plot](bm-20250327-macm4pro-arm64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-base.svg)

