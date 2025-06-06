# Results

- fork: python/49fb75c676bd422b03ae
- version: 3.14.0a6+
- config: 
- commit hash: [49fb75c](https://github.com/python/cpython/commit/49fb75c)
- commit date: 2025-03-21T23:37:49Z
- commit merge base: [d9411ae3c2f6b59d97a0a16ad3dd148cc58ad943](https://github.com/python/cpython/commit/d9411ae3c2f6b59d97a0a16ad3dd148cc58ad943)
- commit date: 2025-03-21T23:37:49+00:00
- ref: 49fb75c676bd422b03ae

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14003213294)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250321-vultr-x86_64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.12.6.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 95.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14003213294)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.12.6.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 77.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6%2B-49fb75c-vs-3.13.0rc2.svg)

