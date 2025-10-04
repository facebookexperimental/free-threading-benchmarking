# Results

- fork: python/18d4e2ecd4e7414ef228
- version: 3.15.0a0
- config: NOGIL
- commit hash: [18d4e2e](https://github.com/python/cpython/commit/18d4e2e)
- commit date: 2025-10-03T21:52:45Z
- commit merge base: [1ae92503647328544866f9586f57eec285e1949a](https://github.com/python/cpython/commit/1ae92503647328544866f9586f57eec285e1949a)
- commit date: 2025-10-03T21:52:45+00:00
- ref: 18d4e2ecd4e7414ef228

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18236829247)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 81.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.12.6.md)
- [📈time plot](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 97.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-base-mem.svg)
- [📄table](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-base.md)
- [📈time plot](bm-20251003-vultr-x86_64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18236829247)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 93.17%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.12.6.md)
- [📈time plot](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x slower (HPT: reliability of 86.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 94.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-base-mem.svg)
- [📄table](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-base.md)
- [📈time plot](bm-20251003-macm4pro-arm64-python-18d4e2ecd4e7414ef228-3.15.0a0-18d4e2e-vs-base.svg)

