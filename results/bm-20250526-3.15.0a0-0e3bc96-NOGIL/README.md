# Results

- fork: python/0e3bc962c6462f836751
- version: 3.15.0a0
- config: NOGIL
- commit hash: [0e3bc96](https://github.com/python/cpython/commit/0e3bc96)
- commit date: 2025-05-26T01:05:08+02:00
- commit merge base: [a32ea456992fedfc9ce61561c88056de3c18cffd](https://github.com/python/cpython/commit/a32ea456992fedfc9ce61561c88056de3c18cffd)
- ref: 0e3bc962c6462f836751

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15243569876)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96.json)

### vs. 3.12.6

- Geometric mean: 1.012x faster (HPT: reliability of 88.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.12.6.md)
- [📈time plot](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 96.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.13.0rc2.md)
- [📈time plot](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-base-mem.svg)
- [📄table](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-base.md)
- [📈time plot](bm-20250526-vultr-x86_64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15243569876)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.33%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.12.6.md)
- [📈time plot](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 51.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.13.0rc2.md)
- [📈time plot](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 96.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-base-mem.svg)
- [📄table](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-base.md)
- [📈time plot](bm-20250526-macm4pro-arm64-python-0e3bc962c6462f836751-3.15.0a0-0e3bc96-vs-base.svg)

