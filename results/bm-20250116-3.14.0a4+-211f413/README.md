# Results

- fork: python/211f41316b7f205d18eb
- version: 3.14.0a4+
- config: 
- commit hash: [211f413](https://github.com/python/cpython/commit/211f413)
- commit date: 2025-01-16T16:32:17+00:00
- commit merge base: [f48702dade921beed3e227d2a5ac82a9ae2533d0](https://github.com/python/cpython/commit/f48702dade921beed3e227d2a5ac82a9ae2533d0)
- ref: 211f41316b7f205d18eb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12813755305)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 91.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-base-mem.svg)
- [📄table](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-base.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-base.svg)

