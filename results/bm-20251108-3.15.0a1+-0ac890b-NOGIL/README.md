# Results

- fork: python/0ac890bea79d3e0162c8
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [0ac890b](https://github.com/python/cpython/commit/0ac890b)
- commit date: 2025-11-08T14:22:05-05:00
- commit merge base: [545299773b40fb589cbd5e54d1d597207d9a2a76](https://github.com/python/cpython/commit/545299773b40fb589cbd5e54d1d597207d9a2a76)
- ref: 0ac890bea79d3e0162c8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19200565479)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 87.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.12.6.md)
- [📈time plot](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 97.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.13.0rc2.md)
- [📈time plot](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-base-mem.svg)
- [📄table](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-base.md)
- [📈time plot](bm-20251108-vultr-x86_64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19200565479)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 97.01%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.12.6.md)
- [📈time plot](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 67.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.13.0rc2.md)
- [📈time plot](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.040x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-base-mem.svg)
- [📄table](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-base.md)
- [📈time plot](bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1%2B-0ac890b-vs-base.svg)

