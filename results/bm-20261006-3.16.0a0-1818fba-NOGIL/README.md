# Results

- fork: python/1818fba7e737320b4241
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1818fba](https://github.com/python/cpython/commit/1818fba)
- commit date: 2026-10-06T23:03:46+02:00
- commit merge base: [6318730aeebdf7282fa9a18aca52af4e87c0c39d](https://github.com/python/cpython/commit/6318730aeebdf7282fa9a18aca52af4e87c0c39d)
- ref: 1818fba7e737320b4241

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37553686157)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 80.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.md)
- [📈time plot](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 97.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.md)
- [📈time plot](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base-mem.svg)
- [📄table](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.md)
- [📈time plot](bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37553686157)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba.json)

### vs. 3.12.6

- Geometric mean: 1.055x faster (HPT: reliability of 84.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.md)
- [📈time plot](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 95.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.md)
- [📈time plot](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base-mem.svg)
- [📄table](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.md)
- [📈time plot](bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.svg)

