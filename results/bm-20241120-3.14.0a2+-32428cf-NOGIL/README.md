# Results

- fork: python/32428cf9ea03bce6d64c
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [32428cf](https://github.com/python/cpython/commit/32428cf)
- commit date: 2024-11-20T14:54:48-08:00
- commit merge base: [0af4ec30bd2e3a52350344d1011c0c125d6dcd71](https://github.com/python/cpython/commit/0af4ec30bd2e3a52350344d1011c0c125d6dcd71)
- ref: 32428cf9ea03bce6d64c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11978595387)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.12.6.md)
- [📈time plot](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.13.0rc2.md)
- [📈time plot](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [🧠memory plot](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-base-mem.svg)
- [📄table](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-base.md)
- [📈time plot](bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-base.svg)

