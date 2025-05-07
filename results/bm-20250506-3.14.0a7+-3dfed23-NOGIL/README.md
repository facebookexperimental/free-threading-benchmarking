# Results

- fork: python/3dfed230928de0f64906
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [3dfed23](https://github.com/python/cpython/commit/3dfed23)
- commit date: 2025-05-06T15:05:20+03:00
- commit merge base: [f8691901d734388a776fe3b66a92ee1dcd11c2f1](https://github.com/python/cpython/commit/f8691901d734388a776fe3b66a92ee1dcd11c2f1)
- ref: 3dfed230928de0f64906

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14872386748)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 87.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.md)
- [📈time plot](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 65.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base-mem.svg)
- [📄table](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base.md)
- [📈time plot](bm-20250506-linux-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14872386748)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23.json)

### vs. 3.12.6

- Geometric mean: 1.007x faster (HPT: reliability of 94.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x slower (HPT: reliability of 96.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base-mem.svg)
- [📄table](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base.md)
- [📈time plot](bm-20250506-vultr-x86_64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14872386748)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 90.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 83.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x slower (HPT: reliability of 99.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base-mem.svg)
- [📄table](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base.md)
- [📈time plot](bm-20250506-macm4pro-arm64-python-3dfed230928de0f64906-3.14.0a7%2B-3dfed23-vs-base.svg)

