# Results

- fork: python/49e83e31bd45e513a3ca
- version: 3.15.0a0
- config: NOGIL
- commit hash: [49e83e3](https://github.com/python/cpython/commit/49e83e3)
- commit date: 2025-09-22T23:46:19+02:00
- commit merge base: [c497694f772763f9e8642603d9f6627675ba64c4](https://github.com/python/cpython/commit/c497694f772763f9e8642603d9f6627675ba64c4)
- ref: 49e83e31bd45e513a3ca

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17932212019)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 87.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.12.6.md)
- [📈time plot](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 96.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-base-mem.svg)
- [📄table](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-base.md)
- [📈time plot](bm-20250922-vultr-x86_64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17932212019)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.12.6.md)
- [📈time plot](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 58.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x slower (HPT: reliability of 99.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-base-mem.svg)
- [📄table](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-base.md)
- [📈time plot](bm-20250922-macm4pro-arm64-python-49e83e31bd45e513a3ca-3.15.0a0-49e83e3-vs-base.svg)

