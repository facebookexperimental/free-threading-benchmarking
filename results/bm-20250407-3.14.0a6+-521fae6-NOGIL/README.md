# Results

- fork: mpage/experiment_noinline
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [521fae6](https://github.com/mpage/cpython/commit/521fae6)
- commit date: 2025-04-07T12:01:48-07:00
- commit merge base: [f0dcb29d3affbbe1ec25b922235f0556bd695067](https://github.com/python/cpython/commit/f0dcb29d3affbbe1ec25b922235f0556bd695067)
- ref: experiment_noinline

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14317317160)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6.json)

### vs. 3.12.6

- Geometric mean: 1.032x faster (HPT: reliability of 72.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-3.12.6.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 86.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-base-mem.svg)
- [📄table](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-base.md)
- [📈time plot](bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6%2B-521fae6-vs-base.svg)

