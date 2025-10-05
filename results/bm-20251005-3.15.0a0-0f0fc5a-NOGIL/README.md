# Results

- fork: python/0f0fc5a16368ea455411
- version: 3.15.0a0
- config: NOGIL
- commit hash: [0f0fc5a](https://github.com/python/cpython/commit/0f0fc5a)
- commit date: 2025-10-05T08:15:29+08:00
- commit merge base: [880c9526f91960b9cba557a18b54e2c32d2f254e](https://github.com/python/cpython/commit/880c9526f91960b9cba557a18b54e2c32d2f254e)
- ref: 0f0fc5a16368ea455411

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18251475358)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 81.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.12.6.md)
- [📈time plot](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 95.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 99.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-base-mem.svg)
- [📄table](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-base.md)
- [📈time plot](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20251005-vultr-x86_64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-default_base_vs_NOGIL.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18251475358)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 94.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.12.6.md)
- [📈time plot](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 80.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 94.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-base-mem.svg)
- [📄table](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-base.md)
- [📈time plot](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.012x faster (HPT: reliability of 64.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20251005-macm4pro-arm64-python-0f0fc5a16368ea455411-3.15.0a0-0f0fc5a-vs-default_base_vs_NOGIL.svg)

