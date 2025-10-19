# Results

- fork: Fidget-Spinner/tracing_jit
- version: 3.15.0a1+
- config: CLANG,JIT
- commit hash: [f38ef69](https://github.com/Fidget%2dSpinner/cpython/commit/f38ef69)
- commit date: 2025-10-19T00:35:34+01:00
- commit merge base: [bedaea05987738c4c6b958d19cec9621bec09f07](https://github.com/python/cpython/commit/bedaea05987738c4c6b958d19cec9621bec09f07)
- ref: tracing_jit

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18622641436)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251019-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f38ef69.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251019-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f38ef69-vs-3.12.6.md)
- [📈time plot](bm-20251019-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f38ef69-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251019-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f38ef69-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f38ef69-vs-3.13.0rc2.svg)

