# Results

- fork: python/47c5a0f307cff3ed4775
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [47c5a0f](https://github.com/python/cpython/commit/47c5a0f)
- commit date: 2024-12-15T23:17:01+00:00
- commit merge base: [b74c8f58e875d909ce6b5b9dbcddd6d8331d2081](https://github.com/python/cpython/commit/b74c8f58e875d909ce6b5b9dbcddd6d8331d2081)
- ref: 47c5a0f307cff3ed4775

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12343624912)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f.json)

### vs. 3.12.6

- Geometric mean: 1.150x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)
- [📈time plot](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.180x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.238x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base-mem.svg)
- [📄table](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.md)
- [📈time plot](bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12343624912)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f.json)

### vs. 3.12.6

- Geometric mean: 1.215x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)
- [📈time plot](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.240x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.271x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base-mem.svg)
- [📄table](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.md)
- [📈time plot](bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.svg)

