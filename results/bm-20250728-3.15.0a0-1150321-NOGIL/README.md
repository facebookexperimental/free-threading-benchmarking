# Results

- fork: python/11503211c6e8985a305f
- version: 3.15.0a0
- config: NOGIL
- commit hash: [1150321](https://github.com/python/cpython/commit/1150321)
- commit date: 2025-07-28T12:35:40-07:00
- commit merge base: [d53199101c7e74273d4d550456a994de01b6e3f1](https://github.com/python/cpython/commit/d53199101c7e74273d4d550456a994de01b6e3f1)
- ref: 11503211c6e8985a305f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16583507331)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 93.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.12.6.md)
- [📈time plot](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 97.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.13.0rc2.md)
- [📈time plot](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-base-mem.svg)
- [📄table](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-base.md)
- [📈time plot](bm-20250728-vultr-x86_64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16583507331)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 95.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.12.6.md)
- [📈time plot](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 81.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.13.0rc2.md)
- [📈time plot](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x slower (HPT: reliability of 99.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-base-mem.svg)
- [📄table](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-base.md)
- [📈time plot](bm-20250728-macm4pro-arm64-python-11503211c6e8985a305f-3.15.0a0-1150321-vs-base.svg)

