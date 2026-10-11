# Results

- fork: corona10/gh_159111
- version: 3.16.0a0
- config: NOGIL
- commit hash: [91f4f86](https://github.com/corona10/cpython/commit/91f4f86)
- commit date: 2026-10-10T22:44:48+09:00
- commit merge base: [7d5dce9b1f0da209d172885e26a5858208f15812](https://github.com/python/cpython/commit/7d5dce9b1f0da209d172885e26a5858208f15812)
- ref: gh_159111

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38101770166)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 69.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.78x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-3.12.6.md)
- [📈time plot](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 86.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.77x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-3.13.0rc2.md)
- [📈time plot](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- [🧠memory plot](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-base-mem.svg)
- [📄table](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-base.md)
- [📈time plot](bm-20261010-vultr-x86_64-corona10-gh_159111-3.16.0a0-91f4f86-vs-base.svg)

