# Results

- fork: python/70154855cf698560dd9a
- version: 3.14.0a2+
- config: 
- commit hash: [7015485](https://github.com/python/cpython/commit/7015485)
- commit date: 2024-12-08T05:57:22+00:00
- commit merge base: [79b7cab50a3292a1c01466cf0e69fb7b4e56cfb1](https://github.com/python/cpython/commit/79b7cab50a3292a1c01466cf0e69fb7b4e56cfb1)
- ref: 70154855cf698560dd9a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12357231006)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.12.6.md)
- [📈time plot](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 75.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.13.0rc2.md)
- [📈time plot](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 98.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base-mem.svg)
- [📄table](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base.md)
- [📈time plot](bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base.svg)

