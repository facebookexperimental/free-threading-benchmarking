# Results

- fork: python/1953713d0d67a4f54ff7
- version: 3.15.0a0
- config: 
- commit hash: [1953713](https://github.com/python/cpython/commit/1953713)
- commit date: 2025-07-05T15:54:26-07:00
- commit merge base: [5dac137b9f75c5c1d5096101bcd33d565d0526e4](https://github.com/python/cpython/commit/5dac137b9f75c5c1d5096101bcd33d565d0526e4)
- ref: 1953713d0d67a4f54ff7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16093366570)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-pystats.json)
- [pystats table](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-pystats.md)
- [raw results](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.12.6.md)
- [📈time plot](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.13.0rc2.md)
- [📈time plot](bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16093366570)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250705-macm4pro-arm64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250705-macm4pro-arm64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.12.6.md)
- [📈time plot](bm-20250705-macm4pro-arm64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 64.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250705-macm4pro-arm64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.13.0rc2.md)
- [📈time plot](bm-20250705-macm4pro-arm64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-vs-3.13.0rc2.svg)

