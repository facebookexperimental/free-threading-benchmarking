# Results

- fork: python/f62050d65743f0c895f7
- version: 3.16.0a0
- config: NOGIL
- commit hash: [f62050d](https://github.com/python/cpython/commit/f62050d)
- commit date: 2026-07-16T10:37:00-07:00
- commit merge base: [b090d06e7331c40b3c94e70b35a09f785b279e17](https://github.com/python/cpython/commit/b090d06e7331c40b3c94e70b35a09f785b279e17)
- ref: f62050d65743f0c895f7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29545510778)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 94.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-3.12.6.md)
- [📈time plot](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 97.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-base-mem.svg)
- [📄table](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-base.md)
- [📈time plot](bm-20260716-vultr-x86_64-python-f62050d65743f0c895f7-3.16.0a0-f62050d-vs-base.svg)

