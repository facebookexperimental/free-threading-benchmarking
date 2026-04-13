# Results

- fork: python/480edc1aae0f54e34d21
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [480edc1](https://github.com/python/cpython/commit/480edc1)
- commit date: 2026-04-12T18:15:01-04:00
- commit merge base: [b29afe62f7236f7161c2670dccc24368217a7fb1](https://github.com/python/cpython/commit/b29afe62f7236f7161c2670dccc24368217a7fb1)
- ref: 480edc1aae0f54e34d21

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24320588997)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 62.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.12.6.md)
- [📈time plot](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 89.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-base-mem.svg)
- [📄table](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-base.md)
- [📈time plot](bm-20260412-vultr-x86_64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24320588997)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.12.6.md)
- [📈time plot](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 55.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-base-mem.svg)
- [📄table](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-base.md)
- [📈time plot](bm-20260412-macm4pro-arm64-python-480edc1aae0f54e34d21-3.15.0a8%2B-480edc1-vs-base.svg)

