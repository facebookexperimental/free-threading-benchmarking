# Results

- fork: Fidget-Spinner/tail_call_force_on
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [0227a6d](https://github.com/Fidget%2dSpinner/cpython/commit/0227a6d)
- commit date: 2025-04-03T22:17:15+08:00
- commit merge base: [06822bfbf625e9777813542be0b8a2d10a685f30](https://github.com/python/cpython/commit/06822bfbf625e9777813542be0b8a2d10a685f30)
- ref: tail_call_force_on

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14245438897)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250403-macm4pro-arm64-Fidget%252dSpinner-tail_call_force_on-3.14.0a6%2B-0227a6d.json)

### vs. 3.12.6

- Geometric mean: 1.156x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250403-macm4pro-arm64-Fidget%252dSpinner-tail_call_force_on-3.14.0a6%2B-0227a6d-vs-3.12.6.md)
- [📈time plot](bm-20250403-macm4pro-arm64-Fidget%252dSpinner-tail_call_force_on-3.14.0a6%2B-0227a6d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x faster (HPT: reliability of 85.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250403-macm4pro-arm64-Fidget%252dSpinner-tail_call_force_on-3.14.0a6%2B-0227a6d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250403-macm4pro-arm64-Fidget%252dSpinner-tail_call_force_on-3.14.0a6%2B-0227a6d-vs-3.13.0rc2.svg)

