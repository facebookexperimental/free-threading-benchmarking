# Results

- fork: Fidget-Spinner/call_function_ex_py
- version: 3.15.0a3+
- config: JIT
- commit hash: [884a7a7](https://github.com/Fidget%2dSpinner/cpython/commit/884a7a7)
- commit date: 2026-01-02T10:51:49Z
- commit merge base: [e5ad7b7694c47555e3eac3fcb227a4b1b7b781c4](https://github.com/python/cpython/commit/e5ad7b7694c47555e3eac3fcb227a4b1b7b781c4)
- commit date: 2026-01-02T10:51:49+00:00
- ref: call_function_ex_py

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20656340799)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7.json)

### vs. 3.12.6

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.12.6.md)
- [📈time plot](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 92.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-base-mem.svg)
- [📄table](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-base.md)
- [📈time plot](bm-20260102-vultr-x86_64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20656340799)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7.json)

### vs. 3.12.6

- Geometric mean: 1.273x faster (HPT: reliability of 100.00%, 1.16x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.12.6.md)
- [📈time plot](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.180x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.016x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-base-mem.svg)
- [📄table](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-base.md)
- [📈time plot](bm-20260102-macm4pro-arm64-Fidget%252dSpinner-call_function_ex_py-3.15.0a3%2B-884a7a7-vs-base.svg)

