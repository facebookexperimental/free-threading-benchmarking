# Results

- fork: python/53d2e14a3081085a12c6
- version: 3.16.0a0
- config: NOGIL
- commit hash: [53d2e14](https://github.com/python/cpython/commit/53d2e14)
- commit date: 2026-08-23T19:52:58Z
- commit merge base: [c1fc4450613e25a864a4dd7c8e875e971643d2b5](https://github.com/python/cpython/commit/c1fc4450613e25a864a4dd7c8e875e971643d2b5)
- commit date: 2026-08-23T19:52:58+00:00
- ref: 53d2e14a3081085a12c6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32676248265)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 86.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.12.6.md)
- [📈time plot](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 97.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.13.0rc2.md)
- [📈time plot](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-base-mem.svg)
- [📄table](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-base.md)
- [📈time plot](bm-20260823-vultr-x86_64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32676248265)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 63.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.12.6.md)
- [📈time plot](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 99.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.13.0rc2.md)
- [📈time plot](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-base-mem.svg)
- [📄table](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-base.md)
- [📈time plot](bm-20260823-macm4pro-arm64-python-53d2e14a3081085a12c6-3.16.0a0-53d2e14-vs-base.svg)

