# Results

- fork: python/cf9ef73121cd2b96dd51
- version: 3.15.0a0
- config: NOGIL
- commit hash: [cf9ef73](https://github.com/python/cpython/commit/cf9ef73)
- commit date: 2025-09-16T17:06:44Z
- commit merge base: [530ddd3e06a425b8bb9e8afb657dc7711a5aa2f9](https://github.com/python/cpython/commit/530ddd3e06a425b8bb9e8afb657dc7711a5aa2f9)
- commit date: 2025-09-16T17:06:44+00:00
- ref: cf9ef73121cd2b96dd51

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17782745097)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 82.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.12.6.md)
- [📈time plot](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 96.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-base-mem.svg)
- [📄table](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-base.md)
- [📈time plot](bm-20250916-vultr-x86_64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17782745097)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 99.28%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.12.6.md)
- [📈time plot](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 56.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-base-mem.svg)
- [📄table](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-base.md)
- [📈time plot](bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73-vs-base.svg)

