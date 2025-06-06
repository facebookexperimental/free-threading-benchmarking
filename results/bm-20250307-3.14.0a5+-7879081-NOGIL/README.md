# Results

- fork: python/78790811989ab47319e2
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [7879081](https://github.com/python/cpython/commit/7879081)
- commit date: 2025-03-07T16:10:02-05:00
- commit merge base: [b1b4f9625c5f2a6b2c32bc5ee91c9fef3894b5e6](https://github.com/python/cpython/commit/b1b4f9625c5f2a6b2c32bc5ee91c9fef3894b5e6)
- ref: 78790811989ab47319e2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13731724455)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-3.12.6.md)
- [📈time plot](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-3.13.0rc2.md)
- [📈time plot](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.132x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-base-mem.svg)
- [📄table](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-base.md)
- [📈time plot](bm-20250307-vultr-x86_64-python-78790811989ab47319e2-3.14.0a5%2B-7879081-vs-base.svg)

