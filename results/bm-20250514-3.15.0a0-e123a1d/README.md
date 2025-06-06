# Results

- fork: python/e123a1d09bcb75aae0c5
- version: 3.15.0a0
- config: 
- commit hash: [e123a1d](https://github.com/python/cpython/commit/e123a1d)
- commit date: 2025-05-14T17:53:51Z
- commit merge base: [ffaeb3dddf17b891301e6f172c87267f59784d00](https://github.com/python/cpython/commit/ffaeb3dddf17b891301e6f172c87267f59784d00)
- commit date: 2025-05-14T17:53:51+00:00
- ref: e123a1d09bcb75aae0c5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15033806196)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.md)
- [📈time plot](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15033806196)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.md)
- [📈time plot](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 51.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d-vs-3.13.0rc2.svg)

