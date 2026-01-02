# Results

- fork: Fidget-Spinner/cover_more_frames
- version: 3.15.0a3+
- config: JIT
- commit hash: [b1e4adf](https://github.com/Fidget%2dSpinner/cpython/commit/b1e4adf)
- commit date: 2026-01-01T23:41:56Z
- commit merge base: [e5ad7b7694c47555e3eac3fcb227a4b1b7b781c4](https://github.com/python/cpython/commit/e5ad7b7694c47555e3eac3fcb227a4b1b7b781c4)
- ref: cover_more_frames

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20648800708)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260101-macm4pro-arm64-Fidget%252dSpinner-cover_more_frames-3.15.0a3%2B-b1e4adf.json)

### vs. 3.12.6

- Geometric mean: 1.238x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260101-macm4pro-arm64-Fidget%252dSpinner-cover_more_frames-3.15.0a3%2B-b1e4adf-vs-3.12.6.md)
- [📈time plot](bm-20260101-macm4pro-arm64-Fidget%252dSpinner-cover_more_frames-3.15.0a3%2B-b1e4adf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.149x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260101-macm4pro-arm64-Fidget%252dSpinner-cover_more_frames-3.15.0a3%2B-b1e4adf-vs-3.13.0rc2.md)
- [📈time plot](bm-20260101-macm4pro-arm64-Fidget%252dSpinner-cover_more_frames-3.15.0a3%2B-b1e4adf-vs-3.13.0rc2.svg)

