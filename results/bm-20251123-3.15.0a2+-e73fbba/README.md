# Results

- fork: python/e73fbbacbba0dc65f852
- version: 3.15.0a2+
- config: 
- commit hash: [e73fbba](https://github.com/python/cpython/commit/e73fbba)
- commit date: 2025-11-23T00:26:50Z
- commit merge base: [227b9d326ec7eba35942a4eb451c7db244a33a6c](https://github.com/python/cpython/commit/227b9d326ec7eba35942a4eb451c7db244a33a6c)
- commit date: 2025-11-23T00:26:50+00:00
- ref: e73fbbacbba0dc65f852

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19603381702)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.12.6.md)
- [📈time plot](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.13.0rc2.md)
- [📈time plot](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 76.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base-mem.svg)
- [📄table](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base.md)
- [📈time plot](bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19603381702)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba.json)

### vs. 3.12.6

- Geometric mean: 1.142x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.12.6.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.13.0rc2.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 99.59%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base-mem.svg)
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base.svg)

