# Results

- fork: Fidget-Spinner/tracing_jit
- version: 3.15.0a1+
- config: JIT
- commit hash: [7e7b240](https://github.com/Fidget%2dSpinner/cpython/commit/7e7b240)
- commit date: 2025-10-24T20:22:16+01:00
- commit merge base: [92c0c45563bdc041b2089444897cfe60711a6eff](https://github.com/python/cpython/commit/92c0c45563bdc041b2089444897cfe60711a6eff)
- ref: tracing_jit

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18792354162)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-3.12.6.md)
- [📈time plot](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 99.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-3.13.0rc2.md)
- [📈time plot](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 99.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-base-mem.svg)
- [📄table](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-base.md)
- [📈time plot](bm-20251024-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e7b240-vs-base.svg)

