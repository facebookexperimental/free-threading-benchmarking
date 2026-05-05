# Results

- fork: python/24aa562062fced910e8b
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [24aa562](https://github.com/python/cpython/commit/24aa562)
- commit date: 2026-05-05T12:10:34+03:00
- commit merge base: [586c97a67b1769e12980d9dd66de58167f7ec38d](https://github.com/python/cpython/commit/586c97a67b1769e12980d9dd66de58167f7ec38d)
- ref: 24aa562062fced910e8b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25383585976)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 81.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.12.6.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 88.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.13.0rc2.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.13.0rc2.svg)

