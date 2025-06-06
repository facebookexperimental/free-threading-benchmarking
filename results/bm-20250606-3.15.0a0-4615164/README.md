# Results

- fork: python/46151648ca8ba1edd2a2
- version: 3.15.0a0
- config: 
- commit hash: [4615164](https://github.com/python/cpython/commit/4615164)
- commit date: 2025-06-06T16:44:43-07:00
- commit merge base: [f00512db20561370faad437853f6ecee0eec4856](https://github.com/python/cpython/commit/f00512db20561370faad437853f6ecee0eec4856)
- ref: 46151648ca8ba1edd2a2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15502217475)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250606-vultr-x86_64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250606-vultr-x86_64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.12.6.md)
- [📈time plot](bm-20250606-vultr-x86_64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250606-vultr-x86_64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.13.0rc2.md)
- [📈time plot](bm-20250606-vultr-x86_64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15502217475)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164.json)

### vs. 3.12.6

- Geometric mean: 1.115x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.12.6.md)
- [📈time plot](bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 98.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.13.0rc2.md)
- [📈time plot](bm-20250606-macm4pro-arm64-python-46151648ca8ba1edd2a2-3.15.0a0-4615164-vs-3.13.0rc2.svg)

