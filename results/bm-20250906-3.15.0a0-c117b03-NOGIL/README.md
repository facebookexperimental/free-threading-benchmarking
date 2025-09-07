# Results

- fork: python/c117b033856ab7873972
- version: 3.15.0a0
- config: NOGIL
- commit hash: [c117b03](https://github.com/python/cpython/commit/c117b03)
- commit date: 2025-09-06T16:53:49-04:00
- commit merge base: [bbe00d53e9f598b012470cf077357cbbcbee737f](https://github.com/python/cpython/commit/bbe00d53e9f598b012470cf077357cbbcbee737f)
- ref: c117b033856ab7873972

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17521278407)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 86.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.12.6.md)
- [📈time plot](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 98.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.13.0rc2.md)
- [📈time plot](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-base-mem.svg)
- [📄table](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-base.md)
- [📈time plot](bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17521278407)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 96.17%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.12.6.md)
- [📈time plot](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 69.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.13.0rc2.md)
- [📈time plot](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.017x slower (HPT: reliability of 99.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-base-mem.svg)
- [📄table](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-base.md)
- [📈time plot](bm-20250906-macm4pro-arm64-python-c117b033856ab7873972-3.15.0a0-c117b03-vs-base.svg)

