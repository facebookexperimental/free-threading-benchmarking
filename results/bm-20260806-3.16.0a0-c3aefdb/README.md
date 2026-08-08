# Results

- fork: python/c3aefdb9eff073405837
- version: 3.16.0a0
- config: 
- commit hash: [c3aefdb](https://github.com/python/cpython/commit/c3aefdb)
- commit date: 2026-08-06T18:09:22+03:00
- commit merge base: [5965f08d702aadfc5ae51134c22261cefbc82da5](https://github.com/python/cpython/commit/5965f08d702aadfc5ae51134c22261cefbc82da5)
- ref: c3aefdb9eff073405837

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31137637182)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260806-vultr-x86_64-python-c3aefdb9eff073405837-3.16.0a0-c3aefdb.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260806-vultr-x86_64-python-c3aefdb9eff073405837-3.16.0a0-c3aefdb-vs-3.12.6.md)
- [📈time plot](bm-20260806-vultr-x86_64-python-c3aefdb9eff073405837-3.16.0a0-c3aefdb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260806-vultr-x86_64-python-c3aefdb9eff073405837-3.16.0a0-c3aefdb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260806-vultr-x86_64-python-c3aefdb9eff073405837-3.16.0a0-c3aefdb-vs-3.13.0rc2.svg)

