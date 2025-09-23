# Results

- fork: DinoV/lazy_imports
- version: 3.15.0a0
- config: 
- commit hash: [27836e5](https://github.com/DinoV/cpython/commit/27836e5)
- commit date: 2025-09-22T15:18:41-07:00
- commit merge base: [f0d8583303d28a5312e4096a3d013ab7fd9be560](https://github.com/python/cpython/commit/f0d8583303d28a5312e4096a3d013ab7fd9be560)
- ref: lazy_imports

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17930090631)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mako, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-3.12.6.md)
- [📈time plot](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mako, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x slower (HPT: reliability of 98.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 2to3, mako, sphinx
- [🧠memory plot](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-base-mem.svg)
- [📄table](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-base.md)
- [📈time plot](bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5-vs-base.svg)

