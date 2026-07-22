# Results

- fork: python/1f649fecb645d70b9c48
- version: 3.16.0a0
- config: 
- commit hash: [1f649fe](https://github.com/python/cpython/commit/1f649fe)
- commit date: 2026-07-20T22:47:43+00:00
- commit merge base: [1c1088b1da5a7484b7b04e90ccc47aa362e709eb](https://github.com/python/cpython/commit/1c1088b1da5a7484b7b04e90ccc47aa362e709eb)
- ref: 1f649fecb645d70b9c48

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29791061110)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260720-vultr-x86_64-python-1f649fecb645d70b9c48-3.16.0a0-1f649fe.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260720-vultr-x86_64-python-1f649fecb645d70b9c48-3.16.0a0-1f649fe-vs-3.12.6.md)
- [📈time plot](bm-20260720-vultr-x86_64-python-1f649fecb645d70b9c48-3.16.0a0-1f649fe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260720-vultr-x86_64-python-1f649fecb645d70b9c48-3.16.0a0-1f649fe-vs-3.13.0rc2.md)
- [📈time plot](bm-20260720-vultr-x86_64-python-1f649fecb645d70b9c48-3.16.0a0-1f649fe-vs-3.13.0rc2.svg)

