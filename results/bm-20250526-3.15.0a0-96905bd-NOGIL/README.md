# Results

- fork: python/96905bdd273d2e5724d2
- version: 3.15.0a0
- config: NOGIL
- commit hash: [96905bd](https://github.com/python/cpython/commit/96905bd)
- commit date: 2025-05-26T21:43:35Z
- commit merge base: [3c0525126ef95efe2f578e93db09f3282e3ca08f](https://github.com/python/cpython/commit/3c0525126ef95efe2f578e93db09f3282e3ca08f)
- commit date: 2025-05-26T21:43:35+00:00
- ref: 96905bdd273d2e5724d2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15264012481)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 88.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.12.6.md)
- [📈time plot](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 96.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.23x
- [🧠memory plot](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-base-mem.svg)
- [📄table](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-base.md)
- [📈time plot](bm-20250526-vultr-x86_64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15264012481)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 98.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.12.6.md)
- [📈time plot](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 56.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 93.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-base-mem.svg)
- [📄table](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-base.md)
- [📈time plot](bm-20250526-macm4pro-arm64-python-96905bdd273d2e5724d2-3.15.0a0-96905bd-vs-base.svg)

