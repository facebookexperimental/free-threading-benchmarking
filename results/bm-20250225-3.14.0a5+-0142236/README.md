# Results

- fork: python/014223649c33b2febbcc
- version: 3.14.0a5+
- config: 
- commit hash: [0142236](https://github.com/python/cpython/commit/0142236)
- commit date: 2025-02-25T09:24:48+00:00
- commit merge base: [99088ab081279329b8362e1c24533fa0be303e6f](https://github.com/python/cpython/commit/99088ab081279329b8362e1c24533fa0be303e6f)
- ref: 014223649c33b2febbcc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13692340670)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-3.12.6.md)
- [📈time plot](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-3.13.0rc2.md)
- [📈time plot](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-base-mem.svg)
- [📄table](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-base.md)
- [📈time plot](bm-20250225-vultr-x86_64-python-014223649c33b2febbcc-3.14.0a5%2B-0142236-vs-base.svg)

