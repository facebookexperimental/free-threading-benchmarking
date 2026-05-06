# Results

- fork: python/17975f92edd2a6a84549
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [17975f9](https://github.com/python/cpython/commit/17975f9)
- commit date: 2026-05-05T14:22:04-07:00
- commit merge base: [4fa5c0428213f9b80a2b3e25e49b52e8596d8528](https://github.com/python/cpython/commit/4fa5c0428213f9b80a2b3e25e49b52e8596d8528)
- ref: 17975f92edd2a6a84549

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25410501186)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 76.69%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 92.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.078x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-base-mem.svg)
- [📄table](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-base.md)
- [📈time plot](bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-base.svg)

