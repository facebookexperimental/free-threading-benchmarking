# Results

- fork: Fidget-Spinner/tracing_jit
- version: 3.15.0a1+
- config: JIT
- commit hash: [7e2bc1d](https://github.com/Fidget%2dSpinner/cpython/commit/7e2bc1d)
- commit date: 2025-11-08T16:49:31+00:00
- commit merge base: [b1554146c29182803d1df23d6367c07a429d21ba](https://github.com/python/cpython/commit/b1554146c29182803d1df23d6367c07a429d21ba)
- ref: tracing_jit

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19196184710)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-3.12.6.md)
- [📈time plot](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.014x faster (HPT: reliability of 97.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-base-mem.svg)
- [📄table](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-base.md)
- [📈time plot](bm-20251108-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-7e2bc1d-vs-base.svg)

