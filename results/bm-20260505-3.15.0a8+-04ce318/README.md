# Results

- fork: python/04ce31852260b3d39e35
- version: 3.15.0a8+
- config: 
- commit hash: [04ce318](https://github.com/python/cpython/commit/04ce318)
- commit date: 2026-05-05T00:44:37Z
- commit merge base: [f025dba62e4deee9cb740cb94dcdf0a9b0a229cc](https://github.com/python/cpython/commit/f025dba62e4deee9cb740cb94dcdf0a9b0a229cc)
- commit date: 2026-05-05T00:44:37+00:00
- ref: 04ce31852260b3d39e35

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25351829340)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318.json)

### vs. 3.12.6

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 99.86%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25351829340)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318.json)

### vs. 3.12.6

- Geometric mean: 1.142x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.md)
- [📈time plot](bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.md)
- [📈time plot](bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.svg)

