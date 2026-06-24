# Results

- fork: python/11f032f904c8019b332a
- version: 3.16.0a0
- config: 
- commit hash: [11f032f](https://github.com/python/cpython/commit/11f032f)
- commit date: 2026-06-15T21:51:39-07:00
- commit merge base: [8646385076ea4f6ef08682d8ef07a544d3b4ef30](https://github.com/python/cpython/commit/8646385076ea4f6ef08682d8ef07a544d3b4ef30)
- ref: 11f032f904c8019b332a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28110751405)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-3.12.6.md)
- [📈time plot](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-base-mem.svg)
- [📄table](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-base.md)
- [📈time plot](bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f-vs-base.svg)

