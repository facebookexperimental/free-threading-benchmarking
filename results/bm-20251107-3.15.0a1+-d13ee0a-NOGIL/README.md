# Results

- fork: python/d13ee0ae186f4704f3b6
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [d13ee0a](https://github.com/python/cpython/commit/d13ee0a)
- commit date: 2025-11-07T13:46:47-05:00
- commit merge base: [3989e12d39bfe2587e5ba80873c37e0c2d449088](https://github.com/python/cpython/commit/3989e12d39bfe2587e5ba80873c37e0c2d449088)
- ref: d13ee0ae186f4704f3b6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19184932946)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 84.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.12.6.md)
- [📈time plot](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 96.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-base-mem.svg)
- [📄table](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-base.md)
- [📈time plot](bm-20251107-vultr-x86_64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19184932946)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.12.6.md)
- [📈time plot](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 53.55%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.034x slower (HPT: reliability of 99.97%, 1.01x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-base-mem.svg)
- [📄table](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-base.md)
- [📈time plot](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-base.svg)

