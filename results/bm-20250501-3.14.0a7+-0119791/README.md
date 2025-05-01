# Results

- fork: python/011979132648d50f83d4
- version: 3.14.0a7+
- config: 
- commit hash: [0119791](https://github.com/python/cpython/commit/0119791)
- commit date: 2025-05-01T08:39:26+09:00
- commit merge base: [cb35c11d82efd2959bda0397abcc1719bf6bb0cb](https://github.com/python/cpython/commit/cb35c11d82efd2959bda0397abcc1719bf6bb0cb)
- ref: 011979132648d50f83d4

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14767060794)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791.json)

### vs. 3.12.6

- Geometric mean: 1.188x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.md)
- [📈time plot](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.144x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14767060794)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14767060794)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 63.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.svg)

