# Results

- fork: nascheme/gh_132380_tp_lookup_
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [d3f79e5](https://github.com/nascheme/cpython/commit/d3f79e5)
- commit date: 2025-04-17T11:32:48-07:00
- commit merge base: [e42bda9441119c7952ada23e88e6f4ab79df86c2](https://github.com/python/cpython/commit/e42bda9441119c7952ada23e88e6f4ab79df86c2)
- ref: gh_132380_tp_lookup_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14523227913)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5.json)

### vs. 3.12.6

- Geometric mean: 1.027x faster (HPT: reliability of 68.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-3.12.6.md)
- [📈time plot](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 95.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 71.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-base-mem.svg)
- [📄table](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-base.md)
- [📈time plot](bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7%2B-d3f79e5-vs-base.svg)

