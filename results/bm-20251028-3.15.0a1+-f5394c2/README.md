# Results

- fork: python/f5394c257ce4118394fe
- version: 3.15.0a1+
- config: 
- commit hash: [f5394c2](https://github.com/python/cpython/commit/f5394c2)
- commit date: 2025-10-28T01:40:41+05:30
- commit merge base: [364ae607d8035db8ba92486ebebd8225446c1a90](https://github.com/python/cpython/commit/364ae607d8035db8ba92486ebebd8225446c1a90)
- ref: f5394c257ce4118394fe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18860046714)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251028-vultr-x86_64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.12.6.md)
- [📈time plot](bm-20251028-vultr-x86_64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-vultr-x86_64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18860046714)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.12.6.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 72.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-f5394c257ce4118394fe-3.15.0a1%2B-f5394c2-vs-3.13.0rc2.svg)

