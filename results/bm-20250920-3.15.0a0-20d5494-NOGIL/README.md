# Results

- fork: python/20d5494c88985beb925b
- version: 3.15.0a0
- config: NOGIL
- commit hash: [20d5494](https://github.com/python/cpython/commit/20d5494)
- commit date: 2025-09-20T11:01:44+03:00
- commit merge base: [69c6b438e84ef2bb94a587e49946a2a4b6454fb3](https://github.com/python/cpython/commit/69c6b438e84ef2bb94a587e49946a2a4b6454fb3)
- ref: 20d5494c88985beb925b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17886510324)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 91.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 96.69%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 95.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base-mem.svg)
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-default_base_vs_NOGIL.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17886510324)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 96.01%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 67.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 61.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base-mem.svg)
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.022x slower (HPT: reliability of 99.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-default_base_vs_NOGIL.svg)

