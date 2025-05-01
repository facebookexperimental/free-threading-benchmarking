# Results

- fork: python/011979132648d50f83d4
- version: 3.14.0a7+
- config: NOGIL
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

- Geometric mean: 1.084x faster (HPT: reliability of 78.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.md)
- [📈time plot](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 57.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base-mem.svg)
- [📄table](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base.md)
- [📈time plot](bm-20250501-linux-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14767060794)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791.json)

### vs. 3.12.6

- Geometric mean: 1.020x faster (HPT: reliability of 87.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x slower (HPT: reliability of 93.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.085x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base-mem.svg)
- [📄table](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14767060794)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 95.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 71.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 91.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base-mem.svg)
- [📄table](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-011979132648d50f83d4-3.14.0a7%2B-0119791-vs-base.svg)

