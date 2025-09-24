# Results

- fork: python/1a2e00c97acfe9f79722
- version: 3.15.0a0
- config: NOGIL
- commit hash: [1a2e00c](https://github.com/python/cpython/commit/1a2e00c)
- commit date: 2025-09-23T21:31:42+03:00
- commit merge base: [6ec058a1f7fcc016fa3b7432bcd0aa6e7d2b21ce](https://github.com/python/cpython/commit/6ec058a1f7fcc016fa3b7432bcd0aa6e7d2b21ce)
- ref: 1a2e00c97acfe9f79722

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17962582155)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 82.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.12.6.md)
- [📈time plot](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 97.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-base-mem.svg)
- [📄table](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-base.md)
- [📈time plot](bm-20250923-vultr-x86_64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17962582155)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 99.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.12.6.md)
- [📈time plot](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 62.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.017x slower (HPT: reliability of 99.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-base-mem.svg)
- [📄table](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-base.md)
- [📈time plot](bm-20250923-macm4pro-arm64-python-1a2e00c97acfe9f79722-3.15.0a0-1a2e00c-vs-base.svg)

