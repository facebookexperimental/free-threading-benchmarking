# Results

- fork: python/c779f2324df06563b4ba
- version: 3.15.0a0
- config: NOGIL
- commit hash: [c779f23](https://github.com/python/cpython/commit/c779f23)
- commit date: 2025-08-28T21:19:15+05:30
- commit merge base: [025a2135eff848abf24f9dc52c81386eea9da397](https://github.com/python/cpython/commit/025a2135eff848abf24f9dc52c81386eea9da397)
- ref: c779f2324df06563b4ba

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17311209060)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 94.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.md)
- [📈time plot](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 97.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.md)
- [📈time plot](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base-mem.svg)
- [📄table](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.md)
- [📈time plot](bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17311209060)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 92.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.md)
- [📈time plot](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 81.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.md)
- [📈time plot](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x slower (HPT: reliability of 99.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base-mem.svg)
- [📄table](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.md)
- [📈time plot](bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.svg)

