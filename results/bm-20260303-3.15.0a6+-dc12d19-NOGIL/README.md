# Results

- fork: python/dc12d1999b88e84d5a6b
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [dc12d19](https://github.com/python/cpython/commit/dc12d19)
- commit date: 2026-03-03T21:41:26Z
- commit merge base: [15f6479c415cc6cd219cd25c1d94bab17d720cbc](https://github.com/python/cpython/commit/15f6479c415cc6cd219cd25c1d94bab17d720cbc)
- commit date: 2026-03-03T21:41:26+00:00
- ref: dc12d1999b88e84d5a6b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22649476367)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 64.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.md)
- [📈time plot](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 86.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.md)
- [📈time plot](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base-mem.svg)
- [📄table](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.md)
- [📈time plot](bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22649476367)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.md)
- [📈time plot](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 59.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.md)
- [📈time plot](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.040x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base-mem.svg)
- [📄table](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.md)
- [📈time plot](bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.svg)

