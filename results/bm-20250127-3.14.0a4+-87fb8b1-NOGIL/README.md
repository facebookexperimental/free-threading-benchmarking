# Results

- fork: python/87fb8b198c1633d9ce0b
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [87fb8b1](https://github.com/python/cpython/commit/87fb8b1)
- commit date: 2025-01-27T18:30:20+08:00
- commit merge base: [7d275611f62c9008c2d90b08c9f21462f80a8328](https://github.com/python/cpython/commit/7d275611f62c9008c2d90b08c9f21462f80a8328)
- ref: 87fb8b198c1633d9ce0b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13004403954)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1.json)

### vs. 3.12.6

- Geometric mean: 1.067x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-3.12.6.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-base-mem.svg)
- [📄table](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-base.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-87fb8b198c1633d9ce0b-3.14.0a4%2B-87fb8b1-vs-base.svg)

