# Results

- fork: kumaraditya303/mrocache
- version: 3.16.0a0
- config: NOGIL
- commit hash: [4fbec93](https://github.com/kumaraditya303/cpython/commit/4fbec93)
- commit date: 2026-06-16T14:35:52+05:30
- commit merge base: [11f032f904c8019b332a3c367f335e05cde63628](https://github.com/python/cpython/commit/11f032f904c8019b332a3c367f335e05cde63628)
- ref: mrocache

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28110624942)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 96.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-3.12.6.md)
- [📈time plot](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 98.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-3.13.0rc2.md)
- [📈time plot](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x slower (HPT: reliability of 99.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-base-mem.svg)
- [📄table](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-base.md)
- [📈time plot](bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93-vs-base.svg)

