# Results

- fork: python/9fcebb361190f5d33825
- version: 3.15.0a0
- config: NOGIL
- commit hash: [9fcebb3](https://github.com/python/cpython/commit/9fcebb3)
- commit date: 2025-05-07T19:05:06-05:00
- commit merge base: [27128e4fa8e2575025fb6d943fbc84000c7c3e8a](https://github.com/python/cpython/commit/27128e4fa8e2575025fb6d943fbc84000c7c3e8a)
- ref: 9fcebb361190f5d33825

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14895909120)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 93.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.12.6.md)
- [📈time plot](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x faster (HPT: reliability of 71.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base-mem.svg)
- [📄table](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base.md)
- [📈time plot](bm-20250507-linux-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14895909120)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3.json)

### vs. 3.12.6

- Geometric mean: 1.007x faster (HPT: reliability of 91.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.12.6.md)
- [📈time plot](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x slower (HPT: reliability of 98.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base-mem.svg)
- [📄table](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base.md)
- [📈time plot](bm-20250507-vultr-x86_64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14895909120)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 97.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.12.6.md)
- [📈time plot](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 70.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x slower (HPT: reliability of 95.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base-mem.svg)
- [📄table](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base.md)
- [📈time plot](bm-20250507-macm4pro-arm64-python-9fcebb361190f5d33825-3.15.0a0-9fcebb3-vs-base.svg)

