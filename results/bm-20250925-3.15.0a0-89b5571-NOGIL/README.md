# Results

- fork: python/89b5571025a5316ea385
- version: 3.15.0a0
- config: NOGIL
- commit hash: [89b5571](https://github.com/python/cpython/commit/89b5571)
- commit date: 2025-09-25T17:13:45Z
- commit merge base: [bc7b5113760ee3069250131a72e073edaadd3e91](https://github.com/python/cpython/commit/bc7b5113760ee3069250131a72e073edaadd3e91)
- commit date: 2025-09-25T17:13:45+00:00
- ref: 89b5571025a5316ea385

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18024229100)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571.json)

### vs. 3.12.6

- Geometric mean: 1.012x slower (HPT: reliability of 74.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.12.6.md)
- [📈time plot](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x slower (HPT: reliability of 92.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.13.0rc2.md)
- [📈time plot](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-base-mem.svg)
- [📄table](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-base.md)
- [📈time plot](bm-20250925-vultr-x86_64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18024229100)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.40%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.12.6.md)
- [📈time plot](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 54.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.13.0rc2.md)
- [📈time plot](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 97.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-base-mem.svg)
- [📄table](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-base.md)
- [📈time plot](bm-20250925-macm4pro-arm64-python-89b5571025a5316ea385-3.15.0a0-89b5571-vs-base.svg)

