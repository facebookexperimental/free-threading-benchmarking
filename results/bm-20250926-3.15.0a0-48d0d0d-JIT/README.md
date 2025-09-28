# Results

- fork: python/48d0d0dd9733eae4935f
- version: 3.15.0a0
- config: JIT
- commit hash: [48d0d0d](https://github.com/python/cpython/commit/48d0d0d)
- commit date: 2025-09-26T19:44:36-07:00
- commit merge base: [93ac3525b92f5f8918211a241c01324dfa8b1e5e](https://github.com/python/cpython/commit/93ac3525b92f5f8918211a241c01324dfa8b1e5e)
- ref: 48d0d0dd9733eae4935f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18066689825)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.12.6.md)
- [📈time plot](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 68.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-base-mem.svg)
- [📄table](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-base.md)
- [📈time plot](bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18066689825)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.12.6.md)
- [📈time plot](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 98.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 81.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-base-mem.svg)
- [📄table](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-base.md)
- [📈time plot](bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-vs-base.svg)

