# Results

- fork: python/009e7b36981fd07f7cca
- version: 3.15.0a0
- config: NOGIL
- commit hash: [009e7b3](https://github.com/python/cpython/commit/009e7b3)
- commit date: 2025-05-18T00:24:40+02:00
- commit merge base: [fc7f4c36664314393bd4c30355e21bd7aeac524d](https://github.com/python/cpython/commit/fc7f4c36664314393bd4c30355e21bd7aeac524d)
- ref: 009e7b36981fd07f7cca

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15090402216)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json)

### vs. 3.12.6

- Geometric mean: 1.135x faster (HPT: reliability of 98.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.12.6.md)
- [📈time plot](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.093x faster (HPT: reliability of 96.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base-mem.svg)
- [📄table](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base.md)
- [📈time plot](bm-20250518-linux-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15090402216)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json)

### vs. 3.12.6

- Geometric mean: 1.013x faster (HPT: reliability of 90.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.12.6.md)
- [📈time plot](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 96.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base-mem.svg)
- [📄table](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base.md)
- [📈time plot](bm-20250518-vultr-x86_64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15090402216)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 93.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.12.6.md)
- [📈time plot](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 80.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base-mem.svg)
- [📄table](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base.md)
- [📈time plot](bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3-vs-base.svg)

