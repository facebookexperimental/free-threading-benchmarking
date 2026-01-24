# Results

- fork: Fidget-Spinner/loop_2000
- version: 3.15.0a5+
- config: JIT
- commit hash: [cec96a9](https://github.com/Fidget%2dSpinner/cpython/commit/cec96a9)
- commit date: 2026-01-24T12:20:15Z
- commit merge base: [012c498035a9adfe9fd218907db1550ecb057f77](https://github.com/python/cpython/commit/012c498035a9adfe9fd218907db1550ecb057f77)
- commit date: 2026-01-24T12:20:15+00:00
- ref: loop_2000

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21315070429)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9.json)

### vs. 3.12.6

- Geometric mean: 1.137x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.12.6.md)
- [📈time plot](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 98.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-base-mem.svg)
- [📄table](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-base.md)
- [📈time plot](bm-20260124-vultr-x86_64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21315070429)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9.json)

### vs. 3.12.6

- Geometric mean: 1.263x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.12.6.md)
- [📈time plot](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.172x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-base-mem.svg)
- [📄table](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-base.md)
- [📈time plot](bm-20260124-macm4pro-arm64-Fidget%252dSpinner-loop_2000-3.15.0a5%2B-cec96a9-vs-base.svg)

