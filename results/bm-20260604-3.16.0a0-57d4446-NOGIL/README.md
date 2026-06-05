# Results

- fork: python/57d444612d9c8a0eab66
- version: 3.16.0a0
- config: NOGIL
- commit hash: [57d4446](https://github.com/python/cpython/commit/57d4446)
- commit date: 2026-06-04T08:00:51+08:00
- commit merge base: [7a468a101268d2b13105f94ae027df8b502d0c87](https://github.com/python/cpython/commit/7a468a101268d2b13105f94ae027df8b502d0c87)
- ref: 57d444612d9c8a0eab66

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26923669671)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 91.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-3.12.6.md)
- [📈time plot](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.79%, 1.01x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-3.13.0rc2.md)
- [📈time plot](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-base-mem.svg)
- [📄table](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-base.md)
- [📈time plot](bm-20260604-vultr-x86_64-python-57d444612d9c8a0eab66-3.16.0a0-57d4446-vs-base.svg)

