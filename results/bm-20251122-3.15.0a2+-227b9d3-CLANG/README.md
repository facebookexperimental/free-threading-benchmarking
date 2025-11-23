# Results

- fork: python/227b9d326ec7eba35942
- version: 3.15.0a2+
- config: CLANG
- commit hash: [227b9d3](https://github.com/python/cpython/commit/227b9d3)
- commit date: 2025-11-22T21:59:14Z
- commit merge base: [425fd85ca360a39a1a3fb16f09c448cb93ff794a](https://github.com/python/cpython/commit/425fd85ca360a39a1a3fb16f09c448cb93ff794a)
- commit date: 2025-11-22T21:59:14+00:00
- ref: 227b9d326ec7eba35942

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19603194720)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3.json)

### vs. 3.12.6

- Geometric mean: 1.127x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.12.6.md)
- [📈time plot](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.13.0rc2.md)
- [📈time plot](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.044x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-base-mem.svg)
- [📄table](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-base.md)
- [📈time plot](bm-20251122-vultr-x86_64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19603194720)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3.json)

### vs. 3.12.6

- Geometric mean: 1.161x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.12.6.md)
- [📈time plot](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.13.0rc2.md)
- [📈time plot](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-base-mem.svg)
- [📄table](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-base.md)
- [📈time plot](bm-20251122-macm4pro-arm64-python-227b9d326ec7eba35942-3.15.0a2%2B-227b9d3-vs-base.svg)

