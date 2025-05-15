# Results

- fork: python/e123a1d09bcb75aae0c5
- version: 3.15.0a0
- config: NOGIL
- commit hash: [e123a1d](https://github.com/python/cpython/commit/e123a1d)
- commit date: 2025-05-14T17:53:51Z
- commit merge base: [ffaeb3dddf17b891301e6f172c87267f59784d00](https://github.com/python/cpython/commit/ffaeb3dddf17b891301e6f172c87267f59784d00)
- commit date: 2025-05-14T17:53:51+00:00
- ref: e123a1d09bcb75aae0c5

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15033806196)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json)

### vs. 3.12.6

- Geometric mean: 1.115x faster (HPT: reliability of 96.28%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.md)
- [📈time plot](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 85.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base-mem.svg)
- [📄table](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base.md)
- [📈time plot](bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15033806196)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json)

### vs. 3.12.6

- Geometric mean: 1.014x faster (HPT: reliability of 86.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.md)
- [📈time plot](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 95.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base-mem.svg)
- [📄table](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base.md)
- [📈time plot](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15033806196)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 92.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.md)
- [📈time plot](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x faster (HPT: reliability of 80.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.016x slower (HPT: reliability of 98.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base-mem.svg)
- [📄table](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base.md)
- [📈time plot](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-base.svg)

