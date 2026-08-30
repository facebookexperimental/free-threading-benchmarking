# Results

- fork: python/41b3f0af266b408438ca
- version: 3.16.0a0
- config: JIT
- commit hash: [41b3f0a](https://github.com/python/cpython/commit/41b3f0a)
- commit date: 2026-08-29T22:40:37+01:00
- commit merge base: [c8ca336e6b321a4ff680ea426cc8a84bfb599bd2](https://github.com/python/cpython/commit/c8ca336e6b321a4ff680ea426cc8a84bfb599bd2)
- ref: 41b3f0af266b408438ca

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33283139039)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a.json)

### vs. 3.12.6

- Geometric mean: 1.170x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.12.6.md)
- [📈time plot](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.131x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-base-mem.svg)
- [📄table](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-base.md)
- [📈time plot](bm-20260829-vultr-x86_64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33283139039)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a.json)

### vs. 3.12.6

- Geometric mean: 1.252x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.12.6.md)
- [📈time plot](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.157x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-base-mem.svg)
- [📄table](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-base.md)
- [📈time plot](bm-20260829-macm4pro-arm64-python-41b3f0af266b408438ca-3.16.0a0-41b3f0a-vs-base.svg)

