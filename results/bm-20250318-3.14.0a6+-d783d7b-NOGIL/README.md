# Results

- fork: python/d783d7b51d31db568de6
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [d783d7b](https://github.com/python/cpython/commit/d783d7b)
- commit date: 2025-03-18T23:37:12Z
- commit merge base: [01b5abbc53b2a9ee8d85e0518c98efce27dbd061](https://github.com/python/cpython/commit/01b5abbc53b2a9ee8d85e0518c98efce27dbd061)
- commit date: 2025-03-18T23:37:12+00:00
- ref: d783d7b51d31db568de6

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13936099299)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 99.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.md)
- [📈time plot](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 99.93%, 1.02x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base-mem.svg)
- [📄table](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base.md)
- [📈time plot](bm-20250318-linux-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13936099299)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base-mem.svg)
- [📄table](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13936099299)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b.json)

### vs. 3.12.6

- Geometric mean: 1.013x slower (HPT: reliability of 99.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base-mem.svg)
- [📄table](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-d783d7b51d31db568de6-3.14.0a6%2B-d783d7b-vs-base.svg)

