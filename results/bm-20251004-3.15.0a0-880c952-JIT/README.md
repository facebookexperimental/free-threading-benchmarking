# Results

- fork: python/880c9526f91960b9cba5
- version: 3.15.0a0
- config: JIT
- commit hash: [880c952](https://github.com/python/cpython/commit/880c952)
- commit date: 2025-10-04T22:06:56+01:00
- commit merge base: [0b2168275e8ec491fe7ea6f8c662e804437dfdab](https://github.com/python/cpython/commit/0b2168275e8ec491fe7ea6f8c662e804437dfdab)
- ref: 880c9526f91960b9cba5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18251316313)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.12.6.md)
- [📈time plot](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.13.0rc2.md)
- [📈time plot](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x faster (HPT: reliability of 99.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-base-mem.svg)
- [📄table](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-base.md)
- [📈time plot](bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18251316313)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.12.6.md)
- [📈time plot](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 83.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.13.0rc2.md)
- [📈time plot](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.032x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-base-mem.svg)
- [📄table](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-base.md)
- [📈time plot](bm-20251004-macm4pro-arm64-python-880c9526f91960b9cba5-3.15.0a0-880c952-vs-base.svg)

