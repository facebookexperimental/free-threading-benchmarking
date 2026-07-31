# Results

- fork: python/49f96670d98c50eca769
- version: 3.16.0a0
- config: 
- commit hash: [49f9667](https://github.com/python/cpython/commit/49f9667)
- commit date: 2026-07-29T14:08:45-07:00
- commit merge base: [11d0da5b54b1a162e8f2566675007cfb2db797b5](https://github.com/python/cpython/commit/11d0da5b54b1a162e8f2566675007cfb2db797b5)
- ref: 49f96670d98c50eca769

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30503332076)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260729-vultr-x86_64-python-49f96670d98c50eca769-3.16.0a0-49f9667.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260729-vultr-x86_64-python-49f96670d98c50eca769-3.16.0a0-49f9667-vs-3.12.6.md)
- [📈time plot](bm-20260729-vultr-x86_64-python-49f96670d98c50eca769-3.16.0a0-49f9667-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260729-vultr-x86_64-python-49f96670d98c50eca769-3.16.0a0-49f9667-vs-3.13.0rc2.md)
- [📈time plot](bm-20260729-vultr-x86_64-python-49f96670d98c50eca769-3.16.0a0-49f9667-vs-3.13.0rc2.svg)

