# Results

- fork: python/47c5a0f307cff3ed4775
- version: 3.14.0a2+
- config: 
- commit hash: [47c5a0f](https://github.com/python/cpython/commit/47c5a0f)
- commit date: 2024-12-15T23:17:01+00:00
- commit merge base: [b74c8f58e875d909ce6b5b9dbcddd6d8331d2081](https://github.com/python/cpython/commit/b74c8f58e875d909ce6b5b9dbcddd6d8331d2081)
- ref: 47c5a0f307cff3ed4775

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12343624912)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)
- [📈time plot](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg)

