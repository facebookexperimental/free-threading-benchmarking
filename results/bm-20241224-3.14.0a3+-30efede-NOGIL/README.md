# Results

- fork: python/30efede33ca1fe32debb
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [30efede](https://github.com/python/cpython/commit/30efede)
- commit date: 2024-12-24T05:17:47+08:00
- commit merge base: [d61542b5ff1fe64705e5ce1bcc53048f14098dba](https://github.com/python/cpython/commit/d61542b5ff1fe64705e5ce1bcc53048f14098dba)
- ref: 30efede33ca1fe32debb

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12474785779)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede.json)

### vs. 3.12.6

- Geometric mean: 1.140x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)
- [📈time plot](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.172x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)
- [📈time plot](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.209x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base-mem.svg)
- [📄table](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.md)
- [📈time plot](bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12474785779)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede.json)

### vs. 3.12.6

- Geometric mean: 1.168x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.195x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.229x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base-mem.svg)
- [📄table](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.svg)

