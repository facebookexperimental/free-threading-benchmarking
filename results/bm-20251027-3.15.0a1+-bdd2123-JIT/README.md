# Results

- fork: Fidget-Spinner/tracing_jit
- version: 3.15.0a1+
- config: JIT
- commit hash: [bdd2123](https://github.com/Fidget%2dSpinner/cpython/commit/bdd2123)
- commit date: 2025-10-27T14:22:05+00:00
- commit merge base: [92c0c45563bdc041b2089444897cfe60711a6eff](https://github.com/python/cpython/commit/92c0c45563bdc041b2089444897cfe60711a6eff)
- ref: tracing_jit

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18844809704)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 99.97%, 1.02x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-3.12.6.md)
- [📈time plot](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 99.91%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-3.13.0rc2.md)
- [📈time plot](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 99.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-base-mem.svg)
- [📄table](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-base.md)
- [📈time plot](bm-20251027-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-bdd2123-vs-base.svg)

