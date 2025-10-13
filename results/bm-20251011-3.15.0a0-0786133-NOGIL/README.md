# Results

- fork: Fidget-Spinner/msvc_tailcall_take_t
- version: 3.15.0a0
- config: NOGIL
- commit hash: [0786133](https://github.com/Fidget%2dSpinner/cpython/commit/0786133)
- commit date: 2025-10-11T22:38:13+01:00
- commit merge base: [5776d0d2e08f4d93dcd62d875bae8c1396a04ba4](https://github.com/python/cpython/commit/5776d0d2e08f4d93dcd62d875bae8c1396a04ba4)
- ref: msvc_tailcall_take_t

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18473503438)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 82.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.12.6.md)
- [📈time plot](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 93.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.13.0rc2.md)
- [📈time plot](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 77.95%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-base-mem.svg)
- [📄table](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-base.md)
- [📈time plot](bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-base.svg)

