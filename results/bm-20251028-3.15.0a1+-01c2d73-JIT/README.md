# Results

- fork: Fidget-Spinner/tracing_jit
- version: 3.15.0a1+
- config: JIT
- commit hash: [01c2d73](https://github.com/Fidget%2dSpinner/cpython/commit/01c2d73)
- commit date: 2025-10-28T00:12:59+00:00
- commit merge base: [a7160912274003672dc116d918260c0a81551c21](https://github.com/python/cpython/commit/a7160912274003672dc116d918260c0a81551c21)
- ref: tracing_jit

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18859814110)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-3.12.6.md)
- [📈time plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 98.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-base-mem.svg)
- [📄table](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-base.md)
- [📈time plot](bm-20251028-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-01c2d73-vs-base.svg)

