# Results

- fork: python/1fd66eadd258223a0e34
- version: 3.15.0a7+
- config: JIT
- commit hash: [1fd66ea](https://github.com/python/cpython/commit/1fd66ea)
- commit date: 2026-03-28T20:21:19Z
- commit merge base: [5bf3a31bc23818907f8e5844d65d610835b4b672](https://github.com/python/cpython/commit/5bf3a31bc23818907f8e5844d65d610835b4b672)
- commit date: 2026-03-28T20:21:19+00:00
- ref: 1fd66eadd258223a0e34

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23697597298)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea.json)

### vs. 3.12.6

- Geometric mean: 1.152x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.12.6.md)
- [📈time plot](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.13.0rc2.md)
- [📈time plot](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-base-mem.svg)
- [📄table](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-base.md)
- [📈time plot](bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23697597298)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea.json)

### vs. 3.12.6

- Geometric mean: 1.277x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.12.6.md)
- [📈time plot](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.184x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.13.0rc2.md)
- [📈time plot](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-base-mem.svg)
- [📄table](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-base.md)
- [📈time plot](bm-20260328-macm4pro-arm64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-vs-base.svg)

