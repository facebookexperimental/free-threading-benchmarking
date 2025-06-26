# Results

- fork: python/6227662ff3bf838d31e9
- version: 3.15.0a0
- config: 
- commit hash: [6227662](https://github.com/python/cpython/commit/6227662)
- commit date: 2025-06-25T13:40:00-04:00
- commit merge base: [cbfaf41caf135b8598a560854cd59e992a2ccfed](https://github.com/python/cpython/commit/cbfaf41caf135b8598a560854cd59e992a2ccfed)
- ref: 6227662ff3bf838d31e9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15890051392)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.md)
- [📈time plot](bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.md)
- [📈time plot](bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15890051392)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.md)
- [📈time plot](bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 81.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.md)
- [📈time plot](bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.svg)

